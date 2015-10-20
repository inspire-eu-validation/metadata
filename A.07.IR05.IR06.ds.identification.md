#A.07.IR05.IR06.ds.identification

**Purpose**: Unique resource identifier. If the type of the resource was dataset or series, a unique identifier identifying the resource must be given.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if a unique [identifier](#identifier) is given and if it is of type MD_Identifier or RS_Identifier.
The contained code element may not be empty.

* In case of RS_identifier, the codespace element should not be empty.
* In case of MD_identifier, discussion is ongoing on how to match this element against a namespace-identifier in a capabilities document/service metadata.

If the type of the resource is not dataset or series, this test is omitted.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.5, Req 5 & 6
* [ISO 19115](README.md#ref_ISO_19115), B.2.7.3

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="identifier"></a> identifier   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:identifier
