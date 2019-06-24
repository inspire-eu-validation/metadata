# Conformity Degree 

**Purpose**: Test that each Conformance Result includes the degree of declared conformity against this specification using a property with value "true" for a conformant resource and "false" for non-conformant resource.

**Prerequisites**

[Conformity Specification](./conformity-specification.md)

**Test method**
* For every [Conformance Result](#conformanceResult) element,

    * Check that it has a child element [Pass](#pass).

        * If gco:Boolean child exists, check its value is 'True' or 'False'.

        * Else, check that an attribute gco:nilReason="unknown" exists.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4.1, Req C.22

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="conformanceResult"></a> Conformance Result | gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult
<a name="pass"></a> Pass | gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult/gmd:pass
