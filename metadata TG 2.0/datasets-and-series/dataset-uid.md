# Dataset UID

**Purpose**: Test that every dataset or dataset series has an Unique Resource Identifier.

**Prerequisites**

**Test method**

* For every [Data Identification](#dataIdentification):

    * Check that a unique [Identifier](#identifier) element exists. Then,

        * Check that its child is a [MD_Identifier](#mdIdentifier) or a [RS_Identifier](#rsIdentifier) element.

            * Check that [Code](#code) exists and its child is a non-empty free text element.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.2.1, Req 1.3
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

The [ISO 19139] xml schemas allow the use of either the MD_Identifier type or its sub-type RS_Identifier, which, in addition to the mandatory code property, also contains an optional codeSpace property.

It is strongly recommended to use the MD_Identifier instead of the the RS_Identifier type and to encode the complete URI in the code element.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="dataIdentification"></a> Data Identification | /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification
<a name="identifier"></a> Identifier | gmd:citation/gmd:CI_Citation/gmd:identifier
<a name="mdIdentifier"></a> MD_Identifier | gmd:citation/gmd:CI_Citation/gmd:identifier/gmd:MD_Identifier
<a name="rsIdentifier"></a> RS_Identifier | gmd:citation/gmd:CI_Citation/gmd:identifier/gmd:RS_Identifier
<a name="code"></a> Code | gmd:citation/gmd:CI_Citation/gmd:identifier/*/gmd:code