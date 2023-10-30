# HTTP Status Codes
A critical component to a well designed API is a comprehensive set of HTTP status codes that clients should be prepared to recieve. Every response should 
contain a status code that describes the nature of the response and accurate characterization of errors when they occur. Suggested response body schemas of errors codes returned by 
an API are available here: [[().

| Code | Description |
| -- | -- | 
| 200 | A successful request. |
| 302 | The target resource was found but resides temporarily under a different URI. A 302 response is not evidence that the operation has been successfully completed. |
| 303 | The server is redirecting the user agent to a different resource. A 303 response is not evidence that the operation has been successfully completed. |
| 304 | An entity tag was provided in the request and the resource has not changed since the previous request. |
| 307 | The target resource resides temporarily under a different URI and the user agent MUST NOT change the request method if it performs an automatic redirection to that URI. |
| 308 | Indicates that the target resource has been assigned a new permanent URI and any future references to this resource ought to use one of the enclosed URIs. |
| 400 | The server cannot or will not process the request due to an apparent client error. For example, a query parameter had an incorrect value. |
| 401 | The request requires user authentication. The response includes a WWW-Authenticate header field containing a challenge applicable to the requested resource. |
| 403 | The server understood the request, but is refusing to fulfill it. While status code 401 indicates missing or bad authentication, status code 403 indicates that authentication is not the issue, but the client is not authorized to perform the requested operation on the resource. |
| 404 | The requested resource does not exist on the server. For example, a path parameter had an incorrect value. |
| 405 | The request method is not supported. For example, a POST request was submitted, but the resource only supports GET requests. |
| 406 | Content negotiation failed. For example, the Accept header submitted in the request did not support any of the media types supported by the server for the requested resource. |
| 500 | An internal error occurred in the server. |
  
  
## Additional Resources
1. A complete list of HTTP response status codes is provided in the MDN Web Documentation (https://developer.mozilla.org/en-US/docs/Web/HTTP/Status).  
2. Comprehensive documentation that describes the entire OGC family of API standards is provided here (https://ogcapi.ogc.org/)  
