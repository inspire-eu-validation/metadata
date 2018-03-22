# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial services.

**Prerequisites**

**Test method**

The test first checks if there is at least one conformance [result](#result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).
Every [gmd:DQ_ConformanceResult](#ConformanceResult) has an element gmd:pass that must contain a value of type gco:Boolean.

This element must contain a citation of [Regulation 1089/2010] codified in accordance with the [Conformity  Specification](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-specification).

The degree of compliance will be coded according to the common requirement of [Conformity  Degree](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-degree).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_TG_MD), 4.3.3.1, Req 5.3
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_ISO_19115)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | ./gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | ./gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult
