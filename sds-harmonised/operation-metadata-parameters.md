# Operation Metadata Request Parameters for Harmonised Spatial Data Services

**Purpose**: For all the required and optional request parameters of the operations, its secondary elements will be checked.
**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

* The required and optional request [parameter](#parameter) of the operation metadata have to be defined from a series of child elements:

*- [Parameter Name](#parameter_name): name of the parameter as used by the service. The multiplicity of this element is 1.
* The child element aName is a Non-empty Free Text Element.
* The child element attributeType shall contain the record or the type part of the attribute name.

*- [Optionality](#optionality): indicates whether the attribute is mandatory or optional. The multiplicity of this element is 1 and its content is free text type, not empty.

*- [Repeatability](#repeatability): from true/false values it is indicated if the attribute can be repeated.

*- [Type Name](#type_name): indicate the data type of the attribute.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#ref_TG_MD), 4.5.1.1 , Req 7.3

**Test type**: Automated

**Notes**

The test method is not clear on how a specific code list is referenced in a gmd:thesaurusName.


##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
<a name="parameter">Parameter</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter
<a name="parameter_name">Parameter Name</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter/srv:name[1]
and gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter/srv:name[1]/gco:aName/text() 
<a name="optionality">Optionality</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter/srv:optionality[1]/text()
<a name="repeatability ">Repeatability</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter/srv:repeatability/true()
<a name="type_name ">Type Name</a> | ./gmd:identificationInfo/\*/srv:containsOperations/srv:SV_OperationMetadata[1]/\*/srv:SV_Parameter/\*/gco:TypeName/gco:Name