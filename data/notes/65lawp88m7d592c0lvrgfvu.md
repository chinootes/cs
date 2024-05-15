

```java
class A{
    int x;
    public static void func(){
        x++; //Error
    }
}
```

When you right this, the method doesn't know which 'x' to call. In case of a non-static method, it is understood that its this.x - it is implicit. But in static context, there is no 'this'.

However, if you tell it the object, it can work. But again, this object will be static.

```java
class A{
    int x;
    static A a = new A(); //static object
    public static void func(){
    a.x++; //Works fine
    }
}
```
