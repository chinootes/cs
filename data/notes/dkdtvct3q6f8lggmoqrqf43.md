
Java Collection Framework defines several classes and interfaces to represent group of individual objects as single entity, i.e. [[data.structure]].  

Although, referred to as a framework, it functions more like a library with a collection of classes and interfaces.

💡 Every Collection class is based on some standard data structure.

- All Collection Classes implement [[lang.java.lib.interfaces.marker.serializable]] and [[lang.java.lib.interfaces.marker.cloneable]]

    - Why though?

        Collections $\equiv$ Containers in C++ → used to transfer

        To transfer object from one place to another, it should be **serializable**.

        When sent from one place to another, the receiver makes a copy of it and operates on it → **clonable**

 