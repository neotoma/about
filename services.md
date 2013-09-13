# Services

This document briefly outlines each service in the proposed asheville
infrastructure. It covers the name, purpose and brief design overview
of each service.

## Diagram

Initially, we started talking about the infrastructure visually. This
is what we came up with.

![infra](https://f.cloud.github.com/assets/28991/1130003/4b638fd6-1b9a-11e3-9b25-a0f331ceeba0.png)

You can see more brief discussion of that in [#5](https://github.com/asheville/spec/issues/5).

### List of Services

This is a current list of each service.

#### asheville.io

Purpose:

The central marketing website, user authentication and OAuth endpoints,
as well as sync status viewer.

Design:

This will be almost all HTML views. To retrieve data, it will talk
to Accounts. It will contain model representations of the
data being retrieved over JSON, in this case a user account.

- Authenticate users with a storage solution (i.e Dropbox)
- Show user status of their sync
- Display marketing pages explaining how the service works

API Interactions:

- Accounts
- Sync Conductor
- *Platform (planned)*

Technology:

To start, it will be built with Python/Flask to keep development fast,
as the other services will be the same. Possibly a JavaScript application
on the frontend for the sign-up and sync pages.

#### Accounts

Purpose:

A JSON interaction layer for the accounts database. The accounts API is
the choke point for user data that is persisted.

Design:

- Return a JSON representation of a user based on some unique identifier
- Create a user based on tokens provided from asheville.io
- Delete and update users based on interactions from asheville.io

API Interactions:

- asheville.io
- Storage
- Sync Conductor
- *Platform (planned)*

Technology:

Flask/Python for the JSON API, Postgres for a datastore.

#### Sync Conductor

Purpose:

An API for checking the status of syncs, cancelling, restarting,
queing.

Design:

- Create a sync based on a user ID for all connected networks
- Create a sync based on a user ID for specific networks
- Show status of a sync for a user ID, for each network
- Cancel a sync for a user based on ID

API Interactions:

- asheville.io
- Accounts
- Sync Workers

Technology:

We'll use Celery to manage queues and workers.

The queue for processing messages will initially be Redis, as it is
dead simple to set-up. If needed, this will move to RabbitMQ in the future.

Celery is backend agnostic, so this change won't require re-writing workers
and administration.

Initially, we'll create a very basic Flask/Python API to complete the tasks
outlined above. This will then talk to celery.

Running task data will be stored in the same Redis database like this:

"running:user_id [1, 2, 3]" where 1, 2, 3 are running celery tasks. This
lets us check worker status based on a user ID. Holding the state like this
is the simplest way to communicate with celery with business logic like "user_id".

#### Sync Worker(s)

Purpose:

A worker talks to an external network, like Twitter or Facebook.

It then parses the social network data, formats it for communication with
the Platform and posts the data there. At that point it has done it's job.

There will be many workers. It will all be contained within one codebase.

API Interactions:

- Platform
- Sync Conductor (via Celery queue)

Technology:

Simple – each worker is a Celery worker. It does the hard work. This worker
picks up jobs designed for it and processes them, returning task status results
to Celery.

#### Storage

This is just the Dropbox API, or whatever backend is used.

#### Platform

Purpose:

The platform is an API and caching layer to interact with Storage. In
order to store or retrieve data from storage, you must go through the platform.

Design:

- Store data in a users storage system (authenticated)
- Retrieve data from a users storage system (authenticated)

Initially the platform API will be very simple, but will eventually
be the interaction point for 3rd party developers building on top
of Asheville.

Technology:

Flask/Python for the JSON API. Redis for caching storage data. This includes
"snapshots", brief pieces of user data, i.e thumbnails or filenames,
used to show sync status. Snapshots are collected on intervals
based on file changes, if that status can be request from the storage API.

Later on, "hot" user data will be cached for short periods of time to enable
a fast API experience, instead of going all the way through to the storage
backend. Passthroughs will be optional here, as well.
