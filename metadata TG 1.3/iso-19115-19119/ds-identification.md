# Dataset identification

**Purpose**: Unique resource identifier. If the type of the resource was dataset or series, a unique identifier identifying the resource must be given.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a unique [identifier](#identifier) is given and if it is of type MD_Identifier or RS_Identifier.

The contained code element may not be empty.

In case of RS_identifier, the codespace element should not be empty.

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD), 2.2.5, Req 5 & 6
* [ISO 19115](./README#ref_ISO_19115), B.2.7.3

**Test type**: Automated

**Notes**

* In case of MD_identifier, discussion is ongoing on how to match this element against a namespace-identifier in a capabilities document/service metadata.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="identifier"></a> identifier   | gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:identifier
