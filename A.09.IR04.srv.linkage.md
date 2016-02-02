#A.09.IR04.srv.linkage

**Purpose**: If a linkage for a service is available, the Resource Locator shall be a
valid URL providing one of the following:
* a link to a web with further instructions
* a link to a service capabilities document
* a link to the service WSDL document (SOAP Binding)
* a link to a client application that directly accesses the service

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* the hierarchylevel of resource should be "service" 

**Test method**

The test first checks if a linkage is provided. If none is given, the test will complete successfully.

If one or more are provided. For each linkage the test checks if the linkage element contains an element of type gmd:URL.
The URL is resolved.

If the response indicates a linkage is a service capabilities or WSDL document, some basic params in the service response are analysed. Else a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions or a client application that directly accesses the service).

Any service response should be checked if it provides proper linkage. The service wsdl or capabilities document should have a featuretype that shares the resource unique identification
if WMS/WMTS/WFS, the link is in //layer[identifier={id}&&@authority={codespace}] if Atom, the link is in //feed[@uuidhref={id}&&@namespace={codespace}] 

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.4, Req 4
* [IR MD](README.md#ref_IR_MD) Part B. 1.4

**Test type:** Automated

**Notes**

##Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="linkage"></a> Linkage   | distributionInfo/*/transferOptions/*/onLine/*/linkage
