

You can't override a [[paradigm.oo.components.modifiers.static.method]].

```java
//Can't do this -> Compile time error
class Foo {
    public static void method() {
        System.out.println("in Foo");
    }
}
 
class Bar extends Foo {
    public void method() {
        System.out.println("in Bar");
    }
}
```

Then [[paradigm.oo.components.modifiers.static.overriding.fail]]