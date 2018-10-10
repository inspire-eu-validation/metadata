# Operation Metadata Parameters

**Purpose**: Test that operation metadata parameters are provided correctly.

**Prerequisites**

**Test method**

* For every [Operation Metadata](#operationMetadata),

    * For every [Parameter](#paramter),

        * Check that exactly one [Parameter Name](#parameterName) element exists and its content is a non-empty free text.

        * Check that exactly one [Attribute Type](#attributeType) element exists.

        * Check that exactly one [Optionality](#optionality) element exists and its content is a non-empty free text.

        * Check that exactly one [Repeatability](#repeatability) element exists and its value is "true" or "false".

        * Check that exactly one [Type Name](#typeName) element exists.

* If any of the checks fails the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.5.1.1 , Req 7.3

**Test type**: Automated

**Notes**

The test method is not clear on how a specific code list is referenced in a gmd:thesaurusName.


##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/srv:SV_ServiceIdentification)
-----------------------------------------------| -------------------------------------------------------------------------

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="operationMetadata"></a>Operation Metadata | srv:containsOperations/srv:SV_OperationMetadata
<a name="parameter"></a>Parameter | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter
<a name="parameterName"></a>Parameter Name | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter/srv:name/gco:aName/
<a name="attributeType"></a>Attribute Type | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter/srv:name/gco:attributeType
<a name="optionality"></a>Optionality | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter/srv:optionality
<a name="repeatability"></a>Repeatability | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter/srv:repeatability/gco:Booleans
<a name="typeName"></a>Type Name | srv:containsOperations/srv:SV_OperationMetadata/srv:parameters/srv:SV_Parameter/srv:valueType/gco:TypeName/gco:Name
