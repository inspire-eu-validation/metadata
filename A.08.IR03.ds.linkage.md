#A.08.IR03.ds.linkage

**Purpose**: If a linkage is available, a resource locator must be given.
If the resource is a service, the linkage should be checked.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if a [linkage](#online) is provided. If none is given, the test will complete successfully.

If one or more are provided. For each linkage the test checks if the linkage element contains an element of type gmd:URL.

The URL is [resolved](./README.md#resolve).

If the response indicates a linkage is a service capabilities or WSDL document, some basic params in the service response are analysed.
Else a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions
or a client application that directly accesses the service).

Any service response should be checked if it provides proper linkage. The service wsdl or capabilities document should have a featuretype that shares the [resource unique identification](A.07.IR05.IR06.ds.identification.md)

if WMS/WMTS/WFS, the link is in //layer[identifier={id}&&@authority={codespace}]
if Atom, the link is in //feed[@uuidhref={id}&&@namespace={codespace}]

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.4, Req 3
* [IR MD](README.md#ref_IR_MD) Part B. 1.4

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="online"></a> Online   | gmd:distributionInfo/*/gmd:transferOptions/*/gmd:onLine/*
