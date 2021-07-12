# Vert.x





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Asynchronous Programming.](https://github.com/descriptions-of-it-technologies/asynchronous-programming)
* [Reactive Programming.](https://github.com/descriptions-of-it-technologies/reactive-programming)
* [Functional Reactive Programming.](https://github.com/descriptions-of-it-technologies/functional-reactive-programming)  
* [Event Loop.](#event-loop) 
* [Event Driven.](#event-driven)
* [Event Bus.](#event-bus)
* [Vertical.](#vertical)
* [Vertx Modules.]()
* [Pattern.](#pattern)
* [Commands.](#commands)
* [Articles.](#articles)
* [Conferences.](#conferences)
* [Conference Speakers.](#conference-speakers)
* [Help.](#help)





## About.





## Documentation.
* [VERT.X](https://vertx.io/)
* [Cluster Manager.](https://vertx.io/docs/vertx-hazelcast/java/)



## The Vert.x instance.
* The Vert.x instance is being shared by multiple verticles, and there is generally only one instance of Vertx per JVM process.





## Workers.
* Worker verticles are a special form of verticles that do not execute on an event loop. Instead, they execute on worker 
  threads, that is, threads taken from special worker pools. You can define your own worker thread pools and deploy 
  worker verticles to them.
* Worker verticles can be used to process blocking I/O and long-running operations.    





## Worker thread pool. 





## Context. 
* Context data
* It is possible to mix code with both Vert.x and non-Vert.x threads by using event-loop contexts.







## Event Driven.





## Cluster Manager.
* [Hazelcast(default)](https://github.com/descriptions-of-it-technologies/hazelcast)
* [Apache Zookeeper.](https://github.com/descriptions-of-it-technologies/zookeeper)
* [Apache Ignite.](https://github.com/descriptions-of-it-technologies/apache-ignite)
* [Infinispan.](https://github.com/descriptions-of-it-technologies/infinispan)





## Cluster HA.





## Pros.
* Embedded event bus
* Abstraction over Java Concurrency
* Reactive
* Polyglot





## Cons.
* 






## Pattern.
* [Multi-Reactor.](https://www.google.com/search?q=multi+reactor+pattern&oq=pattern+multi-re&aqs=chrome.1.69i57j0.14644j0j7&sourceid=chrome&ie=UTF-8)





## Books.





## Articles.
* [Vert.x microservices: an (opinionated) application](https://medium.com/@victorgil_91367/vert-x-microservices-an-opinionated-application-56e44c0b45b4)
* []()




## Conferences.
* [Curso Vert.x - Paradigma Digital](https://www.youtube.com/playlist?list=PL2yjEVbRSX7WuD06zFOXmW_o2CPvCrf7t)





## Conference Speakers.





## Useful Links.
* [What's the difference between the send and publish methods of Vertx's EventBus?](https://stackoverflow.com/questions/56715200/whats-the-difference-between-the-send-and-publish-methods-of-vertxs-eventbus)
* [Vert.x microservices: an (opinionated) application](https://medium.com/@victorgil_91367/vert-x-microservices-an-opinionated-application-56e44c0b45b4)
* []()





## Help.
