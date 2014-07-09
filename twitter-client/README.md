##Twitter-client

In this ServiceWorker demo app a user is viewing a twitter client which allows for the following behaviour offline:

* consumes a feed.
* replay offline actions (favorite, reply, tweet).

The user will then be able to read tweets offline, and do simple actions such as favourite, reply or tweet. Of course since the user is offline then these actions will not be 'seen' on twitter until a user is back online, so when a connection is once again established and the user vists the app a 'sync' will occur which pushes their activity back online. 

For this app you will need to [1] register a ServiceWorker, [2] save items to the cache, [3] use background sync when a user regains a connection after appearing offline.

### More Information
Please feel free to make the app according to the above guidelines without reading anymore! But if you want more information on flow please see below:

* User visits app online
  * Twitter feed is downloaded and saved to ServiceWorker cache (it doesn't matter how many are saved, this is a demo, but go for stress testing if you're not sure!)
  * User interacts with app as normal
* User vists the app when appearing 'offline'
  * User should see the feed as it was cached from their last visit
  * User should be able to read the tweets
  * User should be able to 'favourite' the tweets
  * User should be able to submit a new tweet
  * User activity should be saved in a ServiceWorker cache
* User 'appears' to be back online, and visits the app
  * The 'activity' which was saved when a user was offline is synced to the server.

