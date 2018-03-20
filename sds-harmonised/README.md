# Metadata for Harmonised Spatial Data Services 
Abstract Test Suite for Conformance Class 7 of the [INSPIRE Metadata](http://inspire.ec.europa.eu/id/ats/metadata/2.0) Technical Guidance 
based on ISO/TS 19139:2007.


*Note*: This ATS is in ready for review stage, none of the tests have an official INSPIRE MIG approval.
## Standardization target type

 ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ISO 19139:2007](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common) | Common Requirements | n/a |
| [ISO 19139:2007](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable) | Conformance Class 6 | n/a |

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
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007, version 2.0](https://inspire.ec.europa.eu/sites/default/files/documents/metadata/inspire-tg-metadata-iso19139-2.0.1.pdf)
| ISO 19118 <a name="ref_ISO_19118"></a> | [ISO 19118:2011 Geographic information – Encoding](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=44212)
| SDS ALT <a name="ref_SDS_alt"></a> | Alternative approaches to implement Metadata for Spatial data services (not published?)

## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 7.1      | Invocation Metadata              | [invocation-metadata](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/invocation-metadata) | |
| 7.2      | Operation Metadata               | [operation-metadata](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/operation-metadata) | |
| 7.3      | Operation Metadata Parameters               | [operation-metadata-parameters](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/operation-metadata-parameters) | |


## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [sds-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/invocation-metadata) |  Ready for review  |
| [access-point](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/operation-metadata) |  Ready for review  |
| [conformity](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised/operation-metadata-parameters) |  Ready for review  |

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
