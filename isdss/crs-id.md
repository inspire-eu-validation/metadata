# Coordinates Reference Systems ID

**Purpose**: Test that the default coordinate reference systems uses a correct identifier.

**Prerequisites**

* [referenceSystemIdentifier](./crs.md)

**Test method**

* If the coordinate reference system is listed in the Default Coordinate Reference System Identifiers table in [Annex D.4 - TG MD](./README.md#ref_TG_MD),

    * Check that the value of the HTTP URI Identifier column is used as the value of [Code](#code) element.

    * Check that [Code Space](#codeSpace) does not exists.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 3.2.1.1, Req 2.2

**Test type**: Automated

**Notes**

The gmd:codeSpace element shall not be used in this case.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:referenceSystemInfo)
-----------------------------------------------| ------------------------------------------------------------------
<a name="code"></a> Code  | gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier/gmd:code
<a name="codeSpace"></a> Code Space | gmd:codeSpace