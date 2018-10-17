# Conformity

**Purpose**: 
Test that the conformity degree is given implementing rules for interoperability of spatial data sets and services.

**Prerequisites**

**Test method**

* Check if is given a [Conformance Result](#ConformanceResult) element declaring the conformity to the Implementing Rules for interoperability of spatial data sets and services.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.3.3.1, Req 5.3
* [ISO 19115](./README.md#ref_ISO_19115)

**Test type**: Automated

**Notes**

The multiplicity of the [ConformanceResult](#ConformanceResult) element is one for this purpose.

The specification for this requirement is defined in [Conformity](../common/conformity.md), [Conformity Specification](../common/conformity-specification.md), [Conformity Degree](../common/conformity-degree.md) requirements from [Common Requirements](../common/README.md)

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency
-----------------------------------------------| -------------------------------------------------------------------------
<a name="ConformanceResult"></a> Conformance Result   | gmd:result/gmd:DQ_ConformanceResult