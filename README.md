# Use-cases & Examples for ServiceWorker

This directory contains use cases and examples for ServiceWorker. It was constructed to ensure the spec captures use-cases & identify areas the API could cater for common patterns.

## Test Cases and Demos

The [W3C Web and Mobile Interest Group](https://www.w3.org/wiki/Mobile/Work) would like to support the work the ServiceWorker team by turning these use cases into real demo apps. We can then use these apps to test ServiceWorker, and provide feedback to the spec team to adjust things if necessary.

### Process
If you wish to get to work on some of these items then fantastic! The process below is a guideline to how to get started.

1. Choose one of the use cases / examples, these are given in the directories of this directory [/examples](https://github.com/w3c-webmob/ServiceWorker/tree/master/examples).
2. In 'Issues' find the Use Case and let us know you're working on it!
4. Start building a demo application using an implementation of ServiceWorker
5. Document the process explaining:

* What was easy
* What was difficult
* Behaviour of the ServiceWorker (did it do [a] what it was supposed to do and [b] what you logcally expected it would do?)
* Answer whether the ServiceWorker satisfied the use case
* Anything else you think is relevant!

Documentation doesn't need to be too verbose! Just a short report will suffice. Once we have collected a good number of case examples we will send a Pull Requestto the main ServiceWorker repo. 

## Implementations
Implementations of ServiceWorker are given below. The spec and implementations are in a very early stage! You may find issues with implementations in that they may often change or produce strange results at first. We encourage everyone to submit bugs to the browser vendor in which they experience bugs.

* Chrome: Behind a flag. Check at [chromestatus](http://www.chromestatus.com/features/6561526227927040)
* Firefox: [Build for Nightly](http://blog.nikhilism.com/2014/05/serviceworker-implementation-status-in-firefox.html)

No other browsers implement ServiceWorker as of 20/05/2014.

## What's next?
After we have collected some use case demos and tests we will send a Pull Request to the main ServiceWorker repo so the ServiceWorker spec team can make any adjustments or feel content that they did an awesome job! It will be up to the ServiceWorker team how they go about making any adjustments or using the data that our demos / tests produced. 

## More Use Cases
If you have more use cases please add them to this repo! Fork the repo, add a directory to the /examples/ directory complete with a README.md file explaining the use case in an much detail as you can. Then make a pull request!
