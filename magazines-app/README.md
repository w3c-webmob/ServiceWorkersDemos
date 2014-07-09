## Magazine app 

This ServiceWorker demo webapp will allow a user to view a magazine app when offline, and gain some performance benefits by pulling the 'shell' of the app from a ServiceWorker cache. This should show how ServceWorker can be used to get fresh content from a server as a form of a bundle. Here are some detailed requirements:

* The magazine app 'shell' is held within a ServiceWorker cache
* Some content is also held in a ServiceWorker cache or IndexedDB (this content was originally pulled from a server and displayed to the user on a previous session)
* the app would first try to pull new content from the server
  * if succesful display to the user
  * if unsuccessful the app takes the last piece of content from another ServiceWorker cache *or* from other storage and displays this instead.

The user may benefit from some message to say "you have the most up to date content" (or something similar and less wordy!). In this demo you should [1] register a ServiceWorker, [2] add the 'shell' into one ServiceWorker cache [3] add some content into another ServiceWorker cache, [3] use fetching to get content from the cache or server depending on whether a connection to the server was successful. 

### Cache Age
If the user is viewing a page which was served by a ServiceWorker cache, the user should be aware that a particular page is 30 days old and some data may not be relevant.

### Webfonts
If the page uses webfonts we want to cache web font formats used without having to cache other suggested formats. Eg, cache WOFF or TTF, not  both (similar cases for media-query determined imagery).
 
### Questions 
If you have questions please ask them in the issues. Just start a new issue with your question.
