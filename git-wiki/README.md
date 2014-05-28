# Wikipedia offline

This example will demonstrate how a site like Wikipedia could use the controller to offer an offline experience, where the user selects articles they'd like to be availble offline.


# Cache This
User can cache webpages for a simple info-based site. This could be a wiki, a page from a travel site or an article (arguably the user should 'cache' a portion or the page - like the article - rather than a page itself, this use case could be stated as feeding the web in the state it is and not contributing to the evolution of webapps, however, many people still want this use case, so it may still be worth exloring). This could work a little like Evernote Web Clipper.

## Cool additions (optional)
Additons to this app could include some of the other Use Cases that Evernote Web Clipper has; this could include: caching only the selected parts of a page, caching just the article, highlighting sections for cache. 


## Behaviour draft

* User clicks “read later” on an article for the first time
    * Bootstrap code and related imagery requests added to cache, this process fails if any request fails
    * Article html include (different url to article) & device-dependant inline images requests saved, this process fails if any request fails
    * Confirmation given when bootstrap and article caching has completed
    * Otherwise, meaningful error message displayed (by the site, not browser UI)
* User visits homepage
    * Page structure is pulled from bootstrap cache
    * Content such as “article of the day” is fetched via XHR
        * If XHR fails, unobtrusive message indicating the user is offline is displayed in place of content
    * “Available offline” list is populated with articles the user has cached, along with “remove” buttons
* User visits cached article
    * Page structure is pulled from bootstrap cache
    * Cached content is injected into the content area of the page
    * “read later” button displays spinner
    * Additional online-only content fetched via XHR, eg login state
        * Fails silently, or displays small “offline mode” as login state
    * Article html include requested
        * If request succeeds, update content on page and replace cached content with new content
        * If fails, fail silently
        * Remove spinner from “read later” button
* User visits uncached article
    * Page requested from the server (normal request behaviour)
        * If fails due to network failure (no connection), friendly error message displayed, explaining the user is offline, listing article that are available offline
* On navigate, if a check hasn’t been made for 10 minutes, look for updates to the bootstrap and page templates, update accordingly.
* User saves 99 articles for “offline reading” on a large site such as wikipedia. User adds article on “gravity” to their offline list. Want  to  cache that new article without re-requesting the other 99
    *  User visits article on “Gravity” while offline, want to show cached   version straight away but request updates to the article without   requesting the other 99
    * User selects “update all” from a menu, want to update cache for all 100 articles
