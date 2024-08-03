
## Methods

- `GET` (Read): Used to retrieve data.
- `POST` (Create): To send data for some processing
- `PATCH` (Update/modify): To modify a record with only the updated part. 
- `PUT` (Update/replace): To create or update.
- `DELETE`
- `HEAD`: Like GET but just to get response header (for metadata)
- `CONNECT`: Starts two-way communications with the requested resource. It can be used to open a TCP/IP tunnel.
- `OPTIONS`: To check what HTTP methods are supported by the target system
- `TRACE`: The TRACE method requests that the target resource transfers the received request in the response body. That way a client can see what (if any) changes or additions have been made by intermediaries.


### Mandatory Methods

All general-purpose web servers are required to implement at least the `GET` and `HEAD` methods, and all other methods are considered optional by the specification.


## Response Codes

1. Informational responses (`100`–`199`)
2. Successful responses (`200`–`299`)
3. Redirects (`300`–`399`)
4. Client errors (`400`–`499`)
5. Server errors (`500`–`599`)

### Common Response codes

- 200 OK
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not found
- 405 Method Not allowed
- 408 Request Timeout
- 500 Internal Server error
- 502 Bad gateway


## References

[When should one use CONNECT and GET HTTP methods at HTTP Proxy Server? - StackOverflow](https://stackoverflow.com/questions/11697943/when-should-one-use-connect-and-get-http-methods-at-http-proxy-server)
