# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial data sets..

**Prerequisites**

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'dataset' or 'series'.

The test first checks if there is at least one conformance [result](#result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).
Every [gmd:DQ_ConformanceResult](#ConformanceResult) has an element gmd:pass that must contain a value of type gco:Boolean.

This element must contain a citation of [Regulation 1089/2010] codified in accordance with the [Conformity  Specification](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-specification).

The degree of compliance will be coded according to the common requirement of [Conformity  Degree](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-degree).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-locator/README#ref_TG_MD), 3.1.4.2, Req 1.10
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_ISO_19115)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats//ata/2.0/sets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="result"></a> Result   | ./gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | ./gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult
