# Spatial Resolution

**Purpose**: Test that the spatial resolution is defined using either an scale or a distance resolution.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* For every [Spatial Resolution](#spatialResolution),

    * Check that [Equivalent Scale](#equivalentScale) or [Distance](#distance) element exists.

* Check that all the [Spatial Resolution](#spatialResolution) children are either [Equivalent Scale](#equivalentScale) or [Distance](#distance) but not both.

* If any of the checks fails, the test fails.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 3.1.2.3, Req 1.5

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:spatialResolution)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="spatialResolution"></a> Spatial Resolution | /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:spatialResolution
<a name="equivalentScale"></a> Equivalent Scale | gmd:MD_Resolution/gmd:equivalentScale
<a name="distance"></a> Distance | gmd:MD_Resolution/gmd:distance
