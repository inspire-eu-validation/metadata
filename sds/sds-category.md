# SDS Category Keywords

**Purpose**: Test that a Spatial Data Service category or subcategory is given.

**Prerequisites**

**Test method**

* Check if at least one [keyword](#keyword) has a child CharacterString or Anchor which xlink:href attribute  is one of the language-natural keyword values as defined in Classification of Spatial Data Services Part D 4 [IR_MD](./README.md#ref_IR_MD).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.1.2.2, Req 3.4
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The multiplicity of the [keyword](#keyword) element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | gmd:identificationInfo[1]/srv:SV_ServiceIdentification/gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword
