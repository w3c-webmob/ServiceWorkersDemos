# Maps

This ServiceWorker demo webapp downloads/caches maps for later use. Users often use mapping web apps when on the move. In many cases they use these apps when they are in areas of bad or no connection. In this case a user would be able to download/cache a section of a map (maybe when they are at on their home wifi before leaving) and use this map later.

For this demo webapp you will need to [1] register a ServiceWorker, [2] when a user vists a map when online this map gets 'cached' in a ServiceWorker cache, [3] use 'fetches' to get the map from the cache rather than the server when a user next vists the cached area on the map. 

## More Information / Requirements
Please go ahead and make the app using the brief requirements above! If you want more details requirements see below:

### Zoom Levels
Need to consider what zoom levels of the map need to be downloaded including the zoom level the user is on.
* It may make more sense that all zoom levels from the most granular the user is using and up is downloaded, rather then all levels.
* EXAMPLE: (zoom levels 1-10) This means that if a user is viewing zoom level 5 (medium level of granularity) and they can see the whole of the UK then levels 5-10 will be downloaded (10 will be the whole Earth view). The user will not be able to zoom to levels 4,3,2,1 when offline as they did not visit these online.
* This method helps to make sure in the instance when a user views the whole earth they also don’t accidently download all maps at all zoom levels

## Update
One of the benefits of the web is the fact that the user always (or almost always) sees the most up to date version of any web-app or web-site. When we start introducing complex caching methods the issue arises of when a web-app’s assets have been updated then how does a “cached” web app know this has happened?

In this use case the user should be able to know that they are seeing a cached version of the map, and should see an option to redownload a more up-to-date version. User should then also be informed of any updates to the page if one occured. 

### Questions 
If you have questions please ask them in the issues. Just start a new issue with your question.
