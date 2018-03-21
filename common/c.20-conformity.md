# Dataset conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing 
rules on interoperability of spatial data sets.

**Prerequisites**

**Test method**

* The test first checks if there is at least one conformance [result](#Result) of type [gmd:DQ_ConformanceResult](#ConformanceResult).

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity/README#ref_TG_MD), 2.4.1, Req C.20

**Test type**: Automated

**Notes**
For each specification, a separate element gmd: DQ_ConformanceResult must be used.
The multiplicity of this element is 1 ..to *.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/\*/gmd:report/\*/gmd:result
