# Topological consistency descriptive results
**Purpose**: Evaluate the quantitative results for topological consistency measures.

**Prerequisites**

**Test method**

*The quantitative results for topological consistency measures shall be reported using the [Topological Consistency](#TopologicalConsistency) 
element with a gmd:DQ_QuantitativeResult element as the value of its mandatory gmd:result property. The multiplicity of the element is 0 or more.

*The [Value Unit](#valueUnit) and [Value Record](#valueRecord) child elements are mandatory and shall be used for giving a numerical or 
otherwise quantitative value of the evaluated topology consistency measure.

*The [Value Unit](#valueUnit) and [Value Record](#valueRecord) child elements are mandatory and shall be used for giving a numerical or 
otherwise quantitative value of the evaluated topology consistency measure. The type of this element shall be chosen based on the result 
type of the particular measure, and it shall be declared using the xsi:type attribute.


**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/spatial-representation-type/README#ref_TG_MD) 3.2.4.1, Req 2.8

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="TopologicalConsistency"></a> Topological Consistency | ./gmd:dataQualityInfo/\*/gmd:DQ_TopologicalConsistency[1]
<a name="valueUnit"></a> Value Unit | ./gmd:dataQualityInfo/\*/gmd:DQ_TopologicalConsistency/*\/gmd:valueUnit
<a name="valueRecord"></a> Value Record | ./gmd:dataQualityInfo/\*/gmd:DQ_TopologicalConsistency/*\/gmd:value/gco:Record


