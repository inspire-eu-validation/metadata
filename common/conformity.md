# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

The test first checks if there is at least one conformance [result](#Result) of type [Conformance Result](#conformanceresult).
For each specification, a separate element [Conformance Result](#conformanceresult) must be used.
The multiplicity of this element is one or more.
**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.4.1, Req C.20

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | <gmd:dataQualityInfo>/\*/<gmd:report>/\*/<gmd:result>
<a name="conformanceresult"></a> Conformance Result   | <gmd:dataQualityInfo>/\*/<gmd:report>/\*/<gmd:result>/<gmd:DQ_ConformanceResult>

