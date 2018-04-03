# Operation Metadata for Harmonised Spatial Data Services

**Purpose**: Invocation metadata must be encoded from a series of child elements of Operation Metadata.
**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)
* There must be at least one of the [SV_OperationMetadata](#operation_metadata) elements.

**Test method**
* It is checked if the invocation metadata is coded by a set of secondary elements:

*- [operation_name](#operation_metadata): unique identifier for the interface described by the element. The multiplicity of this element is 1 and its content is free text type, not empty.

*- [Distributed Computing Platform](#dcpList): a reference to the distributed computing platform in which the operation was implemented. The multiplicity of this element is one or more.

*- [Parameter](#parameter): description of a single request parameter to be used in invoking the operation.
* The content of this element is coded according to [operation-metadata-parameters](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/operation-metadata-parameters) requirement, and its multiplicity is 0 or more.

*- [Point URL](#point_url): the end point to access the service and execute the operation. The multiplicity of the element is one or more.


**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#ref_TG_MD), 4.5.1.1 , Req 7.2

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="operation_metadata">Operation Metadata</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]
<a name="operation_name">Operation Name</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/srv:operationName[1]/text()
<a name="dcpList">DCP</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/srv:operationName[1]/\*/srv:DCPList/text()
<a name="parameter ">Parameter</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter
<a name="point_url ">Point URL</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata/srv:connectPoint/\*/gmd:URL[1]
