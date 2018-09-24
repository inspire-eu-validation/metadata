# Metadata Structure and Encoding: Root Element

**Purpose**: Performs a schema validation of the document.

**Prerequisites**

**Test method**

The document shall pass schema validation without errors using the following XML schema definitions: 
* [CSW2 AP ISO](http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas) XML Schema
* [ISO 19139](http://www.isotc211.org/2005/gmd/gmd.xsd) XML Schema as available in the ISO repository , or 
* [ISO 19139](http://schemas.opengis.net/iso/19139/20070417/gmd/gmd.xsd) XML Schema as available in the OGC schema repository15. 
* All three of these XML Schemas declare the same [namespace](http://www.isotc211.org/2005/gmd).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.1 , Req c.1
* [ISO 19119](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19119)


**Test type**: Automated

**Notes**

The choice of which XML Schemas to use for encoding the metadata records depends on the existing technical solutions available, as well as on the GML version wished to be used:

* If the delivery of the metadata records is done via a Discovery Service supporting the [CSW2 AP ISO] standard, using the XML Schema of this specification is a natural choice. 
* If using GML version 3.2.1 in the metadata, then it is recommended to use either the official [ISO 19139] XML Schema available at the ISO schema repository, or the nearly identical version “2007-04-07” available in the OGC schema repository.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression ()
-----------------------------------------------| -------------------------------------------------------------------------
<a name="schemaLocation">Schema Location</a>   | /*/@xsi:schemaLocation
