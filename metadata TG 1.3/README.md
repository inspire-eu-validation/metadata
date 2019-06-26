# Abstract Test Suite: INSPIRE Metadata Technical Guidance

The specification specifies the following conformance classes:

| Conformance class | Standardization target |
| ----------------- | ---------------------- |
| [INSPIRE Profile based on EN ISO 19115 and EN ISO 19119](./iso-19115-19119/README.md) | ISO 19115/19119 metadata record |
| [XML encoding](./xml-encoding/README.md) | XML document (MD_Metadata) |

## Rules for HTTP requests

The INSPIRE technical guidance documents are in general unspecific on the details of HTTP requests to access resources. The following rules apply to all HTTP requests unless a test case explicitly states deviations from these rules.

### Use of HTTPS

Where HTTP is mentioned as the protocol, HTTPS may be used, too. SSL certificates must be valid and issued by a trusted Certification Authority.

This also implies that where "HTTP URI" or "URL" is used, this includes URIs in the HTTPS scheme.

### HTTP methods

If a HTTP request is a request to an INSPIRE network service that is an OGC Web Service only HTTP GET and/or HTTP POST may be used as only the requriements for these methods are specified. Which of the two methods must or can be used in general depends in the requirements stated in the OGC standard and the support for the methods stated in the Capabilities document of a service. Where the choice is constrained by a requirement in the technical guidance, this information is included in the test method description of the test case. If both GET and POST are allowed and supported the service, the executable test is free to choose one of the two.  

For requests to other resources that are accessed using a HTTP URI without payload, HTTP HEAD may be used, too, as HTTP 1.1 states that "the methods GET and HEAD MUST be supported by all general-purpose servers". "Other resources" are identified by the lack of query parameters "SERVICE" and "REQUEST" which are part of all OGC Web Service KVP GET requests.

No conditional GET requests may be used to avoid the impact of HTTP caches. 

### HTTP headers

If a non-INSPIRE dependency (e.g. an OGC standard) specifies requirements on HTTP headers in requests or responses, these must be taken into account in the implementation of tests. This includes, for example, requirements on the content type.

Unless explicitly noted in a test case, no additional HTTP headers should be sent as part of the request or expected as part of the response.  

### HTTP status codes

The expected status code for HTTP GET and POST responses is 200, the expected status code for HTTP HEAD responses is 200 and 204. All other status codes indicate a failure (unless a test case specifies different conditions).
 
Notes:
 
* In OGC Web Services the code 200 is often also used for service exceptions and tests may need to distinguish exceptions from successful completions of a request.
* Redirects (status codes 301, 302, and 303) are in general not allowed as they are not supported by the OGC Web Service standards.

### HTTP timeouts

The timeout for HTTP requests in tests is 30 seconds (unless a test case specifies different conditions).

### HTTP authentication

Until an approved INSPIRE technical guidance for HTTP authentication mechanisms exists, this Abstract Test Suite will not support INSPIRE spatial data services that require HTTP authentication.

I.e., testing of protected resources will require a local installation of the validator in order to connect to the protected service directly (bypassing the security gateway).

### Typical assertions for HTTP requests

Based on the rules specified above, the following assertions may typically be tested for a HTTP response. The first two apply to all responses, the others only in the case of specific requirements stated in the test case.

1. Response is returned within the timeout limits
2. Response has an expected HTTP status code
3. Response has an expected media type in the content-type header
4. Response content meets certain expectations

For example, in the case of an XML response, typical types of expectations regarding the content are: 

* the response is schema valid
* the root element is an expected element (e.g. a Capabilties document) or not a forbidden element (e.g. an ows:ExceptionReport)   
