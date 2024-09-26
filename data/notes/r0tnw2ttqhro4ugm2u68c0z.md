


If class B is inside class A => B is a member and an [[lang.java.paradigms.oo.inner class]]

```java

main()
{ 
A obj = new A();
A.B obj1 = obj.new B();
}

//If j is member of class B
obj1.j=5;
```

## `.class` files generated in this case:

`A.class`
`A$B.class`
