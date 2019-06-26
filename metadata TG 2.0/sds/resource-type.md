# Resource Type

**Purpose**: Test that a resource type is provided as service.

**Prerequisites**

**Test method**

* Check if a resource type is provided exactly once in the [hierarchyLevel](#hierarchyLevel) element and the value is declared as 'service'.

  * Check if [hierarchyLevel](#hierarchyLevel) element includes an attribute "codeList" with the value 
  "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_ScopeCode" and an attribute "codeListValue" with the value "service".

* Check if the name of the hierarchy level is provided exactly once using the [hierarchyLevelName](#hierarchyLevelName) element and its value is a non-empty free text element containing the term "service" in the language of the metadata.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.1.1.1, Req 3.1
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The multiplicity of [hierarchyLevel](#hierarchyLevel) and [hierarchyLevelName](#hierarchyLevelName) elements is one.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/
<a name="hierarchyLevelName"></a> hierarchyLevelName | gmd:hierarchyLevelName/gco:CharacterString