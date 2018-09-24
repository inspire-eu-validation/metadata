# Conformity degree 

**Purpose**: Each Conformance Result shall also include the degree of declared conformity against this specification using a property eith value "true" for a conformant resource and "false" for non-conformant resource.

**Prerequisites**

**Test method**

A property [Pass](#Pass) with boolean value will be included with "true" value within the degree of [ConformanceResult](#ConformanceResult) if the resource is compliant and "false" otherwise.

If the conformance has not yet been evaluated, the [Pass](#Pass) element shall be empty and contain a nil reason attribute with value "unknown".

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.4.1, Req C.22

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult
<a name="Pass"></a> Pass   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/gmd:DQ_ConformanceResult/<gmd:pass>


