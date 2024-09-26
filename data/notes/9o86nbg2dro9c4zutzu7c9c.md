
An exception occurs when a class which is not the superclass or which was not originally the superclass is casted.

For example, if Dog is casted to Cat. Or if Dog is upcasted to Animal and we try casting that Animal object to Cat.

It is advised to determine if the class you're downcasting is an instance of the class you're downcasting to.