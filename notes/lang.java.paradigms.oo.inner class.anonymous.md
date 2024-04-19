---
id: i3hw5ksyabjb19n4zawipqu
title: Anonymous Inner Class
desc: ''
updated: 1712937141120
created: 1712937118927
---

```java
main()
{ 
A obj = new A();
 {
 func(){
 Syso("This is an anonymous class")
  }
 }
}
```

OR (post Java 8)

```java
main()
{ 
A obj = () -> Syso("anonymous class")

}
```
