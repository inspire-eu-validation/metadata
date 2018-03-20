# Invocation Metadata for Harmonised Spatial Data Services

**Purpose**: The invocation metadata must be specified for the Spatial Data Harmonized Services
**Prerequisites**
* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

* It is checked if the metadata are encoded invocation from element [SV_OperationMetadata](#operation_metadata) considering that:

* - The child element [Connect Point](#connectPoint) must be the same as the element that describes the [access-point](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/access-point).
* - The contents of these element shall be given according to [ISO 19119, Section C.2] when the metadata record contains at least one of these elements.


**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#ref_TG_MD), 4.5.1.1 , Req 7.1
* [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/README#ref_ISO_19119)

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="operation_metadata">Operation Metadata</a> | gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]
<a name="connectPoint">Connect Point</a> | gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata/srv:connectPoint 
 