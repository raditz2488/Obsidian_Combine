Just is a publisher that sends a single value and then completes. We initialise a Just object with a value and it immediately emits this value to any subscriber that subscribes to it and then completes immediately.

##### Empirical:
Just sends value synchronously to a subscriber which subscribed and completes.
The same Just which has completed after sending a value to a subscriber, if subscribed to by another subscriber sends a value and completes again.
Thus Just is capable of sending value even after completion, provided the subscription is new.
This behaviour is similar to [[Future]], except the fact that Just does not perform any task, it already has the value stored during its initialisation.