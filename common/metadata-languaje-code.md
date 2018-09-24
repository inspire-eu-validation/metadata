# Metadata Languaje


**Purpose**: A resource language must be given limited to the official languages of the Community expressed in conformity with ISO 639-2.

**Prerequisites**

**Test method**

* The test first checks if a [gmd:LanguageCode](#langcode) object is given and contains a codeList and 
codeListValue attribute.

* It is then checked if the codeListValue attribute contains a valid 3-letter language code (one of the values of 
enumeration type [languageISO6392B](http://inspire.ec.europa.eu/schemas/common/1.0/common.xsd).


**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.2.2 , Req c.5
* [ISO 639-2/B](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_639_2)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="langcode"></a> LanguageCode  | gmd:MD_Metadata/gmd:language/gmd:LanguageCode/@codeListValue
