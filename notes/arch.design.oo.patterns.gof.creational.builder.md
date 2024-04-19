---
id: 17wxn37m1g5w5cuc9to3fk2
title: Builder String
desc: ''
updated: 1708451747234
created: 1708451730684
---

Used to write readable and understandable code to set up complex objects.

Whenever you create a class with some members, you pass the values you want them to have to the constructor while creating object. This could get very complex if there are too many members of different types.

Create another (builder) class with all the same members and setters of individual members and return object of the builder class.

```java
Phone newphone = new PhoneBuilder().setOS().setBattery().getPhone() 
//getPhone gives the object of Phone type
```

No need to specify all the values too. Set only the values you want. Rest will have default values.
