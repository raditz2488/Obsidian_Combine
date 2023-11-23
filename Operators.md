Operators are methods on Publisher protocol that return either the same or another Publisher. This allows us to chain together bunch of operators one after the other. The operator should have an input matching to the previous operator or [[Publisher]].
The previous operator or [[Publisher]] is called upstream. The operators output is called downstream. Operators can be combined to implement a complex subscription chain.
#Operators #Upstream #Downstream
