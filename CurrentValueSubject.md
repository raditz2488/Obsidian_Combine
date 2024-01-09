CurrentValueSubject is a publisher that can be used to send values imperatively.
It stores the value that it send for replay in case a new subscriber subscribes.
When a value is send by the CurrentValueSubject it stores it internally.
Since it holds the recently sent value, when a new subscriber subscribes it sends the recently stored value to the subscriber. 
Any values sent by the CurrentValueSubject after subscription are also received by the subscriber.
This is what separates it from [[PassThroughSubject]].