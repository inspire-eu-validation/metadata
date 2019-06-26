# SDS Type

**Purpose**: Test that exactly one name describing the type of spatial data service is given.

**Prerequisites**

**Test method**

* Check if the [serviceType](#serviceType) element occurs exactly once in the document.

* Check if the [serviceType](#serviceType) element contains text that equals one of the types given in [Spatial Data Service Type](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/SpatialDataServiceType.es.xml) and in [IR MD](./README.md#ref_IR_MD) Part D.3.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.1.2.3, Req 3.5
* [Spatial Data Service Type](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/SpatialDataServiceType.es.xml)
* [IR MD](./README.md#ref_IR_MD) Part D.3.

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="serviceType"></a> Service Type  | gmd:identificationInfo[1]/srv:SV_ServiceIdentification/srv:serviceType/gco:LocalName
