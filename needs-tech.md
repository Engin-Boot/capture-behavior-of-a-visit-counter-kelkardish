# Visit-counter technical needs

The following scenarios works with an assumption that small local memory
accompanies the sensor.

The visit-counter and server are not dependent on each other for full
functioning of either.

A time-stamp attached with each entry update at the local memory.

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given visit-counter records entries
  When the server restarts
  Then fetch the latest count from the local memory of visit-counter and update
  the count at the server.

Scenario: Reconcile counts if the sensor is offline for a while

  Given visit-counter records entries
  When the sensor reconnects with the server after some downtime
  Then fetch the latest count from the local memory of visit-counter and update
  the count at the server after matching the time-stamp of count that's on the
  server and one on the local visit-counter.
