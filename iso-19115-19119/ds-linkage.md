# Dataset linkage

**Purpose**: This test checks each resource locator URL to see if it is syntactically correct and if the resource it references can be accessed, in order to determine its type. If the referenced resource is recognized as a Network Service, it checks whether the linkage to the dataset is declared and implemented.

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test checks if a [linkage](#online) is provided. If none is given, the test will complete successfully. If one or more are provided, for each [linkage](#online) the test checks:

* if the [linkage](#online) element contains an element of type gmd:URL.
* if the element content is a syntactically correct URL.
* if the referenced resource is accessible.
* if the response identifies the [linkage](#online) as a known Harmonised Spatial Data Service type or a Network Service type, the test checks if appropriate [linkage](#online) to dataset is available. The [linkage](#online) is established via the Metadata URL for WMS, WFS and Atom based services. Otherwise a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions or a client application that directly accesses the service).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.2.4, Req 3

**Test type**: Automated/Manual

**Notes**

The depencency to [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="online"></a> linkage   | gmd:distributionInfo/\*/gmd:transferOptions/\*/gmd:onLine/\*
