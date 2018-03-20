# Service identification element

**Purpose**: Resource identifier identifying the resource must be given.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The test first checks if a [Service Identification](#serviceIdentification)  is contained in an element <gmd:identificationInfo>
 for identifying an INSPIRE Spatial Data Service.


**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD),4.1.2, Req 3.2


**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="serviceIdentification"></a> ServiceIdentification   | ./gmd:identificationInfo[1]/<srv:SV_ServiceIdentification>
