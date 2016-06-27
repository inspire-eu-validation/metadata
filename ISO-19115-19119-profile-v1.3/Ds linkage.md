# Ds linkage

**Purpose**: This test checks each resource locator URL to see if it is syntactically correct and if the resource it references can be accessed, in order to determine its type.
If the referenced resource is recognized as a Network Service, it checks whether the linkage to the dataset is declared and implemented.

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed
* [Hierarchy](Hierarchy.md) must be passed

**Test method**

The test checks if a [linkage](#online) is provided.
If none is given, the test will complete successfully.
If one or more are provided, for each [linkage](#online) the test checks:

* if the [linkage](#online) element contains an element of type gmd:URL.
* if the element content is a syntactically correct URL
* if the referenced resource is accessible.
* if the response identifies the [linkage](#online) as a Harmonised Spatial Data Service or a Network Service, the test checks if appropriate [linkage](#online) to dataset is available.
The [linkage](#online) is established via the Metadata URL for WMS, WFS and Atom based services.

A final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions or a client application that directly accesses the service).


**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.4, Req 3


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="online"></a> Online   | gmd:distributionInfo/*/gmd:transferOptions/*/gmd:onLine/*
