# Resource language

**Purpose**: If the type of the resource is dataset or series, a resource language must be given.

**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if a [LanguageCode](#langcode) object is given and contains a codeList and 
codeListValue attribute.

It is then checked if the codeListValue attribute contains a valid 3-letter language code (one of the values of 
enumeration type [ISO 6392B](http://inspire.ec.europa.eu/schemas/common/1.0/common.xsd).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD), 3.1.2.4, Req 1.6
* [ISO 639-2](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_ISO_639_2)

**Test type**: Automated

**Notes**

The ETS does not check if a gmd:LanguageCode contains a codeList attribute, since that is required by the schema.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="langcode"></a> LanguageCode  | ./gmd:language/gmd:LanguageCode/@codeListValue
