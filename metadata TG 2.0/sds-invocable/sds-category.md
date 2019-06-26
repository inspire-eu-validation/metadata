# SDS Category Keywords

**Purpose**:

Test that the service category is given implementing rules for interoperability of spatial data sets and services.

**Prerequisites**

**Test method**

* Check if is given a [Conformance Result](#ConformanceResult) element according with the [Conformity](../common/conformity.md) common requirement.

* Check if [Conformance Result](#ConformanceResult) contains a citation for one of the three Conformance Classes for Invocable Spatial Data Service categories according with the [Conformity Specification](../common/conformity-specification.md) common requirement.

* Check if the title of the cited Conformance Class is encoding using the [Title](#title) element.

* Check if [Title](#title) element has an "xlink:href" attribute with the permanent unique identifier of a Conformance Class. The valid values are:
    
    * http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable
    * http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable
    * http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-harmonised

* Check if [Title](#title) element contains the corresponding neutral name of the category. The valid values are:
  
    * invocable
    * interoperable
    * harmonised

* Check if the degree of conformity with the cited Conformance Class is defined as "true" in the [Conformity Degree](#conformityDegree) element.


**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 4.3.3.2, Req 5.4
* [ISO 19115](./README.md#ref_ISO_19115)

**Test type**: Automated

**Notes**

The multiplicity of the [Conformance Result](#ConformanceResult) element is one for this purpose.

This test must be compliant with [Conformity](../common/conformity.md), [Conformity Specification](../common/conformity-specification.md), [Conformity Degree](../common/conformity-degree.md) requirements from [Common Requirements](../common/README.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="ConformanceResult"></a> Conformance Result | gmd:result/gmd:DQ_ConformanceResult
<a name="title"></a> Title | gmd:specification/gmd:CI_Citation/gmd:title/gmd:Anchor
<a name="conformityDegree"></a> Conformity Degree | gmd:result/gmd:DQ_ConformanceResult/gmd:pass/gco:Boolean