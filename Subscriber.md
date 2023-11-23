A subscriber is a consumer of events from a [[Publisher]]. They do something with the emitted value or completion event. They are the final part in the subscription chain.

Combine provides two subscribers out of the box
- sink - Can provide closures to receive the events
- assign - Can be used to bind the emitted values to some property of models or UI controls via key path.

#Subscriber