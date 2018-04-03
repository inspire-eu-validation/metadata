# Resource locator

**Purpose**: This test checks if there is a resource or the url that points to a resource that provides
 additional information about the set data set or data set series

**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test checks if a [OnlineResource](#online) is provided. 
The multiplicity of this element is 0 or more. If none is given, the test will complete successfully.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD), 3.1.3.1, Req 1.8

**Test type**: Automated/Manual

**Notes**
A Resource Locator encoded using the gmd:CI_OnlineResource element may also include gmd:name, gmd:description, and gmd:function properties.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="online"></a> OnlineResource   | ./gmd:transferOptions/\*/gmd:onLine/gmd: linkage/gmd:URL
