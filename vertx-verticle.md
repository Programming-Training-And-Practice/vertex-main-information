# Verticle.

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
* An each verticle receives its unique deployment ID. This is a string object and the deployment ID is represented in a UUID v4 format.





## The life cycle of any Vertx verticle has following stages:
1. The Vertx instance calls the init() method of a verticle. This method is already implemented in the AbstractVerticle
   class, although you have to provide your own implementation, if you use the Verticle interface, you have to provide
   your own implementation). It provides to the verticle references to Vertx and Context instances. Please note, that
   by default, there is one Vertx instance per JVM.
2. The Vertx instance calls the start() method to execute its startup logic. Based on the Promise object’s result, it
   can either be successfully completed (which means, that the verticle is ready to deploy), either it can fail (which
   means, that the verticle would not be deployed)
3. The Vertx instance deploys the verticle. An each verticle receives its unique deployment ID. This is a string object
   and the deployment ID is represented in a UUID v4 format.
4. The Vertx instance calls the stop() method to execute a termination callback. This means, that this is a place to do
   work that is required before closing, for example, save data or clean used resources.
5. The Vertx instance undeploys a verticle.