# Cache based on Personalisation

User’s data would have been stored in some form ready to be used for personalisation. Cache will have been setup to receive content. User has the ability consume content relevant to them whether offline or online

## Description
The app may want to cache some assets for the user so they have a smooth UI when offline or on low connectivity networks. Larger apps have the issue where the number and total size of their assets is too large (e.g. a music library). In this case the app should be able to cache assets to the USER based on the user personalisation or maybe history (given consent).

## More fun
User can alter what is / is-not stored in a cache (or caches) in some sort of config file or settings.

## Cache Progress

There are a few ways a user may like to be made aware of a ServiceWorker cache update or progress. Below are the use cases for this:

* The user is informed of cache population progress
* The user is shown an app-specific loading screen between pages, indicating that the resource isn't instantly showable (perhaps offering alternatives that are)