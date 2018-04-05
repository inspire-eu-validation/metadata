# Resource Locator

**Purpose**: If available Resource Locator for Services, is tested if it provides the access point of the service through an 
Internet address containing a detailed description of a spatial data service.

**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

* Check that a resource locator linking to the described Spatial Data Service shall be given if [online access](#onlineAccess) to this service is available.

* The multiplicity of this element is zero or more.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD) 4.1.3.1, Req 3.7

**Test type**: Automated

**Notes**
If no online access is available, but there is a publicly available online resource providing additional information about the described service, 
the URL pointing to this resource shall be given instead.

A Resource Locator encoded using the gmd:CI_OnlineResource element may also include gmd:name, gmd:description, and gmd:function properties.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="onlineAccess"></a> Online Access |  ./gmd:distributionInfo/\*/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/ \*/gmd:linkage/gmd:URL