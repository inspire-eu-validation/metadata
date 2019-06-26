# Dataset language

**Purpose**: If the type of the resource is dataset or series, a resource language must be given.

**Prerequisites**

* [Hierarchy](./hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a [gmd:LanguageCode](#langcode) object is given and contains a codeList and codeListValue attribute.

It is then checked if the codeListValue attribute contains a valid 3-letter language code (one of the values of enumeration type `languageISO6392B` in http://inspire.ec.europa.eu/schemas/common/1.0/common.xsd).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.7, Req 8 & 9
* ISO 639-2

**Test type**: Automated

**Notes**

The ETS does not check if a gmd:LanguageCode contains a codeList attribute, since that is required by the schema.

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available dataset (series) metadata records.  

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="langcode"></a> LanguageCode  | gmd:identificationInfo[1]/\*/gmd:language/gmd:LanguageCode
