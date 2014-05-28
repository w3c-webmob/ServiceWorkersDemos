# Magazine app 

## Prefetch Content

Many apps (e.g. news and blogging) will need to get fresh content from a server. In this use case:

* the app 'shell' is held within a ServiceWorker cache
* some content is also held in a ServiceWorker cache or LocalStorage (this content was originally pulled from a server and displayed to the user on a previous session)
* the app would first try to pull new content from the server
** if succesful display to the user
** if unsuccessful the app takes the last piece of content from another ServiceWorker cache ''or'' from LocalStorage and displays this instead.

The user may benefit from some message to say "you have the most up to date content" (or something similar and less wordy!).

## Cache Age

The user is viewing a page which was served by a ServiceWorker cache. The user is aware that a particular page is 30 days old and some data may not be relevant.

## Cache Index

A user may wish to view pages they have added to a ServiceWorker cache, and then remove them if they wish. In this use case the user can refer to an index of pages they have cached offline, built by the site.

This might work well with the [wiki-read-later](/examples/wiki-read-later) use case.

## Webfonts

 Page uses webfonts, want to cache web font formats used without having to cache other suggested formats. Eg, cache WOFF or TTF, not  both (similar cases for media-query determined imagery).
 
## Server Sync (bg sync)
There are many apps where a user will use some content (possibly when they are offline), and some details of this useage will need to be sent back to a server when the server is available. For example, a newspaper app with a subscription allowance would want to know how many articles a user has consumed whilst offline. 

The test app could cache some content which a user has not yet accessed with ServiceWorker (the content could be articles they are likely to read). Once a user has consumed the content (offline or online) then the data should be sent to a server (for billing, for example). 