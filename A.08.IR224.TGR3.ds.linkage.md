
# Resource Locator

**Purpose**	

If a linkage is available, a resource locator must be given.
If the resource is a service, the linkage should be checked.

**Test method**	

The test first checks if a linkage is provided. If none is given, the test will complete successfully. 

If one or more are provided. For each linkage the test checks if the linkage element contains an element of type gmd:URL. (todo: if not one or any = empty then ... fail?)
A validity check of the contained URL using regular expressions is performed. 
The URL is resolved (should not throw 404/500).
If the response indicates any of the resources is a service capabilities or WSDL document, else a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions
or a client application that directly accesses the service).


Optional tests:
Each of the responses that are a service should be checked if they provide proper linkage. The service wsdl or capabilities document should have a layer that shares the resources unique identificatien (see md_IR225)

if WMS/WMTS/WFS, the link is in //layer[id={id}&&codespace={codespace}]
if Soap ...
if Atom, the link is in //feed[uuidhref={id}&&namespace={codespace}]

# Context

gmd:distributionInfo/*/gmd:transferOptions/*/gmd:onLine/*

**Reference(s)**	 

IR, Chap. 2.2.4
TG req 3

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |



