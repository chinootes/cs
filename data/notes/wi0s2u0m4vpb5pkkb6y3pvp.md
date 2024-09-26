

> Test should only fail because of the system under test.

Consider two cases. In the first case, you are testing your code under test which is independent. Now, if an error occurs in your test, you'd know it was because there is something wrong with your code.

Second case - your code depends on some other class or code. Now, if you get error in your unit test, you wouldn't know where the error is coming from. This makes the whole exercise of creating a unit test pointless. You'll still have to investigate which part is causing the error in your machinery despite the test.

## How to ensure test isolation

### Find a [[dev.tests.unit.seam]]

Seams depend on the use case
- [[dev.tests.unit]]s want no dependencies
- Integration/system tests might only isolate a few dependencies
- If you have a small component where three classes that interact very closely, you might not need isolation there because they belong to the same logical problem.
- Anything that depends on time or duration
- You can't wait till February 29th to execute your test

Provide Testability
  Always create classes with interface. That way, if your class is a dependency for another code, the developer can create a test double by simply implementing that interface.

    > Create interfaces for all your classes. Always.
        Interfaces are the heart of testability.
        The users of your code will be grateful.

### Provide an [[arch.design.oo.patterns.di]] mechanism

Implement the interface of the depended-on component
- Interface provided → you are all set
- No interface provided
    - → Convince your colleague to provide an interface
    - → Implement your own interface
      - Only implement the interface methods you need for the test using the keyword `PARTIALLY IMPLEMENTED`

Inherit from the depended-on component
- Redefine the methods where you need to have a test double for
- Drawbacks
      - Not always possible due to [[programming.oo.components.types.final]] definition of the class
      - The risk to execute unwanted code in tests is higher e.g. when methods are added later in the code under test and are forgotten to be REDEFINEd in the subclass
- Implement the test double

### Dependency lookup using [[arch.design.oo.patterns.gof.creational.factory]]

- During tests, the object factory shall return test doubles to the code under test

#### Secure injection

As a test developer, you need a secure technique to inject test doubles into the object factory class

##### Solution - Injector class

- Must only be available for tests. It is therefore declared as test class
- Must be global friend of the factory class to modify object factory class internal

#### Example

```abap
CLASS cl_managed DEFINITION
    PUBLIC
    FINAL
    CREATE PRIVATE
    GLOBAL FRIENDS cl_factory.
    
    PUBLIC SECTION.
    INTERFACES if_managed.
…
```

```abap
CLASS cl_factory DEFINITION
    PUBLIC
    FINAL
    CREATE PRIVATE
    GLOBAL FRIENDS cl_injector.

    PUBLIC SECTION.
    CLASS-METHODS get_managed
    RETURNING VALUE(r_instance)
    TYPE REF TO if_managed.
    PRIVATE SECTION.
    CLASS-DATA g_managed
    TYPE REF TO if_managed.
…

CLASS cl_factory IMPLEMENTATION.
    METHOD get_managed.
    IF g_managed IS NOT BOUND.
    g_managed = NEW cl_managed( ).
    ENDIF.
    r_instance = g_managed.
    ENDMETHOD.
...
```

```abap
CLASS cl_injector DEFINITION
    PUBLIC
    FOR TESTING
    FINAL
    CREATE PRIVATE.

    PUBLIC SECTION.
    CLASS-METHODS inject_managed
    IMPORTING i_test_double
    TYPE REF TO if_managed.
…

CLASS cl_injector IMPLEMENTATION.
    METHOD inject_managed.
    cl_factory=>g_managed = i_test_double.
    ENDMETHOD.
…
```

> Consider a [[arch.design.oo.patterns.gof.creational.factory]] for integration tests that manages your application / component indirections and collects all factory methods.
