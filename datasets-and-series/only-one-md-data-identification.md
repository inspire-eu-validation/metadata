# Only One Data Identification

**Purpose**:
Test that the identification info section of the metadata for data sets and data set series is provided correctly.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* Check that the first [Identification Info](#identificationInfo) contains only one [Data Identification](#dataIdentification)

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD),3.1.2, Req 1.2
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

Although more than one IdentificationInfo can be given within the MD_Metadata element, only the first instance is used for the identification of the INSPIRE resource.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to root)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="identificationInfo"></a> Identification Info   | /gmd:MD_Metadata/gmd:identificationInfo
<a name="dataIdentification"></a> Data Identification   | /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification
