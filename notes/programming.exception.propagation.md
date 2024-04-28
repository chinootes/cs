---
id: rb96rzpop2hdhbemhk95q3d
title: Exception Propagation
desc: ''
updated: 1708611076526
created: 1708611006327
---


An exception is first thrown from the top of the stack and if it is not caught, it drops down the call stack to the previous method,If not caught there, the exception again drops down to the previous method, and so on until they are caught or until they reach the very bottom of the call stack.This is called exception propagation.

💡 Rule: By default [[programming.exception.types.unchecked]]s are forwarded in calling chain (propagated).

```java
class TestExceptionPropagation{  
 
  void m(){  
    int data=50/0;  
  }  
  
 void n(){  
    m();  
  }  
  
 void p(){  
   try{  
    n();  
   }catch(Exception e){System.out.println("exception handled");}  
  }  
  
 public static void main(String args[]){  
   TestExceptionPropagation1 obj=new TestExceptionPropagation1();  
   obj.p();  
   System.out.println("normal flow...");  
  }  
}
```

```console
Output:exception handled
       normal flow...
```

💡 Rule: By default, [[programming.exception.types.checked]]s are not forwarded in calling chain (propagated).
