# Neotoma

### Short Description

Neotoma is an open-source system intended to help individuals posess and reuse the content they post online.

### Long Description

Neotoma will work for users in three main ways:

1. It will continually monitor the content that users post or otherwise produce online (to applications such as social networks, publishing platforms, bank accounts, etc.) and copy it over to their cloud storage accounts, creating canonical, aggregate records of their online data for personal usage. This is called **Sync**.

2. It will host a RESTful API layer on top of these cloud storage accounts that serves as a conduit for third-party applications to leverage users' records as their data models, reading and writing data as desired by users. This is called **Platform**.

3. It will provide a catalog of these online applications, making it easy for users to discover, set up, and manage new ways to use their personal and publishable data. This is called **Apps**.

Here are some hypothetical, real-world use cases:

- Sarah travels a lot and uses both Foursquare and Yelp to check in at places. She'd like to place an automatically updated map of all the cities and countries she's visited on her personal website. She uses Neotoma to store all of her check-in data on Dropbox and sets up an application that accesses that data to generate such a map on her own domain. Selecting a particular region of the map reveals all of the venues she visited there, highlighting the places she liked or reviewed.

- Joe posts a lot of photos online using Flickr, Instagram and Facebook. He wants to make sure he doesn't lose the memories represented by these photos and their corresponding likes comments, etc. should those services change in the future (maybe Flickr will become neglected by Yahoo again, or Facebook will become unpopular and eventually go the route of MySpace). He uses Neotoma to automatically store copies of his photos from across these services in organized album folders on Google Drive. And he's set up a third-party application with Neotoma that will ask him if he wants to share new photos back out to these services any time he drags them into his Google Drive account, making it more convenient to post photos online in bulk as well.

- Anne continually updates Twitter and Vine with the details of her life, posting tweets, photos and videos. She's close to her family, who would love to get all these updates from her, but they aren't very active on social media. She uses Neotoma to sync her content to iCloud and set up an application that automatically emails a daily update to her mom and a weekly one to the rest of her family, featuring that very content. She sets up another app that takes the content she's posted within an entire year and makes a scrapbook out of it that she can give to her grandparents for the holidays.

- Dan is a prolific writer online, using various platforms such as WordPress, Google+ and Tumblr to distribute his work. However, he's always looking for new gigs and wants to provide a good representation of his best writing whenever asked. So he sets up Neotoma to copy all of his pieces to Adobe Creative Cloud, where he can easily copy and paste snippets into emails or Word documents when asked by potential employers. And he sets up an application that automatically posts a list of his top work, ranked by number of comments and likes, to his LinkedIn profile.

- Barbara is a fitness fanatic. Both she and her trainer want to track how her exercise and diet correlate to her weight, so she uses Neotoma to sync her data from TrackMyRun, Withings and Evernote, which she uses to track her runs, weight and food intake respectively. She also sets up an application that will automatically take all of this information on a monthly basis and compile a spreadsheet that she can share with her trainer to review her progress. TrackMyRun is a startup that later has the bad luck of going out of business, but fortunately she can continue assessing her running times from past years because they've been preserved on Dropbox.

This is just a small sample of the potential ways in which Neotoma could be used to improve individuals' lives online. It's also possible that an additional type of use case will arise once a sufficient number of people use Neotoma, one in which applications are built to facilitate communication directly between Neotoma users themselves, enabling users to treat  cloud storage as the true point of origin for their content and powering all online applications as an extension.

For more details about Neotoma, see:

* __[Overview](overview.md)__: A  verbose (and incomplete) treatise on this project's intent and design
* __[Terms](terms.md)__: Some vocabulary standardized for clarity throughout the documentation
* __[Storage](storage.md)__: Possible storage options for synchronization
* __[Sources](sources.md)__: Possible sources of content for synchronization
* __[Content Types](content-types.md)__: Possible types of content supported for synchronization
* __[User Objectives](user-objectives/overview.md)__: An outline of user objectives intended to be supported by the service's web application, broken down by type

### Organization

Neotoma is an open source software project with core contributors working collaboratively within a greater community. An open source license will be chosen and implemented to make the legal implications of this intent clear.

Most anyone can participate in everything from product planning to code reviews and feature discussions. If you are interested in participating, we encourage you to [join us in Slack](https://neotoma.slack.com). You can [email Mark Hendrickson](mailto:markmhendrickson@gmail.com) to request access.

In order to facilitate collaboration, Neotoma uses GitHub to share not only code but ideas and discussions as well.

### Productization Goals

We are not content on simply drafting specifications and providing source code. [Our hosted version of Neotoma](https://neotoma.io) provides clear value to non-technical and technical users alike.

We strive not only towards a long-term vision that embodies the project's general ideals but short-term releases as well. These releases will incrementally provide more and more value along the lines of the greater vision while ensuring that we get critical feedback from users and the community.

Other individuals and organizations, regardless of their participation as contributors, are free to host their own installations of Neotoma.
