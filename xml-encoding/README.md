# Conformance class: XML encoding of ISO 19115/19119 metadata (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Metadata Technical Guidance](http://inspire.ec.europa.eu/id/ats/metadata/1.3).

## Standardization target type

All requirements of a conformance class apply to a single resource type, the standardization target type:

* XML document (MD_Metadata)

## Parameters

A Conformance class may be parameterized, i.e. the class’s tests depend on some parameter that must be defined before the tests can be executed.
 
| Parameter | Values | Description |
| --------- | ------ | ----------- |
| `encoding` | `CSW ISO AP 1.0` `ISO/TS 19139` | The XML schema documents used by the metadata record | 

## Dependencies

### Direct dependencies

none

### Indirect dependencies

none
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| ISO/TS 19139 <a name="ref_ISO_TS_19139"></a> | [ISO/TS 19139:2005 Geographic information -- Metadata -- XML schema implementation](http://www.iso.org/iso/catalogue_detail.htm?csnumber=32557)
| CSW_ISO_AP <a name="ref_CSW_ISO_AP"></a> | [OGC Catalogue Services Specification 2.0.2 - ISO Metadata Application Profile for CSW 2.0, version 1.0.0 (OGC 07-045)](http://portal.opengeospatial.org/files/?artifact_id=21460)

## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Schema validation](http://inspire.ec.europa.eu/id/ats/metadata/1.3/xml-encoding/schema-validation)  	                          | Ready for review  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
