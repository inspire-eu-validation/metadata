# Data Quality Info Section 

**Purpose**: Test that one citation of the product specification or user requirement against which data is being evaluated is provided.

**Prerequisites**

**Test method**

* Check that exactly one [Data Quality](#dataQuality) element exists.

    * Check that [Scope Code](#scopeCode) exists and the attribute codeListValue is "dataset" or "series".

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD), 3.1.4.1, Req 1.9

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

According to ISO/TS 19139:2007, it is also recommended that the [Scope Code](#scopeCode) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="dataQuality"></a> Data Quality | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality
<a name="scopeCode"></a> Scope Code | gmd:scope/gmd:DQ_Scope/gmd:level/gmd:MD_ScopeCode
