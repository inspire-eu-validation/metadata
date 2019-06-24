# Spatial Representation Type

**Purpose**: Test the type of spatial representation of the data.

**Prerequisites**

**Test method**

* Check that [Spatial Representation Type Code](#spatialRepresentationTypeCode) element exists. If it does,

    * Check that it has an attribute codeList with value "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_SpatialRepresentationTypeCode" and an attribute codeListValue with value "vector", "grid", "tin" or "textTable".

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.2.1, Req 2.4

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:spatialRepresentationType)
-----------------------------------------------| ------------------------------------------------------------------
<a name="spatialRepresentationTypeCode"></a> Spatial Representation Type Code  | gmd:MD_SpatialRepresentationTypeCode
