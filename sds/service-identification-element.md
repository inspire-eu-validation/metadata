# Service Identification Element

**Purpose**: Test that a resource identifier identifying the resource is given.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* Check if a [Service Identification](#serviceIdentification) is contained in the first gmd:identificationInfo element for identifying an INSPIRE Spatial Data Service.


**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD), 4.1.2, Req 3.2


**Test type**: Automated

**Notes**

The multiplicity of this element is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="serviceIdentification"></a> ServiceIdentification   | gmd:identificationInfo[1]/srv:SV_ServiceIdentification
