## What is event driven programming?
In an event driven app/program there are events and the event handlers. 
An event handler is a piece of code that runs when an event is triggered.
The event is triggered by an event source.
This can be implemented in various different ways as below:
- Notifier & Observer - Achieved with notifications.
	- Event source sends notifications to interested observers
- Delegation - Achieved with protocols
	- Event source informs delegates through a pre established contract
- Callbacks - Achieved with closures
	- Event source executes a closure when it triggers an event
- Timers - Achieved with timers(time driven events)
	- Event source is a timer. When the timer fires it is considered an event and it runs some piece of code.

All these techniques are imperative.

## What is combine?
Combine is an alternative to imperative event driven programming.
**Combine** provides a declarative syntax.
It enables declarations of a process chain which links together pieces of a subscription.
The process chain is a source code.
The leading piece of the chain is a **[[Publisher]]** and the trailing is a **[[Subscriber]]** piece.
This chain represents a **Subscription**.
The **Publisher** is an event source and the **Subscriber** an event observer/consumer.
In particular **Publisher** emits events
	- Data event - Emits some data of the **Output** generic type of the **Publisher**
	- Completion event - with succession
	- Completion event - with an error of the **Publisher's** **Failure** type.
The **Subscriber** receives these events and consumes them.
The process chain can optionally have zero or more **[[Operators]]** in between the **Publisher** and the **Subscriber**.
The **Operator** is a piece in the chain that modifies the event it receives from the piece behind it.
It then sends this modified event to the piece ahead of it in the chain.

## How is it different then async/await?
Combine provides a rich set of operators.
They make a lot of complex common scenarios with asynchronous programming, easy to address.
#Combine #EventDrivenProgramming #Publisher #Subscriber #Operators
