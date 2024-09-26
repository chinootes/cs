
**aka REpresentational State Transfer.**

- Set of **architecture principles** => implementation is up to developers
- built for web services and mobile applications => lightweight
- Request for data is usually sent over [[std.web.http]].
- Return message can be in a variety of formats:
  - HTML
  - XML
  - Plain Text
  - [[std.web.json]]

Application is said to be RESTful if it follows these 6 architecture guidelines:

1. [[Client-Server]] architecture composed of clients, servers and resources.
2. [[Stateless]] client-server communication
   - No client content is stored in server between requests i.e. requests don't share any client information on server side.
   - Information about the session's state is held with client
3. Cacheable data to eliminate the need for some client-server interactions.
4. Uniform interface between components => information is transferred in a standardized way instead of being application-specific.  
   > Central feature that distinguishes the REST architectural style from other network-based styles. - Roy Fielding (originator of REST)
5. A layered system constraint => client-server interactions can be mediated by hierarchical layers.
6. [[Code on demand]]: Allowing servers to extend the functionality of a client by transferring executable Code.
    => Also reduces visibility => **Optional**.

