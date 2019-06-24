# Dataset Conformity

**Purpose**: Test that the metadata includes information on the degree of conformity with the implementing rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

* Checks that at least one [Conformance Result](#conformanceresult) exists.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.4.1, Req C.20

**Test type**: Automated

**Notes**

The multiplicity of this element is one or more.

For each specification, a separate element [Conformance Result](#conformanceresult) must be used.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="conformanceresult"></a> Conformance Result   | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult