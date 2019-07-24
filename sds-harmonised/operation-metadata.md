# Operation Metadata

**Purpose**: Test that operation metadata is encoded correctly.

**Prerequisites**

**Test method**

* Check that at least one [Operation Metadata](#operationMetadata) element exists.

* For every [Operation Metadata](#operationMetadata) element,

    * Check that exactly one [Operation Name](#operationName) element exists and its content is a non-empty free text.

    * Check that at least one [Distributed Computing Platform List](#dcpList) element exists.

    * Check that at least one [URL](#url) element exists.

* If any of the checks fails the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.5.1.1 , Req 7.2

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/srv:SV_ServiceIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="operationMetadata"></a>Operation Metadata | srv:containsOperations/srv:SV_OperationMetadata
<a name="operationName"></a>Operation Name | srv:containsOperations/srv:SV_OperationMetadata/srv:operationName
<a name="dcpList"></a>Distributed Computing Platform List | srv:containsOperations/srv:SV_OperationMetadata/srv:DCP/srv:DCPList
<a name="url"></a>URL | srv:containsOperations/srv:SV_OperationMetadata/srv:connectPoint/gmd:CI_OnlineResource/gmd:URL
