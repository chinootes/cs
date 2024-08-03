[[arch.design.oo.patterns.di]] 


### Spring Container

Core component of Spring which is responsible for managing bean lifecycle.

### Injection 

### Annotations 

#### `@Lazy`

Instantiates bean only when required.

```java
 ...
 @Autowired
    public A(@Lazy B b) {
        this.b = b;
    }
...
```

#### `@DependsOn`

Specified dependency explicitly to control order of instantiation.

```java
@Component
@DependsOn("b")
public class A {
    private final B b;   
}
```



### [[concepts.dependency.cyclic]]

#### What does Spring do?

When a cyclic dependency is detected, Spring automatically uses [[concepts.dependency.cyclic.early reference resolution]] to partially initialize beans by injecting a proxy, and injecting the actual dependency later.

#### What can you do using Spring features?

In case of circular dependencies, the behavior depends on the kind of [[arch.design.oo.patterns.di]] mechanism you use.

##### Use [[arch.design.oo.patterns.di.setter]]

In such cases, [[arch.design.oo.patterns.di.constructor]] will causes `BeanCurrentlyInCreation`[[lang.java.exceptions]] - should be avoided.

[[arch.design.oo.patterns.di.setter]] or [[arch.design.oo.patterns.di.field]] allow Spring to break down the injection into a two-step process to resolve the dependencies:

1. **Instatiation**: Spring instantiates the beans without the dependencies.
2. **Injection**: Spring injected the (already initialized) dependencies.

[[arch.design.oo.patterns.di.field]] is anyway discouraged, so use [[arch.design.oo.patterns.di.setter]] as a best practice.

##### `@Lazy` annotation 

Can help manage dependencies by delaying the initialization until the bean is actually needed.

##### `@DependsOn` annotation

Doesn't necessarily resolve circular dependency but can help in specifying order of instatiation.

#### Handling it yourself (recommended)

