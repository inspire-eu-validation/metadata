# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing
rules on interoperability of spatial data sets and services.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

For every conformity statement, one conformance result indicated by a boolean value must be given.

The test first checks if there is at least one conformance [result](#result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).

Every [gmd:DQ_ConformanceResult](#ConformanceResult) has an element gmd:pass that must contain a value of type gco:Boolean.

One of the [CI_Citation](#CI_Citation) elements shall contain title and date of the [Regulation 1089/2010], i.e.
* Title (in English): "Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services" (or the corresponding title in the relevant metadata language)
* Date: 2010-12-08
* Date type: publication

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.8.1, Req 28
* [TG MD](./README.md#ref_TG_MD), 2.8
* [ISO 19115](./README.md#ref_ISO_19115)
* [Regulation 1089/2010](https://eur-lex.europa.eu/eli/reg/2010/1089/oj)

**Test type**: Automated

**Notes**

According to TG MD 2.8.1 (and recommendation 21), the value of gmd:pass may also be null (with nilReason = “unknown”). This is not yet covered by the test method. The ETS covers this aspect, too.

TG MD Requirement 29 is also relevant, because it states of which type the result of a dataQualityInfo shall be (DQ_DomainConsistency). The ETS covers this aspect, too.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult
<a name="CI_Citation"></a> CI_Citation   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/\*/gmd:CI_Citation
