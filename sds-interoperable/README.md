# Metadata for Interoperable Spatial Data Services

Abstract Test Suite for Conformance Class 6 of the [INSPIRE Metadata](http://inspire.ec.europa.eu/id/ats/metadata/2.0) Technical Guidance 
based on ISO/TS 19139:2007.

*Note*: This ATS is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.
## Standardization target type

 ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ISO 19139:2007](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common) | Common Requirements | n/a |
| [ISO 19139:2007](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable) | Conformance Class 5 | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007](#ref_TG_MD) |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| INT SDS <a name="ref_INT_SDS"></a> | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| INT SDS AMD <a name="ref_INT_SDS_AMD"></a> | [Commission Regulation (EU) No 1312/2014 of 10 December 2014 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1312&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [Commission Regulation (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata (Text with EEA relevance)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32008R1205&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007, version 2.0](https://inspire.ec.europa.eu/sites/default/files/documents/metadata/inspire-tg-metadata-iso19139-2.0.1.pdf)
| SDS ALT <a name="ref_SDS_alt"></a> | Alternative approaches to implement Metadata for Spatial data services (not published?)
| DS CRS <a name="ref_DS_CRS"></a> | [D2.8.I.1 Data Specification on Coordinate Reference Systems – Technical Guidelines](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_RS_v3.2.pdf)

## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 6.1      | Coordinate Reference System Identifier              | [crs](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/crs) | |
| 6.2      | CRS http URIs               | [crs-http-uris](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/crs-http-uris) | |
| 6.3      | Conditions Applying to Access and Use               | [conditions-applying-to-access-and-use](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use) | |
| 6.4      | Responsible Party              | [responsible-party](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/responsible-party) | |
| 6.5      | Quality of Service              | [quality-of-service](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/quality-of-service) | |


## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [sds-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/crs) |  Ready for review  |
| [access-point](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/crs-http-uris) |  Ready for review  |
| [conformity](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use) |  Ready for review  |
| [sds-category](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/responsible-party) |  Ready for review  |
| [conformity-to-technical-specifications](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/quality-of-service) |  Ready for review  |


## Open issues


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gmd | http://www.isotc211.org/2005/gmd
gml | http://www.opengis.net/gml/3.2
srv | http://www.isotc211.org/2005/srv
inspire\_sds\_gmd | [missing]
xlink          | http://www.w3.org/1999/xlink
