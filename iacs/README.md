# Conformance Class 2c: INSPIRE data sets and data set series metadata for IACS

This Abstract Test Suite (ATS) describes a set of additional requirements for INSPIRE metadata, which are not currently included in the [Technical Guidance](#ref_TG_IACS).

*Note*: It is Ready for review stage, none of the tests have an official INSPIRE MIG approval.

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

 *There is not indirect dependencies for this set of requirements.*
 
## External document references


| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](https://eur-lex.europa.eu/eli/dir/2007/2)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](https://eur-lex.europa.eu/eli/reg/2008/1205)
| TG IACS <a name="ref_TG_IACS"></a> | [Technical guidelines on IACS spatial data sharing. Part 1 - Data discovery](https://publications.jrc.ec.europa.eu/repository/handle/JRC121450)
| ID MON <a name="ref_ID_MON"></a> | [Commission Implementing Decision (EU) 2019/1372 of 19 August 2019 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards monitoring and reporting](http://data.europa.eu/eli/dec_impl/2019/1372/oj)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)
| ISO 639-2/B  <a name="ref_ISO_639_2"></a> | [ISO 639-2/B: Codes for the Representation of Names of Languages](http://www.loc.gov/standards/iso639-2/)


## TG Requirement coverage

Based on requirement numbering in [TG IACS](#ref_TG_IACS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| TG5      | Resource title of LPIS | [IACS-datasets](./IACS-datasets.md) |
| TG6      | Resource title of GSAA | [IACS-datasets](./IACS-datasets.md) |
| TG7      | Resource locator | [IACS-datasets](./IACS-datasets.md) |
| TG8      | Topic category of LPIS and GSAA | [IACS-datasets](./IACS-datasets.md) |
| TG9      | INSPIRE data theme for LPIS | [IACS-datasets](./IACS-datasets.md) |
| TG10      | INSPIRE data theme for GSAA | [IACS-datasets](./IACS-datasets.md) |
| TG11      | Mandatory keyword from GEMET | [IACS-datasets](./IACS-datasets.md) |
| TG12      | Other mandatory keywords for LPIS | [IACS-datasets](./IACS-datasets.md) |
| TG13      | Other mandatory keywords for GSAA | [IACS-datasets](./IACS-datasets.md) |
| TG14      | Mandatory value of the temporal reference type of the LPIS and GSAA datasets | [IACS-datasets](./IACS-datasets.md) |
| TG15      | Updating the value of the last revision metadata element for an LPIS dataset | [IACS-datasets](./IACS-datasets.md) |
| TG16      | Minimum frequency of publishing the updated LPIS datasets | [IACS-datasets](./IACS-datasets.md) |
| TG17      | Value of the last revision of GSAA dataset | [IACS-datasets](./IACS-datasets.md) |
| TG18      | Minimum frequency of publishing the GSAA dataset | [IACS-datasets](./IACS-datasets.md) |

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [IACS-datasets](./IACS-datasets.md) | Ready for review  |

## Open issues


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
