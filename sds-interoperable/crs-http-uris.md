# Coordinates Reference Systems HTTP URIs

**Purpose**: Test that the default coordinate reference systems use a correct identifier.

**Prerequisites**

* [ReferenceSystemIdentifier](./crs.md)

**Test method**

* If the coordinate reference system is listed in the Default Coordinate Reference System Identifiers table in [Annex D.4 - TG MD](./README.md#ref_TG_MD) or if it is a new approved coordinate reference system (all coordinate reference systems approved for use in INSPIRE are available in the following table: https://github.com/INSPIRE-MIF/helpdesk/blob/main/crs.md),

    * Check that the value of the HTTP URI Identifier column is used as the value of [Code](#code) element.

    * Check that [Code Space](#codeSpace) does not exists.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 4.4.1.1, Req 6.2
* [TG MD](./README.md#ref_TG_MD) Annex D.4 "Default Coordinate Reference Systems"

**Test type**: Automated

**Notes**
The gmd:codeSpace element shall not be used in this case.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:referenceSystemInfo)
-----------------------------------------------| ------------------------------------------------------------------
<a name="code"></a> Code  | gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier/gmd:code
<a name="codeSpace"></a> Code Space | gmd:codeSpace
