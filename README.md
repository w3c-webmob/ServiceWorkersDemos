We hope to build a set of reference applications that make full use of [service workers](https://slightlyoff.github.io/ServiceWorker/spec/service_worker/index.html). However, currently there are no working demos in this repo.

## For ServiceWorker demos try out:

### Service Worker recipes

- [Basic registration](https://googlechrome.github.io/samples/service-worker/registration/index.html) -
a bare-bones sample that simply performs service worker registration, with placeholders for various event handlers.
- [Detailed registration](https://googlechrome.github.io/samples/service-worker/registration-events/index.html) -
a sample that provides detailed information about the service worker registration and the state changes that a
service worker undergoes.
- [Prefetching resources during installation](https://googlechrome.github.io/samples/service-worker/prefetch/index.html) -
a sample demonstrating how to prefetch and cache a list of URLs during the service worker's installation, ensuring that they're
available offline.
- [Selective caching](https://googlechrome.github.io/samples/service-worker/selective-caching/index.html) -
a sample of how a service worker can cache resources "on the fly", assuming the resources meet certain criteria (MIME type,
domain, etc.).
- [Read-through caching](https://googlechrome.github.io/samples/service-worker/read-through-caching/index.html) -
a sample of caching _all_ resources that are requested "on the fly", unconditionally.
- [Offline Google Analytics](https://googlechrome.github.io/samples/service-worker/offline-analytics/index.html) -
extends the [read-through caching](https://googlechrome.github.io/samples/service-worker/read-through-caching/index.html) example to add in support for "replaying" failed Google Analytics pings, allowing pages to submit Google Analytics data associated with offline/cached page views.
- [Fallback responses](https://googlechrome.github.io/samples/service-worker/fallback-response/index.html) -
a sample illustrating how you can return alternative "fallback" content if an initial fetch request fails.
- [Mock responses](https://googlechrome.github.io/samples/service-worker/mock-responses/index.html) -
a sample illustrating how you can return content created on the fly in response to a page's requests.
- [Using `postMessage`](https://googlechrome.github.io/samples/service-worker/post-message/index.html) -
a sample illustrating the use of `postMessage()` to send commands from a controlled page to its service worker, giving the page control over the cache.


### Basic Demos
* [Wiki engine demo](https://github.com/sandropaganotti/service-worker-wiki)
* [isserviceworkerready spec tests](https://github.com/jakearchibald/isserviceworkerready/tree/master/src/demos)
* [Cache All](https://github.com/boopathi/sw-cache-all) - The bare minimum Service Worker to cache all requests from the app.

### Substantial demos
* [Offline News](https://github.com/jakearchibald/offline-news-service-worker)
* [Trained to Thrill](https://github.com/jakearchibald/trained-to-thrill)
* [Tweetdeck offline](https://github.com/jakearchibald/tweetdeck-prototype)



<hr>




## This repo is just getting started
All the code in this repo is  in the earliest stage of development. We are looking for people to help us create these apps! 

Our goal is to show how you can perform tasks that are common in native applications using this new set of APIs. We want to keep the apps simple, so they can be easily bisected and copied by anyone.

**Please note that the spec and implementations are in a very early stage!** You may find issues with implementations in that they may often change or produce strange results at first. : 

**To see what actually works in browsers today, see Jake Archibald's [IsServiceWorkerReady](https://jakearchibald.github.io/isserviceworkerready/) page.**

### How can you help? 
The process below is a guideline to how to get started.

1. Fork this repo! 
1. Choose one of the apps from the directories above.
1. Use the app's behavior draft to implement the application. 
1. Keep it really simple! See our list of resources below to learn about service workers.  

## How to run these things?
We will be hosting them on a website soon, so you can see them as we build them. 

Right now, you will need:

* [Chrome](https://www.google.com/chrome/browser/desktop/index.html).
* [Opera](http://www.opera.com/pl/computer/windows).

## Wanna build something different?
If you have a more interesting app you want to build, please add them to this repo. Just add a directory to the root directory with a README.md file explaining what the app does and send us a pull request! 

##Resources

* [The specification](https://slightlyoff.github.io/ServiceWorker/spec/service_worker/index.html).

### Articles/Vidoes 

* [ServiceWorkers and Firefox](https://hacks.mozilla.org/2014/06/serviceworkers-and-firefox/) - Introduction to ServiceWorkers on Firefox!
* [Service Worker - first draft published](http://jakearchibald.com/2014/service-worker-first-draft/) - Introduction and tutorial including code snippets!
* [Video: The ServiceWorker: The network layer is yours to own](https://www.youtube.com/watch?v=4uQMl7mFB6g) - video introducing ServiceWorker including HTTP caching, request, and showing SW in forms, the basis for push messaging, alarms, geofencing and background sync.

### Debugging

* ServiceWorkerInternals (chrome canary only - chrome://serviceworker-internals/) - page for debugging ServiceWorkers in chrome, including stopping, unregistering and starting workers.

### Examples

* [Jake Archibald's Trained to Thrill](https://jakearchibald.github.io/trained-to-thrill/) - Jake made a great demo app which pulls in images from Flickr, uses fetch, uses cache (not implemented yet) and worker registrations.
* [Simple ServiceWorker](https://github.com/matthew-andrews/serviceworker-simple) - A simple Service Worker example by Matt Andrews.

### Related APIs

* [Promises HTML5Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/) - Understanding Promises (used frequently in ServiceWorkers especially in fetch, cache). 
* [The Basics of Web Workers](http://www.html5rocks.com/en/tutorials/workers/basics/) - Understanding concurrency in JavaScript and how web workers work.


