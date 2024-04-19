---
id: vyx58ro2hbq206ttprvsmie
title: String Conversion
desc: ''
updated: 1712863891091
created: 1712863873567
---

- Conversion from primitive type to String
  - Done through [[lang.java.lib.classes.wrappers]] which override the toString() method
  - Syntax

        ```java
        Integer a = 130;
        String s = a.toString();
        ```

- Conversion from String to primitive type
  - Each wrapper class has a *parse* method → parseXXX()
  - Syntax

        ```java
        int a = Integer.parseInt(s);
        byte b = Byte.parseByte(s);
        
        //Exception
        //Since String is made of chars anyway 
        //considering the String is made of a single character
        char c = s.charAt(0)
        
        ```
