# Conditions Applying to Access and Use 

**Purpose**: Test that the technical restrictions of access and use of an interoperable spatial data service are specified in the metadata.

**Prerequisites**

**Test method**

* Check that exactly one [Legal Constraints](#legalConstraints) element exists.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 4.4.2.1, Req 6.3
* [ISO 19115](./README.md#ref_ISO_19115) table B.8 MD_RestrictionCode

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

The specification for this requirement is defined in [Conditions for access and use](../common/conditions-for-access-and-use.md) requirement from [Common Requirements](../common/README.md).

This element shall not be the same used for describing limitations on public access.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/*/gmd:resourceConstraints)
-----------------------------------------------| ------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints |  gmd:MD_LegalConstraints
