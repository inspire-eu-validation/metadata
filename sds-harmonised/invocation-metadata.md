# Invocation Metadata

**Purpose**: Test that the invocation metadata for the Spatial Data Harmonized Services is provided.

**Prerequisites**

**Test method**

* If at least one [Operation Metadata](#operationMetadata) element exists,

    * For every [Operation Metadata](#operationMetadata) element,

        * The content of the element is in accordance with [ISO 19119, Section C.2](../README.md#ref_ISO_19119)

* Else

    * Check that [Connect Point](#connectPoint) exists and it is the same as the one described in [Access Point](../sds-invocable/access-point.md) requirement from conformance class 5.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.5.1.1 , Req 7.1
* [ISO 19119](../README.md#ref_ISO_19119)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/srv:SV_ServiceIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="operationMetadata">Operation Metadata</a> | srv:containsOperations/srv:SV_OperationMetadata
<a name="connectPoint">Connect Point</a> | srv:containsOperations/srv:SV_OperationMetadata/srv:connectPoint
