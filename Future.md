Future is a publisher that can perform some task to create a value and then send that value and complete. 
Future sends this value and completion asynchronously.
It does not need a subscriber to start its task and that makes it **greedy**. 
The task is performed in a closure that the Future initialiser provides. 
This task encapsulating closure expects a promise as a parameter, which itself is also a closure and should not be mistaken with the task closure. 
When the task closure is called by the internal implementation of Future, the Future first creates a promise closure and sends it as a param to the task closure. 
When the task completes the task closure flow should call the promise closure whether it be *success* or *failure*. 
The promise closure expects a [[Result]] parameter. 
When the promise is called with the result, the result is stored and **replayed** to every subscriber, which has subscribed to this Future.
##### Empirical:
If a subscriber subscribes before completion of the task by the Future, the Future will complete its task and then send the value and completion to the subscriber.
If a subscriber subscribes after completion of the task by the Future, the publisher will not re-execute the task, but will send the value it stored after completion of the task. This way **Future** will send the value to a new subscriber even if it has completed.
This behaviour is similar to [[Just]], the only difference being that the Future executes a task which cab be asynchronous.