# Coupled resource

**Purpose**: If the resource is a spatial data service, this metadata element refers to the
target spatial data set(s) of the service. It is implemented by reference, i.e. through a URL that
points to the metadata record of the data on which the service operates.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The operatesOn element in the [SV_ServiceIdentification](#SV_ServiceIdentification) element should be a HTTP URI that when retrieved using HTTP GET should return the metadata document describing the dataset exposed by this service (i.e. the resource must be a metadata record with a [hierarchyLevel](#hierarchyLevel) 'dataset' or 'series').

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.2.6, req 7

**Test type**: Automated

**Notes**

How to identify that the service operates on a dataset? Only services with service types http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view or http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download for now?

*todo*: to validate this is the proper identification, the identification used in capabilities might be required

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="coupling"></a> SV_ServiceIdentification   | ./gmd:identificationInfo/srv:SV_ServiceIdentification/srv:operatesOn
