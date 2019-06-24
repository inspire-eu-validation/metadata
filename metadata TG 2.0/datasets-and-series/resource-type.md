# Resource Type 'dataset' or 'series'

**Purpose**: Test that a resource type is provided as a dataset or series.

**Prerequisites**

**Test method**

* Check that [Hierarchy Level](#hierarchyLevel) exists and it has a child element [Scope Code](#scopeCode).

    * Check that [Scope Code](#scopeCode) has an attribute codeList with value "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_ScopeCode" and an attribute codeListValue with value "dataset" or "series".

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.1.1, Req 1.1
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | /gmd:MD_Metadata/gmd:hierarchyLevel
<a name="scopeCode"></a> Scope Code | /gmd:MD_Metadata/gmd:hierarchyLevel/gmd:MD_ScopeCode