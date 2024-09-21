---
id: hwuuss57w4hy7yl2w392pwb
title: Spring MVC
desc: ''
updated: 1722108354513
created: 1719248735136
---

Submodule within Spring [[lang.java.spring.web]], which provides specific capabilities for implementing [[arch.pattern.mvc]] architecture.

Provides out-of-the-box [[dist.comm.api.rest]] service capabilities.

## Defining web service using annotations

### Stereotypes

#### `@Controller`

Makes [[arch.modelling.roles.controller]]s capable of handling HTTP requests.

Works along with `@RequestMapping` annotation to map HTTP handler methods.

#### `@RestController`

`@Controller` + `@ResponseBody`

Special type of [[arch.modelling.roles.controller]], which combines `@Controller` and `@RequestBody`.

=> Return values of handler methods are automatically serialized into JSON or XML and returned as response.

> NOTE: For the below annotations to work, it is important that the class is annotated with `@Controller` or `@RESTController`. Otherwise, it won't work, there won't be any errors, it simply wouldn't work. 

### Endpoints and [[std.web.http]] methods

- `@RequestMapping` 
- `@GetMapping` 
- `@PostMapping`
- `@PutMapping`
- `@PatchMapping`
- `@DeleteMapping`

### Request, response and parameters

#### Payload and response

Can be specified by `@RequestBody` and `@ResponseBody` (not required if you're using REST Controller) annotation.


#### URI (Path) Params and Query (Request) Params

`/users/{userId}/orders/{status}?search=keyword&page=1`

```java
@GetMapping("/users/{userId}/orders/{status}")
public String getItemUser(@PathVariable String userId, @PathVariable String status, @RequestParam("search") String searchString, @RequestParam int page){
...
}
```

### Consuming Web Service



## References

- [Sprign @RequestParam vs @PathVariable](https://www.baeldung.com/spring-requestparam-vs-pathvariable)  #read-later