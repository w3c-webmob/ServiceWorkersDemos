# Service Workers example apps (Work in progress)

In this project, we hope to build a set of reference applications that make full use of [service workers](https://slightlyoff.github.io/ServiceWorker/spec/service_worker/index.html). Currently there are no working demos in this repo. For ServiceWorker demos try out:

### Basic Demos
* [Simple ServiceWorker Registration demo](https://github.com/GoogleChrome/samples/tree/gh-pages/service-worker/registration)
* [Cleveland respondWith demo](https://github.com/GoogleChrome/samples/tree/gh-pages/service-worker/basic)
* [Wiki engine demo](https://github.com/sandropaganotti/service-worker-wiki)
* [isserviceworkerready spec tests](https://github.com/jakearchibald/isserviceworkerready/tree/master/www/demos)
* [Cache All](https://github.com/boopathi/sw-cache-all) - The bare minimum Service Worker to cache all requests from the app.

### Substantial demos
* [Offline News](https://github.com/jakearchibald/offline-news-service-worker)
* [Trained to Thrill](https://github.com/jakearchibald/trained-to-thrill)
* [Tweetdeck offline](https://github.com/jakearchibald/tweetdeck-prototype)



## WE ARE JUST GETTING STARTED
Sorry about going all caps there, but these are all in the earliest stage of development. We are looking for people to help us create these apps! 

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

* [Chrome Canary](http://www.google.com/intl/en/chrome/browser/canary.html). Type: "chrome://flags/" in the URL bar and turn on "enable-service-worker" and "experimental-web-platform-features".

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


