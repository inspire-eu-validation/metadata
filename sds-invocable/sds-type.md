# SDS Type

**Purpose**: 

Test that a valid service type value for invocable spatial data services is provided.

**Prerequisites**

**Test method**

* Check that the [serviceType](#serviceType) element occurs exactly once in the document.

* Check that the element [serviceType](#serviceType) contains text and the value of the element is equal to "other" for all Invocable Spatial Data Services.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.3.1.1, Req 5.1
* [Spatial Data Service Type](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/SpatialDataServiceType.es.xml)

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="serviceType"></a>Service Type | gmd:identificationInfo[1]/srv:SV_ServiceIdentification/srv:serviceType/gco:LocalName
