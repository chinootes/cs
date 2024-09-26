
- Private JVM Stack in [[stack|lang.java.jre.memory#stack]] memory is created
- New frame is created and stored in the stack
- [[lang.java.jre.memory.methods.arguments]]
- Frame destroyed when method invocation completes

    A new one will be created again when the method is invoked.

## How are arguments passed in Java?

- Why is Java always 'pass by value'?
    
    Whenever a method is invoked in Java, it is allotted its own stack space. Regardless of the original variable type, each time a method is invoked, a copy for each argument is created in the stack memory and the copy version is passed to the method. Thus, always **pass by value.**
    
- Passing Primitive Arguments
    
    Consider two variables, x and y , of primitive types and thus stored inside the stack memory. when calling a function, two copies are created inside the stack memory (let's say w and z) and are then passed to the method. hence, the original variables are not being sent to the method and any modification inside the method flow is affecting only the copies.
    
    ![Primitive args](/assets/images/2024-04-21-22-31-37.png)
    
- Passing [[lang.java.lib.classes.wrappers]]/[[lang.java.lib.string]] Arguments
    
    Wrappers are stored inside the heap memory with a corresponding reference inside the stack memory. When calling a function, copy for each reference is created inside the stack memory, and the copies are passed to the method. Any change to the reference inside the method is actually changing the reference of the copies and not the original references.
    
    If you change the value of wrapper objects inside the method like this: x += 2, the change is not reflected outside the method, since wrapper objects are immutable. they create a new instance each time their state is modified. String objects work similarly to wrappers, so the above rules apply also on strings.
    
    ![Wrapper/string args](/assets/images/2024-04-21-22-29-04.png)

- Passing [[Collection|lang.java.lib.collection]]/[[lang.java.lib.classes.object]] Arguments
    
    When defining any collection or object in java, a reference is created inside the stack that points to multiple objects inside the heap memory. when calling a function, a copy of the reference is created and passed to the method. the actual object data is referenced by two references, and any change done by one reference is reflected in the other.
    
    ![Collection/object args](/assets/images/2024-04-21-22-29-43.png)