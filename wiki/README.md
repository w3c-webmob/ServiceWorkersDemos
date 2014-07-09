## Simple wiki
This demo will show ServiceWorkers working in a wiki to give the user an offline experience. ServiceWorkers are being built to work for many use cases; and the wiki use case is one of the most simple and most popular. This demo should:

* allow a user to 'save' articles to view them offline
* when offline, the user should be able to navigate back to these articles and view them.

For this demo you're going to need to [1] register a ServiceWorker [2] detect fetches and [3] use the ServiceWorker cache. For extra-bonus points the demo app could also:

* allow the user to edit an article offline
* allow the user to create an article while offline.

### More Information
Please go ahead and create a demo app based on the info above! If you do want some more in-detail requirements, then please keep reading! More information / requirements:

* User is viewing an article, and clicks “read later” on an article for the first time
    * Bootstrap code and related imagery requests added to a ServiceWorker cache, this process fails if any request fails
    *  Articles in the cache should include the html & device-dependant inline images requests, and this process should fail if any request fails
    *   User should see some confirmation when the article has been saved into the cache
    *   Otherwise, a meaningful error message displayed (by the site, not browser UI)
* User visits homepage
    *   User should see a list of the articles they have saved in the cache
    *   "remove" buttons for the articles the user has saved should be shown and be active
    *   (for bonus points) A wiki often displays an "article of the day", so the main page should try to fetch this via XHR
        *   If XHR fails, unobtrusive message indicating the user is offline is displayed in place of content
* User visits cached article
    *   The page structure is pulled from the ServiceWorker cache
    *   Cached content is injected into the content area of the page
    *   (for bonus points) Some articles may include additional "online-only content" fetched via XHR, eg login state
        *   If offline, this should Fails silently, or displays small “offline mode” as login state
    *   The cached article may have an html include, this is then requested when a user visits this page
        *   If request succeeds (if a user is online), update content on page and replace cached content with new content
        *   If fails, fail silently
* User visits uncached article
    *   The page should be requested from the server (normal request behaviour)
        *   If fails due to network failure (no connection), friendly error message displayed, explaining the user is offline, listing article that are available offline
* On navigate, if a check hasn’t been made for 10 minutes, look for updates to the bootstrap and page templates, update accordingly.
