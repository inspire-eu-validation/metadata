# Only One Data Quality Info Element

**Purpose**: 

Test that a dataQuality element is given, and that the scope is encoded using an scopeCode element and described in a scopeDescription element.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* Check if exactly one [dataQuality](#dataquality) is given scoped to the entire described service.

* Check if a [scopeCode](#scopeCode) element is provided referring the value "service". 

  * Check if MD_ScopeCode element has a "codeList" attribute with value "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_ScopeCode" and a "codeListValue" attribute with value "service".

* Check if the a [scopeDescription](#scopeDescription) element is provided with an non-empty free text containing the term "service" in the language of the metadata.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 4.1.4.1, Req 3.8

**Test type**: Automated

**Notes**

The multiplicity of this elements is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="dataquality"></a> dataQuality    | gmd:dataQualityInfo/gmd:DQ_DataQuality
<a name="scopeCode"></a> scopeCode    | gmd:dataQualityInfo[1]/gmd:DQ_DataQuality/gmd:scope/gmd:DQ_Scope/gmd:level/gmd:MD_ScopeCode
<a name="scopeDescription"></a> scopeDescription    | gmd:dataQualityInfo[1]/gmd:DQ_DataQuality/gmd:scope/gmd:DQ_Scope/gmd:levelDescription/gmd:MD_ScopeDescription/gmd:other/gco:CharacterString

