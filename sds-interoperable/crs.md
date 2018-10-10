# Coordinates Reference Systems

**Purpose**: Test that the coordinate reference system identifiers are provided.

**Prerequisites**

**Test method**

* Check that at least one [RS Identifier](#rsIdentifier) element exists.

    * For every [RS Identifier](#rsIdentifier),

        * Check that [Code](#code) element exist and its content is a not-empty free text.

        * If [Code Space](#codeSpace) exists, check that its content is a non-empty free text.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD) 4.4.1.1, Req 6.1

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:referenceSystemInfo/gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier)
-----------------------------------------------| ------------------------------------------------------------------
<a name="rsIdentifier"></a> RS Identifier | /gmd:MD_Metadata/gmd:referenceSystemInfo/gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier
<a name="code"></a> Code | gmd:code
<a name="codeSpace"></a> Code Space | gmd:codeSpace