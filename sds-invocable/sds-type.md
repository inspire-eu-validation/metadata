# Srv type

**Purpose**: If the type of the resource was service, exactly one name describing the type of service must be given.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

If the type of the resource is service, exactly one name describing the type of service must be given.
First, a check is performed to establish whether the [serviceType](#serviceType) element occurs exactly once in the document. The test then checks if the element [serviceType](#serviceType) contains text that equals one of
the types given in ([Spatial Data Service Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/ns/README#ref_Spatial Data Service Type) Chap. 1.3.1.)

The value for the element shall be "other".

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_TG_MD) 4.3.1.1, Req 5.1
* [Spatial Data Service Type](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/SpatialDataServiceType.es.xml)

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
serviceType <a name="serviceType"></a>   | ./gmd:identificationInfo[1]/\*/srv:serviceType/gco:LocalName
