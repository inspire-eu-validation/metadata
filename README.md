# INSPIRE dataset and service metadata version 2.0

The Abstract Test Suites (ATSs) defined in this section are based on the Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007 version 2.0 [TG MD](#ref_TG_MD).

## Abstract Test Suites & Conformance Classes

The conformance classes (CC), described in the abovementioned TG, are compound of requirements that must be met to be conformant with INSPIRE. An ATS is created for every CC in order to make the metadata validation process as clear as possible.

The [TG MD](#ref_TG_MD) defines 8 CC. The first one is a set of Common Requirements for datasets, data set series and data services. CC1 and CC2 are relevant to data sets and data set series only. Additionally, two new ATSs (CC2b and CC2c) are developed, which is not yet part of the TG MD and include requirements relevant for INSPIRE Monitoring and Reporting and requirements for IACS datasets, respectively. Finally, CC from CC3 to CC7 are relevant to services only.

* Metadata for INSPIRE datasets and data set series
    * [Common Requirements for XML Encoded INSPIRE metadata](./common/README.md)
    * [Conformance Class 1: Baseline metadata for data sets and data set series](./datasets-and-series/README.md)
    * [Conformance Class 2: Interoperability metadata for data sets and data set series](./isdss/README.md)
    * [Conformance Class 2b: Monitoring metadata for data sets and data set series](./monitoring/README.md)
    * [Conformance Class 2c: INSPIRE data sets and data set series metadata for IACS](./iacs/README.md)

* Metadata for INSPIRE Spatial Data Services
    * [Common Requirements for XML Encoded INSPIRE metadata](./common/README.md)
    * [Conformance Class 3: Baseline metadata for Spatial Data Services](./sds/README.md)
    * [Conformance Class 4: Metadata for INSPIRE Network Services](./ns/README.md)
    * [Conformance Class 5: Metadata for Invocable Spatial Data Services](./sds-invocable/README.md)
    * [Conformance Class 6: Metadata for Interoperable Spatial Data Services](./sds-interoperable/README.md)
    * [Conformance Class 7: Metadata for Harmonised Spatial Data Services](./sds-harmonised/README.md)

## Conformance classes relations and dependencies
The mutual dependencies between conformance classes are shown in Figure 1.

![Diagram](./hierarchydiagram.jpg)
Figure 1. Dependencies between conformance classes in the TG MD and link with the TG chapters.


Conformance classes at each level depend on conformance classes at the above levels. For instance, to satisfy CC6, three conformance classes (CC5, CC3 and Common Requirements) must be also satisfied. Similarly, to satisfy the Monitoring metadata requirements (CC2b), both CC1 and Common Requirements must be also satisfied.

## External document references


| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007](https://inspire-mif.github.io/technical-guidelines/metadata/metadata-iso19139/metadata-iso19139.pdf)
| ID MON <a name="ref_ID_MON"></a> | [Commission Implementing Decision of 19.8.2019 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards monitoring and reporting](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32019D1372&from=EN)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)
| ISO 639-2/B  <a name="ref_ISO_639_2"></a> | [ISO 639-2/B: Codes for the Representation of Names of Languages](http://www.loc.gov/standards/iso639-2/)
