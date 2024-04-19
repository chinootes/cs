---
id: x3o9601w94tnkmzjeoc1f60
title: System
desc: ''
updated: 1713121976754
created: 1712994244922
---

```java
class Java.lang.System extends Object
```

System class provides means and interfaces to interact with the [[lang.java.jre]],[[lang.java.jre.jvm]] and [[lang.java.jre.system]].

## Facilities provided by System Class

1. Standard input stream
2. Standard output stream
3. Error output stream
4. Access to externally defined properties and environment variables
5. Means of loading files and libraries
6. Some utility methods for quickly copying a portion of an array and getting hashcode.

## Fields

Following are the standard streams within the System class. All streams are open and ready to supply data.

- **`public static final InputStream in`:**

    Typically this stream corresponds to keyboard input or another input source specified by the host environment or user.

- **`public static final PrintStream out`:**

    Typically this stream corresponds to display output or another output destination specified by the host environment or user.

    💡`println()` is a method of the `PrintStream` class. We can access it from the `out` static member of `System` class. Thus, `System.out.println()`.

- **`public static final PrintStream err`:**

    Typically this stream corresponds to display output or another output destination specified by the host environment or user.

---

- Why are there two separate streams for output and error when error can be displayed on the output screen itself?

    By convention, this output stream is used to display error messages or other information that should come to the immediate attention of a user even if the principal output stream, the value of the variable out, has been redirected to a file or other destination that is typically not continuously monitored.


## Methods

All methods in System class are [[paradigm.oo.components.types.static]].



### To interact with [[lang.java.jre]] and [[lang.java.jre.system]] 
- `String clearProperty(String key)`
- `String getProperty(String key)`
- `String getProperty(String key, String def)`
- `String setProperty(String key, String def)`
- `Properties getProperties()`
    Determines the current Java System Properties
- `Map getenv()`
    Returns an unmodifiable String Map view of the current system environment
- `String getenv(String name)`
    Gets the value of the specified environment variable.
- `SecurityManager getSecurityManager()`
    Get the system security interface
- `void setSecurityManager(SecurityManager s)`
    Sets the system security
- `String lineSeperator()`
    Returns the system-dependent line separator String    

### To interact with [[lang.java.jre.jvm]] 

- `Console console()`
    Returns the unique Console object associated with the current Java virtual machine, if any.
- `long currentTimeMillis`
    Returns current time in milliseconds
- `long nanoTime()`
   Returns the current value of the running Java Virtual Machine’s high-resolution time source, in nanoseconds.

- `void exit()`
   
    Terminates the currently running JVM

    ```java
        class Runtime{
            void exit(int status){...}
        }
    ```

    - The argument serves as a status code; by convention, a nonzero status code indicates abnormal termination.
    - This method calls the exit method in class Runtime. This method never returns normally.
    - The call `System.exit(n)` is effectively equivalent to the call: `Runtime.getRuntime().exit(n)`

- `void gc()`

    Calling the gc method suggests that the Java Virtual Machine expend effort toward recycling unused objects in order to make the memory they currently occupy available for quick reuse. When control returns from the method call, the Java Virtual Machine has made a best effort to reclaim space from all discarded objects.

- `void runFinalization()`
    Request to JVM to run finalization for discarded objects.
- `Channel inheritedChannel`
    Return the channel inherited from the entity that created this JVM


### I/O Methods

- `void setErr(PrintStream err)`
    Reassigns the "standard" error output stream
- `void setIn(InputStream in)`
    Reassigns the "standard" input stream
- `void setOut(PrintStream out)`
    Reassigns the "standard" output stream               


### Methods for loading files/libraries

- `void load(String filename)`

    Loads a code file with the specified filename from the local file system as a dynamic library.

    filename = complete path + name

- `void loadLibrary(String libname)`

    Loads the system library specified by the libname argument (The manner in which a library name is mapped to the actual system library is system dependent)


- `String mapLibraryName(String libname)`

    Maps a library name into a platform-specific string representing a native library


## Utility Methods

- `void arrayCopy(Object source, int sourceStart, Object Target, int targetStart, int Size)`

- `int identityHashCode(Object x)`

    Returns the same hash code for the given object as would be returned by the default method hashCode().

