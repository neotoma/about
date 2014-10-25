# Asheville

### Short Description

Asheville is an open-source system intended to help individuals better posess and reuse the content they post online.

### Long Description

Asheville will work for users in three main ways:

1. It will continually monitor the content that users post or otherwise produce online (to applications such as social networks, publishing platforms, bank accounts, etc.) and copy it over to their cloud storage accounts, creating canonical, aggregate records of their online data for personal usage. This is called **Sync**.

2. It will host a RESTful API layer on top of these cloud storage accounts that serves as a conduit for third-party applications to leverage users' records as their data models, reading and writing data as desired by users. This is called **Platform**.

3. It will provide a catalog of these online applications, making it easy for users to discover, set up, and manage new ways to use their personal and publishable data. This is called **Apps**.

Here are some hypothetical, real-world use cases:

- Sarah travels a lot and uses both Foursquare and Yelp to check in at places. She'd like to place an automatically updated map of all the cities and countries she's visited on her personal website. She uses Asheville to store all of her check-in data on Dropbox and sets up an application that accesses that data to generate such a map on her own domain. Selecting a particular region of the map reveals all of the venues she visited there, highlighting the places she liked or reviewed.

- Joe posts a lot of photos online using Flickr, Instagram and Facebook. He wants to make sure he doesn't lose the memories represented by these photos and their corresponding likes comments, etc. should those services change in the future (maybe Flickr will become neglected by Yahoo again, or Facebook will become unpopular and eventually go the route of MySpace). He uses Asheville to automatically store copies of his photos from across these services in organized album folders on Google Drive. And he's set up a third-party application with Asheville that will ask him if he wants to share new photos back out to these services any time he drags them into his Google Drive account, making it more convenient to post photos online in bulk as well.

- Anne continually updates Twitter and Vine with the details of her life, posting tweets, photos and videos. She's close to her family, who would love to get all these updates from her, but they aren't very active on social media. She uses Asheville to sync her content to iCloud and set up an application that automatically emails a daily update to her mom and a weekly one to the rest of her family, featuring that very content. She sets up another app that takes the content she's posted within an entire year and makes a scrapbook out of it that she can give to her grandparents for the holidays.

- Dan is a prolific writer online, using various platforms such as WordPress, Google+ and Tumblr to distribute his work. However, he's always looking for new gigs and wants to provide a good representation of his best writing whenever asked. So he sets up Asheville to copy all of his pieces to Adobe Creative Cloud, where he can easily copy and paste snippets into emails or Word documents when asked by potential employers. And he sets up an application that automatically posts a list of his top work, ranked by number of comments and likes, to his LinkedIn profile.

- Barbara is a fitness fanatic. Both her and her trainer want to track how her exercise and diet correlate to her weight, so she uses Asheville to sync her data from TrackMyRun, Withings and Evernote, which she uses to track her runs, weight and food intake respectively. She also sets up an application that will automatically take all of this information on a monthly basis and compile a spreadsheet that she can share with her trainer to review her progress. TrackMyRun is a startup that later has the bad luck of going out of business, but fortunately she can continue assessing her running times from past years because they've been preserved on Dropbox.

This is just a small sample of the potential ways in which Asheville could be used to improve individuals' lives online. It's also possible that an additional type of use case will arise once a sufficient number of people use Asheville, one in which applications are built to facilitate communication directly between Asheville users themselves, enabling users to treat  cloud storage as the true point of origin for their content and powering all online applications as an extension.

For more details about Asheville, see:

* __[Overview](overview.md)__: A  verbose (and incomplete) treatise on this project's intent and design
* __[Terms](terms.md)__: Some vocabulary standardized for clarity throughout the documentation
* __[Storage](storage.md)__: Possible storage options for synchronization
* __[Sources](sources.md)__: Possible sources of content for synchronization
* __[Content Types](content-types.md)__: Possible types of content supported for synchronization
* __[User Objectives](user-objectives/overview.md)__: An outline of user objectives intended to be supported by the service's web application, broken down by type

### Status

Asheville is still under initial development and therefore not ready for end users yet. 

However, latest versions of the [frontend interface code](https://github.com/asheville/web) are pushed to GitHub Pages and can be previewed at [asheville.github.io/web](http://asheville.github.io/web). Built-in simulations make it possible to experience what it may be like to set up a real account with Asheville once ready.

If you're a developer, you can view and fork the current code base, which has been made fully available during development. See the other repos in the Asheville organization for code that powers its various services. We encourage you to contribute per below.


### Mailing List

Want to receive general announcements about Asheville, such as when it's ready?

[Leave us your name and email address](https://docs.google.com/forms/d/1i2iHhLVcfhYIEHPS5G7iD0gC4z-K-2e535GLGrj_qNE/viewform) and we'll let you know!

### Organization

Asheville is an open source software project with core contributors working collaboratively within a greater community. An open source license will be chosen and implemented to make the legal implications of this intent clear.

Most anyone can participate in everything from product planning to code reviews and feature discussions. If you are interested in participating, we encourage you to join us in IRC or for a meeting, per further instructions below.

In order to facilitate collaboration, Asheville uses GitHub to share not only code but ideas and discussions as well.

### Productization Goals

We are not content on simply drafting specifications and providing source code. We fully intend to produce a hosted version of Asheville that provides clear value to non-technical and technical users alike.

We strive not only towards a long-term vision that embodies the project's general ideals but short-term releases as well. These releases will incrementally provide more and more value along the lines of the greater vision while ensuring that we get critical feedback from users and the community.

Other individuals and organizations, regardless of their participation as contributors, are free to host their own installations of Asheville.

### Product Management

The following tools are used in addition to GitHub to manage product design and development:

- __Trello__ for high-level sprint specification, organization and status tracking: [Product Sprints](https://trello.com/b/gN599TRG/product-sprints)

- __Pivotal Tracker__ for low-level development ticket specification, prioritization and tracking: [Sync](https://www.pivotaltracker.com/n/projects/1059342) and [Web](https://www.pivotaltracker.com/n/projects/951914)

### IRC

We encourage all collaborators to join our IRC channel when working on the project. You can [join on the web](http://webchat.freenode.net/?channels=asheville) or connect to `#asheville` on Freenode (irc://irc.freenode.net/asheville) with your favorite client.