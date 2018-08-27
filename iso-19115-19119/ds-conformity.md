# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing
rules on interoperability of spatial data sets and services.

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

For every conformity statement, one conformance result indicated by a boolean value must be given.

The test first checks if there is at least one conformance [result](#result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).

Every [gmd:DQ_ConformanceResult](#ConformanceResult) has an element gmd:pass that must contain a value of type gco:Boolean.

One of the CI_Citation elements shall contain title and date of the [Regulation 1089/2010].

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD),2.8.1, Req 28
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD),2.8
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_ISO_19115)

**Test type**: Automated

**Notes**

According to TG MD 2.8.1 (and recommendation 21), the value of gmd:pass may also be null (with nilReason = “unknown”). This is not yet covered by the test method. The ETS covers this aspect, too.

TG MD Requirement 29 is also relevant, because it states of which type the result of a dataQualityInfo shall be (DQ_DomainConsistency). The ETS covers this aspect, too.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult
