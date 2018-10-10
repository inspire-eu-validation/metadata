# Resource Title

**Purpose**: Test that a non-empty title of the described data is provided.

**Prerequisites**

**Test method**

* Check that exactly one [Title](#title) element exists. If it does:

    * Check that its content is a non-empty free text element.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.1 , Req c.8

**Test type**: Automated

**Notes**

The multiplicity of [Title](#title) is one.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="title"></a> Title  | gmd:citation/gmd:CI_Citation/gmd:title