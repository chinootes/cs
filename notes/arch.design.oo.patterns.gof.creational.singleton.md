---
id: rncr11aflhfcq2i6xx7qgmc
title: Singleton
desc: ''
updated: 1708449165922
created: 1708449071932
---


[[arch.design.oo.patterns.gof.creational]] in which only one instance of a class is allowed.

## What is a **Singleton class?**

Only one instance is allowed

## How to implement it?

To only allow one instance for your class:

1. Create a static object of a class within the class
2. Make default constructor private
3. Create a static method which returns an instance of your class

```java
class Abc{
    public static Abc obj = new Abc();
    int i;
    private Abc();
    public static Abc getInstance(){
        return obj;
    }
}
```

Now, the only way an instance of this class can be obtained is through this method and since the method is static, it will return the same static instance which was the member of your class.

## Why is this implementation eager?

This instance of the class will be created as soon as the class is loaded in the memory. It will be global and will be there in the memory even if its not used.

## How to make it lazy?

Instead of creating, if you just declare the object in the class and create it inside the function, it will become lazy. But this will mean that every time your function is called, it will return a new object. Hence, the class won't be singleton anymore.

```java
class Abc{
    public static Abc obj;
    int i;
    private Abc();
    public static Abc getInstance(){
        obj = new Abc(); // new object eveytime the function is called
        return obj;
    }
}
```

To prevent this, put the initialisation of object into an if condition which checks whether the object is null or not. → This will only create the object, the first time the function is called. Else it will return the old object.

```java
class Abc{
    public static Abc obj;
    int i;
    private Abc();
    public static Abc getInstance(){
        if(obj == null ) obj = new Abc(); // new object created only for the first time
        return obj;
    }
}
```

Although this won't work if simultaneous calls are made to the method from multiple threads.

## How to make it thread safe?

You can make your method *synchronized* to resolve this issue. But this will slow down your app.

```java
class Abc{
    public static Abc obj;
    int i;
    private Abc();
    public static synchronized Abc getInstance(){
        if(obj == null ) obj = new Abc(); // new object created only for the first time
        return obj;
    }
}
```

To solve this, you can perform a double checked locking. That is, don't put synchronize on the function but inside the function. Check if the object is null - twice. Once inside a synchronized block and once outside.

```java
class Abc{
    public static Abc obj;
    int i;
    private Abc();
    public static Abc getInstance(){
        if(obj == null ){
            synchronized(Abc.class){
                if(obj==null) 
                    obj = new Abc(); 
            }
        }
        return obj;
    }
}
```

## What is the best way to implement a Singleton class?

```sql
enum Abc {
    INSTANCE;
}
```

## Why is Singleton pattern/class used?

It is used to provide global point of access to an object. So it can be used in logging, caches, thread pools, configuration settings, device driver objects. Basically, wherever there is a possibility of multiple clients or users accessing and initializing a new object and we don't want that - Singleton design is used.

## Why not create a static class for such requirements?

- Singleton can implement interfaces and extend classes
- Static class will have only static members
- Can be lazily loaded. Static will be initialized when first loaded.
- Stored in heap, static stored in stack
- Clonable
- Can use OO feature of polymorphism

