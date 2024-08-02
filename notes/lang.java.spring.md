---
id: vtssw70mxi17onoif07cght
title: Spring
desc: ''
updated: 1722107778793
created: 1718987906201
---

Framework for building enterprise-level applications in Java. 



## [[paradigm.attribute oriented]] / Spring Annotations

### Stereotype Annotations

Define purpose of a class. 

Although, these are not just indicators. These annotations also trigger additional behavior and configurations. These additional behaviors and configurations are based on common aaplication patterns.

#### `@Component`

Marks the class as a general-purpose bean (Spring-managed component).

- Main influence here is to make the class eligible for component scanning. This adds the class to application context.
- Also allows using `@Autowired` for [[arch.design.oo.patterns.di]].


#### `@Service`

Marks the class as [[arch.modelling.roles.service]].

Transaction management can automatically be applied to methods in service class.

#### `@Repository`

Marks a class as [[arch.modelling.roles.repository]].


Enables [[arch.modelling.roles.dao]] and persistence related exceptions under Spring's `DataAccessException` hierarchy.


![[lang.java.spring.web.mvc#controller]]

![[lang.java.spring.web.mvc#restcontroller]]


## Multi-value/array configuration

You can provide multiple values to annotation attributes in form of an array.

```java
@RequestMapping(value = "/", method = { RequestMethod.GET, RequestMethod.POST })
```



## References

- [Spring Guides](https://spring.io/guides) 