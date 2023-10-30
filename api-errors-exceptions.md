# Errors and Exception Handling
**<strong><span style="color:red">Status: Draft</span></strong>**

In programming, errors are referred to as "exceptions". The mechanisms that return useful information about errors are called "exception handlers". 
An API exception handler returns a custom JSON response body with detailed information about the error(s) for human and machine consumers. 
In addition, the handler returns a short description of suggested actions the end-user may take to resolve the error(s). More than three dozen 
HTTP status codes belong to the official IANA Registry (https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml). An API exception handler 
is targeted to a carefully chosen subset of status codes at the 300- and 400-level applicable to API response bodies, provided in the HTTP Status 
Codes documentation ().

| Schema/Standard | Link | 
| -- | -- |
| IBM MQ | https://www.ibm.com/docs/en/ibm-mq/9.1?topic=api-rest-error-handling |
| OGC API Core | https://docs.opengeospatial.org/is/17-069r3/17-069r3.html |
| JSON:API | https://jsonapi.org/format/ |
| RFC 7807 | https://datatracker.ietf.org/doc/html/rfc7807 |


