# Conformity to Technical Specifications

**Purpose**: 

Test that is given the conformity degree with at least one technical specifications providing all the necessary technical elements to actually invoke the service and enable its usage.

**Prerequisites**

* [Conformity](../common/conformity.md)

**Test method**

* Check if full compliance is declared with at least one technical specification providing all the necessary technical elements to actually invoke the service and enable its usage, encoded using a [Conformance Result](#ConformanceResult) element.

* For each [Conformance Result](#ConformanceResult) element,

    * Check if is given a citation for the technical specification encoded using a  [Citation](#citation) element.

    * Check if the degree of conformity with the given specification is defined as "true" in the [Conformity Degree](#conformityDegree) element.

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.3.3.3, Req 5.5

**Test type**: Automated

**Notes**

The multiplicity of the [Conformance Result](#ConformanceResult) element is one or more.

This test must be compliant with [Conformity](../common/conformity.md), [Conformity Specification](../common/conformity-specification.md), [Conformity Degree](../common/conformity-degree.md) requirements from [Common Requirements](../common/README.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="ConformanceResult"></a> Conformance Result   | gmd:result/gmd:DQ_ConformanceResult
<a name="citation"></a> Citation  | gmd:specification/gmd:CI_Citation
<a name="conformityDegree"></a> Conformity Degree | gmd:result/gmd:DQ_ConformanceResult/gmd:pass/gco:Boolean


