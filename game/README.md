## Game with independently caching levels

This ServiceWorker web app demo will be a game where each level is a different cache group. 

You can go ahead and do this however you wish; a good example would be a 2D platformer based on levels. Each level could have it's own ServiceWorker cache, when a user is visiting the app levels are cached in separate caches (maybe the next 2/3 levels?) which will then be ready for them to load and play as soon as they complete the previous level. 

## More Information / Requirements

* User visited page that was cached in a ServiceWorker cache, the site decides to show them the cached data straight away for performance, then update with fresh data when/if it arrives.

* User visits game’s url
    * If first visit
        * Loading screen delivered (as normal html)
        * Assets for menu screens and non-level specific behaviour (physics engine etc) downloaded and cached
            * If any request fails, error message (not browser UI) shown to user
    * Menu screen shown (using cached assets)
    * Send versions of game logic / menus & each cached level to server, server returns items that are out of date
        * if fail, abort these steps
        * If game logic / menus are out of date
            * Fetch new assets
            * If any request fails, do not cache, abort these steps
            * Once all assets are fetched, cache’em
        * for each out of date level, delete from cache
    * For each undownloaded level (with priority to earlier levels)
        * Download some kind of manifest for level, containing version, level structure and additional assets required
        * Request any additional resources indicated by manifest
        * Once the manifest and all resources have downloaded, commit to cache
        * If any request fails, do not cache, fail silently
* User clicks “play”
    * Level select screen fetched from cache and shown
    * Download progress/success/failure of levels indicated
    * User clicks on level whose download has failed or in progress
        * See “Starting uncached level”
    * User clicks on cached level
        * See “Starting cached level”
* Starting uncached level
    * Show loading screen
    * Restart download if failed
    * Download level data & cache as specified earlier (see “For each undownloaded level”)
    * If succeed
        * See “Starting cached level”
    * Else
        * Show reason as error message
* Starting cached level
    * Load level from cache & begin having fun
    * On level complete
        * If next level cached
            * See “Starting cached level”
        * Else
            * See “Starting uncached level”

### Special Requirement
In this demo we have a special requirement for those of you who want to do something extra: one of the levels should go through an 'update'. The expected behaviour is the user should only be able to play an 'updated' level when 100% of the level has been cached. Of course it will be difficult for us to replicate this, so please go through the experience and just document the results as a .md file!

### Questions 
If you have questions please ask them in the issues. Just start a new issue with your question.
