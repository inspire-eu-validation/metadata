# XML Schema

**Purpose**: Performs a schema validation of the document.

**Prerequisites**

**Test method**

* Check that the document validates against at least one of the following XML schemas:

    * [CSW2 AP ISO](http://inspire.ec.europa.eu/draft-schemas/inspire-md-schemas-temp/apiso-inspire/apiso-inspire.xsd) XML Schema

    * [ISO 19139](http://www.isotc211.org/2005/gmd/gmd.xsd) XML Schema as available in the ISO repository

    * [ISO 19139](http://schemas.opengis.net/iso/19139/20070417/gmd/gmd.xsd) XML Schema for GML version 3.2.1 or [ISO 19139](http://schemas.opengis.net/iso/19139/20060504/gmd/gmd.xsd) XML Schema for GML version 3.2.0 as available in the OGC schema repository.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.1 , Req c.1
* [ISO 19119](./README.md#ref_ISO_19119)


**Test type**: Automated

**Notes**

The choice of which XML Schemas to use for encoding the metadata records depends on the existing technical solutions available, as well as on the GML version wished to be used:

* If the delivery of the metadata records is done via a Discovery Service supporting the [CSW2 AP ISO] standard, using the XML Schema of this specification is a natural choice. 

* If using GML version 3.2.1 in the metadata, then it is recommended to use either the official [ISO 19139] XML Schema available at the ISO schema repository, or the nearly identical version (2007-04-07) available in the OGC schema repository.

All three of these XML Schemas declare the same [namespace](http://www.isotc211.org/2005/gmd).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="schemaLocation">Schema Location</a>   | /*/@xsi:schemaLocation
