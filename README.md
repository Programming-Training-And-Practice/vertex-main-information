# Vert.x





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Reactive Programming.](https://github.com/descriptions-of-it-technologies/reactive-programming)
* [Functional Reactive Programming.](https://github.com/descriptions-of-it-technologies/functional-reactive-programming)  
* [Event Loop.](#event-loop) 
* [Event Driven.](#event-driven)
* [Event Bus.](#event-bus)
* [Vertical.](#vertical)
* [Vertex Core.](#vertex-core)
* [Vertex Web.](#vertex-web)
* [Pattern.](#pattern)
* [Commands.](#commands)
* [Articles.](#articles)
* [Conferences.](#conferences)
* [Conference Speakers.](#conference-speakers)
* [Help.](#help)





## About.





## Documentation.
* [VERT.X](https://vertx.io/)




## Event Loop. 



## Workers. 





## Event Driven. 





## Event Bus.
* Point to point
* Request/Response 
* Pub/Sub
* разпределонная комуникационная шына





## Vertical. 




## Verticles.
* Standard
  * Son aquellos que son asincronos
* Worker
  * creado especificamente para ejecutar operaciones sincronas
* Multithread worker
  * es semilar que 'worker' pero permite ejecutar las instancias concurrente





## Vertex Core.





## Vertex Web.





## Pattern.
* [Multi-Reactor.](https://www.google.com/search?q=multi+reactor+pattern&oq=pattern+multi-re&aqs=chrome.1.69i57j0.14644j0j7&sourceid=chrome&ie=UTF-8)





## Commands.
`vertx run [fileName] -cluster` 
флаг "-cluster"  придназначен для того чтобы днный Vertical мог принимать сообщения из других JVM 

`vertx run [fileName] -ha` 
етот узел если он начнет пропадать может бить реплецырован на других узлах нашего кластера 
и в том числе если другие узлы нашего кластера будут пропадать в етот узел тоже можна реплецыроватся

`jps` - show java processes
`kill -9 [processId]` - kill proces   

`vertx run [fileName] -ha -quorum 2`

`java -jar fat.jar -ha` 



## Articles.





## Conferences.
* [Curso Vert.x - Capítulo 1 - Paradigma Digital](https://www.youtube.com/watch?v=QKbntEUAO1E&ab_channel=ParadigmaDigital)
* [Curso Vert.x - Capítulo 2 - Paradigma Digital](https://www.youtube.com/watch?v=pVsmdwgaUWE&ab_channel=ParadigmaDigital)





## Conference Speakers.





## Pros.
* Embedded event bus
* Abstraction over Java Concurrency
* Reactive
* Polyglot





## Cons.
* 




## Help.
