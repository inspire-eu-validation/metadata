# Data Encoding

**Purpose**: Evaluate encoding and the storage or transmission format for data sets and series.

**Prerequisites**

**Test method**

* Check that at least one [Distribution Format](#distributionFormat) element exists.

* For every [Distribution Format](#distributionFormat),

    * Check that [Name](#name1) element exist and its content is a not-empty free text.

    * Check that [Version](#version) element exists. Then,

        * If content is not empty, check that its content is a non-empty free text.

        * Else, check that it has an attribute gco:nilReason="unknown" or "inapplicable".

* If any of the checks fails, the test fails.

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.3.1, Req 2.6

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:distributionInfo/gmd:distributionFormat)
-----------------------------------------------| ------------------------------------------------------------------
<a name="distributionFormat"></a> Distribution Format | /gmd:MD_Metadata/gmd:distributionInfo/gmd:distributionFormat
<a name="name1"></a> Name | gmd:MD_Format/gmd:name
<a name="version"></a> Version | gmd:MD_Format/gmd:version
