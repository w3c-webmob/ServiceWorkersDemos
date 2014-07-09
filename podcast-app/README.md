## A Simple Podcast Subscription / Listening Webapp 

This ServiceWorker demo webapp would allow users to subscribe to a set of podcasts via RSS.  It would then periodically check these RSS feeds for new episodes and sync new episodes to local storage to enable offline listening. 

For this app you will need to [1] register a ServiceWorker, [2] get podcasts via XHR whilst running the in background (maybe as a inactive tab?), [3] save podcasts in a ServiceWorker cache and [4] detect 'fetches' to get podcasts from the cache rather than from a server.

### More Information
Please go ahead and make the app to the brief requirements given above! If you want more in detail requirements please see below. The app should:

- display a menu of available podcasts
- allow user to subscribe to podcasts from the menu or by entering in an RSS feed URL
- pull down RSS feeds when online
- determine if there are new items listed
- download new items if online
- queue for later download if offline
- periodically check if offline or online and download queued files when online
- know when the user is on wifi as opposed to cellular coverage and prompt "are you sure" before downloading over cellular
- allow user to choose podcasts to play from menu generated from RSS feed data
- indicate to user which episodes are unplayed
- mark episodes as played when user plays them
- remove played items from local storage after a configured period of time
- allow user to view and delete episodes

### Questions 
If you have questions please ask them in the issues. Just start a new issue with your question.
