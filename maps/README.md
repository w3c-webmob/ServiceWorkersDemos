# Maps

Downloads/caches maps for later use. Users often use mapping web apps when on the move. In many cases they use these apps when they are in areas of bad or no connection. In this case a user would be able to download/cache a section of a map (maybe when they are at on their home wifi before leaving) and use this map later.

## Possible Requirements
### Zoom Levels
* Need to cinsider what zoom levels of the map need to be downloaded including the zoom level the user is on.
** It may make more sense that all zoom levels from the most granular the user is using and up is downloaded, rather then all levels.
** EXAMPLE: (zoom levels 1-10) This means that if a user is viewing zoom level 5 (medium level of granularity) and they can see the whole of the UK then levels 5-10 will be downloaded (10 will be the whole Earth view). The user will not be able to zoom to levels 4,3,2,1 when offline as they did not visit these online.
* This method helps to make sure in the instance when a user views the whole earth they also don’t accidently download all maps at all zoom levels

### Note
'''Offline or Low Connectivity?'''
Distinction needs to be made between offline and low connectivity. If a USER caches a map and accesses it on low connectivity does the app attempt to get a new version or use the cache? 

## Update
One of the benefits of the web is the fact that the user always (or almost always) sees the most up to date version of any web-app or web-site. When we start introducing complex caching methods the issue arises of when a web-app’s assets have been updated then how does a “cached” web app know this has happened?

In this use case the user should be able to know that they are seeing a cached version of something, and should see an option to redownload a more up-to-date version. User should then also be informed of any updates to the page if one occured. 

