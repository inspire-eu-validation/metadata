# Dataset conformity

**Purpose**: Test that the metadata includes information on the degree of conformity with the implementing rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

* Check that [Conformance Result](#conformanceResult) exists and it declares conformity to the Implementing Rules for interoperability of spatial data sets and services [Regulation 1089/2010](https://publications.europa.eu/en/publication-detail/-/publication/6c9b0d4b-831f-47fe-b551-ac13604d9797/language-en).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.4.2, Req 1.10
* [ISO 19115](./README.md#ref_ISO_19115)
* [Regulation 1089/2010](https://publications.europa.eu/en/publication-detail/-/publication/6c9b0d4b-831f-47fe-b551-ac13604d9797/language-en)

**Test type**: Automated

**Notes**

The multiplicity of this element is one.

The specification for this requirement is defined in [Conformity](../common/conformity.md), [Conformity Specification](../common/conformity-specification.md), [Conformity Degree](../common/conformity-degree.md) requirements from [Common Requirements](../common/README.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="conformanceResult"></a> Conformance Result | gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult
