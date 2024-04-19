---
id: o570qgvv6bxq30qdjl8x0mn
title: Members of a class
desc: ''
updated: 1708179891332
created: 1708179756720
---

Members of class are entities which are part of the class. These can be categorised on basis of ownership and on basis of their type.

## Categorisation 1: Based on ownership

- **instance**: instance members belong to the object
- **static**: static members belong to the class

## Categorisation 2: Based on type

- **data**: data members are -
  - variables
  - constants
  in a class
- **method**: member methods are methods specified in a class

You can pair any of the categories in categorisation 1 with any of the categories in categorisation 2 to refer to a member of a class more specifically. For example, instance data member, static method, instance member variable etc.  

```java
class Box
 {
   private int length, breadth, height;
  public void setDimension(int l, int b, int h)
   { length=l; breadth=b; height=h;}
  public void showDimension()
  {
  System.out.println(“L = ”+length);
  System.out.println(“B = ”+breadth);
  System.out.println(“H = ”+height);
  }
}
```

Length, breadth, height will be called instance member variables as they will be created only when an instance(object) of a class is created. Similarly, setDimension() and showDimension() are called instance member functions.
