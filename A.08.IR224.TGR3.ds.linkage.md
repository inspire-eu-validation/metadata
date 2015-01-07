
# Resource Locator

**Purpose**	

If a linkage is available, a resource locator must be given.
If the resource is a service, the linkage should be checked.

**Test method**	

The test first checks if a [linkage](#online) is provided. If none is given, the test will complete successfully. 

If one or more are provided. For each linkage the test checks if the linkage element contains an element of type gmd:URL. 

The URL is [resolved](./README.md#resolve).

If the response indicates a linkage is a service capabilities or WSDL document, some basic params in the service response are analysed.
Else a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions
or a client application that directly accesses the service).

Any service response should be checked if it provides proper linkage. The service wsdl or capabilities document should have a featuretype that shares the [resource unique identification](A.07.IR225.TGR5.ds.identification.md) 

if WMS/WMTS/WFS, the link is in //layer[identifier={id}&&@authority={codespace}]
if Atom, the link is in //feed[@uuidhref={id}&&@namespace={codespace}]

# Context

**Reference(s)**	 

* IR, Chap. 2.2.4
* TG req 3

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="online"></a> Online   | gmd:distributionInfo/*/gmd:transferOptions/*/gmd:onLine/*



