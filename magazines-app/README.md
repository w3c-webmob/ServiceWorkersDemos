# Magazine app 

Many apps (e.g. news and blogging) will need to get fresh content from a server as a form of a bundle. In this use case:

* The app 'shell' is held within a ServiceWorker cache
* Some content is also held in a ServiceWorker cache or IndexedDB (this content was originally pulled from a server and displayed to the user on a previous session)
* the app would first try to pull new content from the server
  * if succesful display to the user
  * if unsuccessful the app takes the last piece of content from another ServiceWorker cache ''or'' from other storage and displays this instead.

The user may benefit from some message to say "you have the most up to date content" (or something similar and less wordy!).

## Cache Age

The user is viewing a page which was served by a ServiceWorker cache. The user is aware that a particular page is 30 days old and some data may not be relevant.

## Webfonts

 Page uses webfonts, want to cache web font formats used without having to cache other suggested formats. Eg, cache WOFF or TTF, not  both (similar cases for media-query determined imagery).