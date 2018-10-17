# Resource Locator

**Purpose**: Test if there is a resource or the url that points to a resource that provides  additional information about the set data set or data set series.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* For every [URL Resource](#urlResource),

    * Check that a correct URL is provided.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.3.1, Req 1.8

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

A Resource Locator encoded using the gmd:CI_OnlineResource element may also include gmd:name, gmd:description, and gmd:function properties.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="urlResource"></a> URL Resource | gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL
