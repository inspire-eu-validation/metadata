# Temporal Reference Systems

**Purpose**: Test if the temporal reference system(s) is provided correctly.

**Prerequisites**

**Test method**

* Check that at least one [RS Identifier](#rsIdentifier) element exists.

    * For every [RS Identifier](#rsIdentifier),

        * Check that [Code](#code) element exist and its content is a not-empty free text.

        * If [Code Space](#codeSpace) exists, check that its content is a non-empty free text.

* If any of the checks fails, the test fails.

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.1.2, Req 2.3

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

The gmd:codeSpace child element shall be used if the [code](#codeChild) alone does not uniquely identify the referred coordinate reference system.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:referenceSystemInfo)
-----------------------------------------------| ------------------------------------------------------------------
<a name="referenceSystemIdentifier"></a> referenceSystemIdentifier  | gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier
<a name="code"></a> Code | gmd:code
<a name="codeSpace"></a> Code Space | gmd:codeSpace
