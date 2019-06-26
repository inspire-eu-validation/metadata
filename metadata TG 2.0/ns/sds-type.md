# SDS Type

**Purpose**: 
Test that exactly one valid service type value is provided.

**Prerequisites**

**Test method**

* Check that the [serviceType](#serviceType) element occurs exactly once in the document.

* Check that the element [serviceType](#serviceType) contains text that shall be "view", "download", "discovery" or "transformation" depending on the kind of the described Network Service.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.2.1.1, Req 4.1
* [Spatial Data Service Type](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/SpatialDataServiceType.es.xml)

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
serviceType <a name="serviceType"></a>   | /gmd:identificationInfo[1]/srv:SV_ServiceIdentification/srv:serviceType/gco:LocalName
