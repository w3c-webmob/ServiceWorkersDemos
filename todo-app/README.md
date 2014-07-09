## todo (Single page app)

This ServiceWorker demo app makes a simple to-do app work in an offline mode. AppCache was great at doing things like this, so we're particularly interested in making sure ServiceWorker is just as useful for these use cases! More details below:

### More Details
First of all, create a basic web-based todo app; it can follow a framework, be one you made earlier, or made from scratch. Then, use ServiceWorker to get the following use cases worker:

* User visits todo app
    * If the app is cached
        * Fetch from cache
        * Check for updated application
        * If update found / no cache exists
            * Download new resources
            * Once all downloaded successfully
                * Clear cache
                * Add downloaded content to cache
                * If “interacted with”
                    * Show “Update available” message
                * Else
                    * Refresh page
    * Else
        * Deliver page and resources normally
        * Once all resources are successfully download, add to cache
    * On UI interaction (changing the state of the page)
        * Mark page as “interacted with”

For this app you will need to [1] register a ServiceWorker [2] detect fetches to see when the app is loaded [3] use the ServiceWorker cache to load into and from. 

### Questions 
If you have questions please ask them in the issues. Just start a new issue with your question.
