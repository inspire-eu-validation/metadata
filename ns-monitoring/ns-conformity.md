# Network services conformity

**Purpose**: Test that the service metadata includes information on the degree of conformity with the implementing rules for network services.

**Prerequisites**

**Test method**

* Check that [Conformance Result](#conformanceResult) exists and it declares conformity to the Implementing Rules for network services [Regulation 976/2009](http://data.europa.eu/eli/reg/2009/976).

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.2.2.1 Conformity, Rec 4.1 - 4.2
* [ISO 19115](./README.md#ref_ISO_19115)
* [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://data.europa.eu/eli/reg/2009/976)


**Test type**: Automated

**Notes**

The multiplicity of this element is one.

Sample encoding for this metadata element is contained in the [4.2.2.1. Conformity](https://github.com/INSPIRE-MIF/technical-guidelines/blob/main/metadata/metadata-iso19139/metadata-iso19139.adoc#4221-conformity) section of the TG MD.

The specification for this requirement is defined in [Conformity](../common/conformity.md), [Conformity Specification](../common/conformity-specification.md), [Conformity Degree](../common/conformity-degree.md) requirements from [Common Requirements](../common/README.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="conformanceResult"></a> Conformance Result | gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult
