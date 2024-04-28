---
id: 02fn6fs88mdjr1r02gikfuo
title: No pointers
desc: ''
updated: 1713723425342
created: 1713723223035
---

## Why Java doesn't have pointers?

![[programming.components.variable.pointer.against]]

Considering the above points:
- Java has a robust security model and disallows pointer arithmetic for this reason. It would be impossible for the JVM to ensure that code containing pointer arithmetic is safe without expensive runtime checks.
- Java instead provides very good automatic garbage collection which takes care of memory management for you.

    For many people who had previously been forced to deal with [[programming.memory management.manual]] in Pascal/C/C++ this was one of the biggest advantages of Java when it launched.

- Complexity
  
  - **Array access via pointer offsets**
      Java does this via indexed array access so you don't need pointers. A big advantage of Java's indexed array access is that it detects and disallows out of bounds array access, which can be a major source of bugs. This is generally worth paying the price of a tiny bit of runtime overhead.
  - **References to objects**
      Java has this, it just doesn't call them pointers. Any normal object reference works as one of these. When you do `String s="Hello";` you get what is effectively a pointer to a string object.
  - **Passing argument by reference**
      i.e. passing a reference which allows you to change the value of a variable in the caller's scope - Java doesn't have this, but it's a pretty rare use case and can easily be done in other ways. This is in general equivalent to changing a field in an object scope that both the caller and callee can see.

From the sun white paper [The Java Language Environment](http://java.sun.com/docs/white/langenv/Simple.doc2.html):
  
  > Most studies agree that pointers are one of the primary features that enable programmers to inject bugs into their code. Given that structures are gone, and arrays and strings are objects, the need for pointers to these constructs goes away. Thus, Java has no pointer data types. Any task that would require arrays, structures, and pointers in C can be more easily and reliably performed by declaring objects and arrays of objects. Instead of complex pointer manipulation on array pointers, you access arrays by their arithmetic indices. The Java run-time system checks all array indexing to ensure indices are within the bounds of the array.You no longer have dangling pointers and trashing of memory because of incorrect pointers, because there are no pointers in Java.

## References

- [Why Java doesn't support pointers? — Stack overflow](https://stackoverflow.com/questions/9595636/why-java-doesnt-support-pointers)
- [The Java Language Environment - Sun White Paper](http://java.sun.com/docs/white/langenv/Simple.doc2.html)
