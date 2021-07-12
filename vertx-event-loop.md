# Vertx Event Loop.

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
* By default, Vert.x creates twice the number of event-loop threads as CPU cores. If you have 8 cores, then a Vert.x
  application has 16 event loops. The assignment of verticles to event loops is done in a round-robin fashion.
* It is possible to tweak how many event loops should be available, but it is not possible to manually allocate a given
  verticle to a specific event loop. This should never be a problem in practice, but in the worst case you can always
  plan the deployment order of verticles.
* The basic rule when running code on an event loop is that it should not block, and it should run “fast enough.”
* Vert.x provides two options for dealing with blocking code: worker verticles and the executeBlocking operation.
* In case, when event loop can't find a handler for an event, event loop can go to an error handler.