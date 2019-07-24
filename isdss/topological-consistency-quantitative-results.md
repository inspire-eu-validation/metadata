# Topological Consistency Quantitative Results

**Purpose**: Test that the topological consistency quantitative results is provided correctly.

**Prerequisites**

**Test method**

* If [Topological Consistency](#topologicalConsistency) and [Quantitative Result](#quantitativeResult) exist,

    * For every [Quantitative Result](#quantitativeResult),

        * Check that [Value Unit](#valueUnit) exists.

        * Check that [Record](#record) exists and it has an attribute "xsi:type".

* If any of the checks fails, the test fails.

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.4.1, Req 2.7

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_TopologicalConsistency)
-----------------------------------------------| ------------------------------------------------------------------
<a name="topologicalConsistency"></a> Topological Consistency | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_TopologicalConsistency
<a name="quantitativeResult"></a> Quantitative Result | gmd:result/gmd:DQ_QuantitativeResult
<a name="valueUnit"></a> Value Unit | gmd:result/gmd:DQ_QuantitativeResult/gmd:valueUnit
<a name="record"></a> Record | gmd:result/gmd:DQ_QuantitativeResult/gmd:value/gco:Record
