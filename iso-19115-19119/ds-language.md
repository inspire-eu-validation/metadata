# Dataset language

**Purpose**: If the type of the resource is dataset or series, a resource language must be given.

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a [gmd:LanguageCode](#langcode) object is given and contains a codeList and codeListValue attribute.

It is then checked if the codeListValue attribute contains a valid 3-letter language code (one of the values of enumeration type `languageISO6392B` in http://inspire.ec.europa.eu/schemas/common/1.0/common.xsd).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.2.7, Req 8 & 9
* ISO 639-2

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="langcode"></a> LanguageCode  | gmd:identificationInfo[1]/*/gmd:language/gmd:LanguageCode
