# Metadata Structure and Encoding: Root Element

**Purpose**: Performs a schema validation of the document.

**Prerequisites**

**Test method**

* The document shall pass schema validation without errors using the following XML schema definitions: 
* -	[CSW2 AP ISO] XML Schema , 
* -	[ISO 19139] XML Schema as available in the ISO repository , or 
* -	[ISO 19139] XML Schema as available in the OGC schema repository15. 
 
* All three of these XML Schemas declare the same [namespace](http://www.isotc211.org/2005/gmd).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.1 , Req c.1
* [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19119)

http://www.loc.gov/standards/iso639-2/

**Test type**: Automated

**Notes**

This schema is an XML implementation of the [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/README#ref_ISO_19119) service metadata.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression ()
-----------------------------------------------| -------------------------------------------------------------------------
<a name="schemaLocation">Schema Location</a>   | /*/@xsi:schemaLocation
