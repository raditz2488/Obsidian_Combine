A subscription is formed between a [[Publisher]] and a [[Subscriber]]. The steps undertaken are as below:
1. [[Publisher]] and [[Subscriber]] are created.
2. The subscribe(:) method of the [[Publisher]] is called, passing the [[Subscriber]] as the parameter.
3. The implementation of subscribe(:) calls receive(subscriber:).
4. The implementation of receive(subscriber:) will create a [[Subscription]] object.
5. Then the [[Publisher]] calls the method receive(subscription:) on the [[Subscriber]] and passes the [[Subscription]] created in the last step as the parameter.
6. The [[Subscriber]] then calls the request(:) method of the [[Subscription]]


#WIP
