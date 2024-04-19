---
id: w71erhkqhzr5ja5mnn2z7tm
title: System Environment
desc: ''
updated: 1713114264919
created: 1713113432692
---

This environment is a system-dependent mapping from names to values which is passed from parent to child processes. Primarily the set of variables that define or control certain aspects of process execution.


## System Properties

Java maintains a set of system properties for its operations. Each java system property is a key-value (String-String) pair.

### System Properties vs Environment Variables

System properties and environment variables are both conceptually mappings between names and values. Both mechanisms can be used to pass user-defined information to a Java process. Environment variables have a more global effect, because they are visible to all descendants of the process which defines them, not just the immediate Java subprocess. They can have subtly different semantics, such as case insensitivity, on different operating systems. For these reasons, environment variables are more likely to have unintended side effects. It is best to use system properties where possible. Environment variables should be used when a global effect is desired, or when an external system interface requires an environment variable (such as PATH).


## References

- [What is System Environment - Stack Exchange](https://sqa.stackexchange.com/questions/5328/what-is-system-environment)
- [Java Process: What is the Environment?](https://stackoverflow.com/questions/28244332/java-process-what-is-the-environment)
- [getenv - Oracle Docs](https://docs.oracle.com/javase/8/docs/api/java/lang/System.html#getenv--:~:text=The%20environment%20is%20a%20system%2Ddependent%20mapping%20from%20names%20to%20values%20which%20is%20passed%20from%20parent%20to%20child%20processes.)
- [System Environment - IBM](https://www.ibm.com/docs/en/aix/7.1?topic=administration-system-environment#:~:text=2022%2D02%2D07-,The%20system%20environment%20is%20primarily%20the%20set%20of%20variables%20that%20define%20or%20control%20certain%20aspects%20of%20process%20execution.,-They%20are%20set)


- [When to use environment variables vs. system properties? - Stack Overflow](https://stackoverflow.com/questions/14026558/when-to-use-environment-variables-vs-system-properties)
- [Java system properties and environment variables](https://stackoverflow.com/questions/7054972/java-system-properties-and-environment-variables)
- [Java System.getProperty vs System.getenv](https://www.baeldung.com/java-system-get-property-vs-system-getenv)

