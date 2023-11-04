Publishers are types that can emit events over time. Once they finish emitting values they complete either with success or failure.
After completing the publisher will not emit any value.
The contract of three possible events is so universal that it can be applied to any kind of task like networking, number crunching, user touches etc.
You can avoid looking at your toolbox, for the right tool to grab for the task at hand, be it adding a delegate or a callback closure and just use a publisher.
With publishers error handling is not optional. You need to write code to handle it.
The **Publisher** protocol is generic over two types:
- Output - The type of value the publisher emits
- Failure - The error type that the publisher can throw if it fails.
With a publisher you always know what value it emits and which errors it could fail with.
#Publisher #Eventsource

