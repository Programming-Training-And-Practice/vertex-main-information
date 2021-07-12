# Vertx Event Bus.





## Event Bus.
* разпределонная комуникационная шына





## The Eventbus class provides three approaches to send messages: 
1. publish()
2. send()
3. request()





## 
* 'event bus' concept is implemented in the EventBus class.
* There is a single event bus instance for every Vert.x instance.
* An interesting fact to know about the Vert.x Event bus implementation, is that it allows you to utilize bridges, which 
  extend communication possibilities of the Event Bus. For instance, TCP Event Bus bridge, which is built on top of TCP
  protocol, allows any application that can create TCP sockets to interact with a remote Vertx instance using the event bus. 
  A different way to communicate with the Event bus outside the JVM is by using Sock JS library. With this approach you
  need to register a Sock JS handler, that enables your application to communicate with JavaScript web applications.
* Please note, that by default, the EventBus class transports data as a generic Object class. You need to register a 
  custom codec if you would like to send your own entity classes via the Event Bus and to specify it in using the MessageConsumer class.




  
## Producer.
* publish/subscribe ('broadcasting', 'single publisher to many consumers')
* Point to point (single publisher and a single consumer)
* Request/Response





## Consumer.
* Each consumer has its own address, which can be any string (however, it is highly recommended to establish some kind 
  of a naming convention for a project).
  




## Message.
* It is represented by the Message class and is more than just a plain data. You can understand it as a container.