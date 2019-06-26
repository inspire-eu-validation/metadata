# Resource Title

**Purpose**: Test that a non-empty title of the described data is provided.

**Prerequisites**

**Test method**

* If it is a Datatasets or Series metadata

    * Check that exactly one [Title for Datasets and Series](#titleData) element exists. If it does:

        * Check that its content is a non-empty free text element.

* Else if it is a Service metadata

    * Check that exactly one [Title for Services](#titleServ) element exists. If it does:

        * Check that its content is a non-empty free text element.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.1 , Req c.8

**Test type**: Automated

**Notes**

The multiplicity of [Title](#title) is one.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="titleData"></a> Title for Datasets and Series  | gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:title
<a name="titleServ"></a> Title for Services  | srv:SV_ServiceIdentification/gmd:citation/gmd:CI_Citation/gmd:title