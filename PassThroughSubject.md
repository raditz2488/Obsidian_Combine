PassThroughSubject is a publisher that can be used to send values imperatively. 
It does not store any value. 
Rather it simply sends the value passed as a parameter in the send function. 
Since it does not hold any value, when a new subscriber subscribes it does not receive the recent value that was send by the PassThroughSubject.
Any values sent by the PassThroughSubject after subscription are received by the subscriber.
This is what separates it from [[CurrentValueSubject]].
