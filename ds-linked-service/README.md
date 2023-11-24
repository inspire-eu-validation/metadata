# Conformance Class 8: INSPIRE data sets and data set series linked service metadata

This Abstract Test Suite (ATS) describes a set of additional requirements for INSPIRE metadata, which were defined in the [Data Service Linking Simplification: Good Practice guidelines](#ref_GP_DSLS).

*Note*: It is Ready for the review stage, none of the tests have an official INSPIRE MIG approval. This new conformance class will be added to the MD TG if the [related change proposal](https://github.com/INSPIRE-MIF/technical-guidelines/issues/108) is endorsed.

## Standardization target type

ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| INSPIRE Metadata | [Conformance Class 1](../datasets-and-series/README.md) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| INSPIRE Metadata | [Common Requirements](../common/README.md) | n/a |
 
## External document references


| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| GP DSLS <a name="ref_GP_DSLS"></a> | [Data Service Linking Simplification: Good Practice guidelines](https://github.com/INSPIRE-MIF/gp-data-service-linking-simplification/blob/main/good-practice/data-service-linking-simplification-spec.md)
| ID MON <a name="ref_ID_MON"></a> | [Commission Implementing Decision of 19.8.2019 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards monitoring and reporting](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32019D1372&from=EN)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)
| ISO 639-2/B  <a name="ref_ISO_639_2"></a> | [ISO 639-2/B: Codes for the Representation of Names of Languages](http://www.loc.gov/standards/iso639-2/)


## TG Requirement coverage

Based on requirement numbering in [GP DSLS](#ref_GP_DSLS).

| Req#   | Description                          | Covered by test(s)                 |
| ------ | ------------------------------------ | ---------------------------------- |
| view-linkage      | View Service linkage | [Data set Metadata Resource Locator](./ds-md-resource-locator.md) |
| download-linkage  | Download Service linkage | [Data set Metadata Resource Locator](./ds-md-resource-locator.md) |


## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Data set Metadata Resource Locator](./ds-md-resource-locator.md) | Ready for review  |

## Open issues


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
