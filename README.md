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



## Verticles.
* Put simply, a verticle is the fundamental processing unit in Vert.x. The role of a verticle is to encapsulate a 
  technical functional unit for processing events, such as exposing an HTTP API and responding to requests, providing 
  a repository interface on top of a database, or issuing requests to a third-party system. Much like components in 
  technologies like Enterprise JavaBeans, verticles can be deployed, and they have a life cycle.
  Asynchronous programming is key to building reactive applications, since they have to scale, and verticles are 
  fundamental in Vert.x for structuring (asynchronous) event-processing code and business logic.
* verticles have private state that may be updated when receiving events, they can deploy other verticles, and they 
  can communicate via message-passing (more on that in the next chapter). Verticles do not necessarily follow the orthodox 
  definition of actors, but it is fair to consider Vert.x as being at least inspired by actors.
* Standard
  * Son aquellos que son asincronos
* Worker
  * creado especificamente para ejecutar operaciones sincronas
* Multithread worker
  * es semilar que 'worker' pero permite ejecutar las instancias concurrente





## Event Loop. 
* Handler callbacks are run from event-loop threads. It is important that code running on an event loop takes as little 
  time as possible, so that the event-loop thread can have a higher throughput in the number of processed events. 
  This is why no long-running or blocking I/O operations should happen on the event loop.
* That being said, it may not always be easy to spot blocking code, especially when using third-party libraries. 
  Vert.x provides a checker that detects when an event loop is being blocked for too long.
* CONFIGURING THE VERT.X BLOCKED THREAD CHECKER
  The time limit before the blocked thread checker complains is two seconds by default, but it can be configured to a 
  different value. There are environments, such as embedded devices, where processing power is slower, and it is normal 
  to increase the thread-checker threshold for them.
  You can use system properties to change the settings:
    * `-Dvertx.options.blockedThreadCheckInterval=5000` changes the interval to five seconds.
    * `-Dvertx.threadChecks=false` disables the thread checker.
  Note that this configuration is global and cannot be fine-tuned on a per-verticle basis.


## Workers. 





## Event Driven. 





## Event Bus.
* Point to point
* Request/Response 
* Pub/Sub
* разпределонная комуникационная шына





## Vertical. 





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





## Vert.x Modules
* [Vertex Core.](vertx-core.md)
* [Vertex Web.](vertx-web.md)





## Pattern.
* [Multi-Reactor.](https://www.google.com/search?q=multi+reactor+pattern&oq=pattern+multi-re&aqs=chrome.1.69i57j0.14644j0j7&sourceid=chrome&ie=UTF-8)





## Books.





## Articles.





## Conferences.
* [Curso Vert.x - Paradigma Digital](https://www.youtube.com/playlist?list=PL2yjEVbRSX7WuD06zFOXmW_o2CPvCrf7t)





## Conference Speakers.





## Help.


git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autocomplete