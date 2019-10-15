# Topological Consistency Descriptive Results

**Purpose**: Test that the topological consistency descriptive results is provided correctly.

**Prerequisites**

**Test method**

* If [Topological Consistency](#topologicalConsistency) and [Conformance Result](#conformanceResult) exist,

    * For every [Conformance Result](#conformanceResult),

        * Check that [Title](#title) element exists and its value is "INSPIRE Data Specifications - Base Models - Generic Network Model".
        
        * Check that [Date](#date) element exists.

        * Check that [Date Type Code](#dateTypeCode) element exist and it has an attribute codeListValue with value "publication".

        * Check that [Pass](#pass) element exists and its value is false.

        * Check that [Explanation](#explanation) element exists and its content is non-empty free text.

* If any of the checks fails, the test fails.

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.4.1, Req 2.8

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

According to ISO/TS 19139:2007, it is also recommended that the [Date Type](#dateType) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_TopologicalConsistency)
-----------------------------------------------| ------------------------------------------------------------------
<a name="topologicalConsistency"></a> Topological Consistency | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_TopologicalConsistency
<a name="conformanceResult"></a> Conformance Result | gmd:result/gmd:DQ_ConformanceResult
<a name="title"></a> Title | gmd:result/gmd:DQ_ConformanceResult/gmd:specification/gmd:CI_Citation/gmd:title/gco:CharacterString
<a name="date"></a> Date | gmd:result/gmd:DQ_ConformanceResult/gmd:specification/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date
<a name="dateTypeCode"></a> Date Type Code | gmd:result/gmd:DQ_ConformanceResult/ gmd:specification/gmd:CI_Citation/ gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
<a name="pass"></a> Pass | gmd:result/gmd:DQ_ConformanceResult/gmd:pass
<a name="explanation"></a> Explanation | gmd:result/gmd:DQ_ConformanceResult/gmd:explanation
