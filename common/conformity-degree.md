# Conformity degree 

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

* A property [Pass](#Pass) with boolean value will be included with "true" value within the degree of [ConformanceResult](#ConformanceResult) if the resource is compliant and "false" otherwise.

* If the conformance has not yet been evaluated, the gmd:pass element shall be empty and contain a nil reason attribute with value "unknown"

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.4.1, Req C.22

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/<gmd:specification>
<a name="Pass"></a> Pass   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/<gmd:specification>


