# Dataset specification

**Purpose**: For every conformity statement, one citation of the product specification or user requirement against which data is being evaluated must be given.

**Prerequisites**

**Test method**

This test case only applies to records with a hierarchyLevel value 'dataset' or 'series'.

The test first checks if there is at least one [specification](#specification). In case there is none, the test fails.
It then performs the following checks
*	The [specification](#specification) must contain an element of type gmd:CI_Citation/gmd:title which should not be an [empty characterstring](./README#emptychar)
*	The [specification](#specification) must contain an element of type gmd:CI_Citation/gmd:date[./\*/gmd:dateType/\*/text()='{type}']/\*/gmd:date, where {type} is one of 'creation', 'revision' and 'publication'.
*	The [DQ_ConformanceResult](#DQ_ConformanceResult) has an element gmd:pass that must contain a value of type gco:Boolean.
*	The [specification](#specification) has gmd:DQ_DomainConsistency as a parent element.

**Reference(s)**

* [TG MD](./README#ref_TG_MD), 2.8.2
* [TG MD](./README#ref_TG_MD), 2.8, Req 29

**Test type**: Automated

**Notes**

The test method does not explicitly state if the test applies only to datasets, dataset series, or also services. TG MD sections 2.8 and 2.8.2 are not clear on this point, either. For example, section 2.8.2 says: "If a spatial  data service is an INSPIRE Network service, use this element to report the relevant INSPIRE Network Implementing Rule to which it conforms." The test has therefore been implemented as a common test in the ETSs.

The test method states that a warning is thrown, if a metadata record does not contain a specification. The ETS only checks requirements, i.e. it detects failures. Therefore, it does not report warnings.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="specification"></a> specification    | ./gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result/\*/gmd:specification
<a name="DQ_ConformanceResult"></a> Conformance Result    | ./gmd:dataQualityInfo/*/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult
