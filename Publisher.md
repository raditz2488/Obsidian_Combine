Publishers are types that can emit **values** over time and then **complete** . 
Once they are done emitting values they complete either with *finish* or *failure*.
After completion the publisher will not emit any value.
The contract of three possible events(value, finish and failure) is so universal that it can be applied to any kind of task like networking, number crunching, user touches etc.
You can avoid looking at your toolbox, for the right tool to grab for the task at hand, be it adding a delegate or a callback closure and just use a publisher.
With publishers error handling is not optional. You need to write code to handle it.
The **Publisher** protocol is generic over two types:
- Output - The type of value the publisher emits
- Failure - The error type that the publisher can complete with if it fails.
With a publisher you always know what type of value it emits and which errors it could fail with.
The completion of Publisher is encapsulated using [[Completion]]
A publisher can emit **finite** or **indefinite** values and a single completion event **synchronously** or **asynchronously** over a period of time.
Combine provides different [[Publishers out of the box]]
#Publisher #Eventsource

