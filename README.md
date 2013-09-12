# Asheville

Asheville is a system for owning one's identity, content and
associations online.

### What is it?

In a nutshell, Asheville is a service that continually monitors the information and content that individuals post to various social networks and copies it automatically into their personal cloud storage accounts, such as Dropbox. 

This provides the immediate benefit of automatically backing up their personal data so it's more effectively in those individuals' possession, stored in familiar file formats and into perpetuity regardless of how those social networks function now or into the future.

Furthermore, by synchronizing this data over to personal cloud storage accounts, they gain an important dual nature: both locally stored and Internet-accessible at the same time. This allows Asheville to provide, in turn, an API on top of these individuals' data and make all or some of them accessible to Internet applications, as they choose. An individual could, for example, set up an application that helps them publish a personal website to display the activity they've taken across numerous social networks.

For more explanation of what the service intends to do, see:

* __[Overview](overview.md)__: A more lengthy description of this project's intent and design
* __[Terms](terms.md)__: Some vocabulary standardized for clarity throughout the documentation
* __[Storage](storage.md)__: Possible storage options for synchronization
* __[Sources](sources.md)__: Possible sources of content for synchronization
* __[Content Types](content-types.md)__: Possible types of content supported by Asheville for synchronization
* __[User Objectives](user-objectives/overview.md)__: An outline of user objectives intended to be supported by the service, broken down by type


### Organization

Asheville is an open source software project intended to have no central authority or managing body but rather various contributors working collaboratively within a greater community. We are currently assessing open source licensing options to make the legal implications of this intent clear.

Most anyone can participate in everything from product planning to code reviews and feature discussions. If you are interested in participating, we encourage you to join us in IRC or for a meeting, per further instructions below.

In order to facilitate collaboration, Asheville uses GitHub to share not only code but ideas and discussions as well.

### Productization Goals

We are not, however, content on simply drafting specifications and providing source code. We fully intend to produce a hosted version of Asheville that provides clear value to non-technical and technical users alike.

We strive not only towards a long-term vision that embodies the project's general ideals but short-term releases as well. These releases will incrementally provide more and more value along the lines of the greater vision while ensuring that we get critical feedback from users and the community.

Other individuals and organizations, regardless of their participation as contributors, are free to host their own installations of Asheville.

### IRC

We encourage all collaborators to join our IRC channel whenever working on the project. You can join on the web [here](http://webchat.freenode.net/?channels=asheville) or connect to `#asheville` on Freenode.

### Meetings

Meetings will be held either with Google Hangouts or Skype.

When a meeting is planned, someone will create an issue
under the [meeting](https://github.com/asheville/spec/issues?labels=meet
ing&page=1) tag with information about what's intended for discussion as well as a link to join if it's hosted on Google Hangouts. It's worth commenting on the issue ahead of time if you have something in particular you want to put on the agenda.

Notes will be taken during meetings and added to their respective issues so that those who did not participate can review what was discussed and decided.

### Cost

Initially, core contributors will choose how to distribute basic costs amongst themselves.

### Account Security

Accounts on systems like infrastructure providers will need to be kept private, of course. In this case, credentials and emails are shared among core contributors to prevent siloing access while still upholding security.

### Liability

There are liability concerns with running servers and accepting even minimal user data (such as Dropbox tokens). We will probably need to set up a legal entity to assume responsibility for these concerns.