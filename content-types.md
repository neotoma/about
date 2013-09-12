# Content Types

The following are types of content that Asheville could support for pulling from sources and placing in storage.

* Photos
* Checkins / Locations Visited
* Status Updates
* Blog Posts
* Audio Tracks
* Videos
* Events / Plans
* Links
* Exercise Routes
* Traveled GPS Paths
* Steps
* Weight and BMI
* Friends
* Followers / Subscribers
* Likes (generic, movies, music, TV shows, books, etc)
* Q&A

## Considerations

* We'll probably want to  pull and store these types from sources directly (such as when pulling photos from Instagram and storing them as photos) and indirectly (such as when pulling photos from Instagram and using their meta data to additionally store locations visited). In other words, we can potentially store several types of content for each piece of content pulled from a source, depending on what kind of data it provides us in its entirety.
* When pulling content from various sources, we'll want to de-duplicate content within each type to make sure we don't store more than one copy of the same content, such as the same photo twice (from the same source or different ones).