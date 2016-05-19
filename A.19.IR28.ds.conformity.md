#A.19.IR28.ds.conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing
rules on interoperability of spatial data sets and services.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.04.IR01.IR02.hierarchy](A.04.IR01.IR02.hierarchy.md) must be passed. The outcome has to be 'service' or 'dataset'.

**Test method**

For every conformity statement, one conformance result indicated by a boolean value must be given.

The test first checks if there is at least one conformance [result](#result) of type gco:Boolean.
It then performs the following actions for every element at ./*/gmd:result:
*	If the element has an element ./*/gmd:pass, it must contain a value of type gco:Boolean.

Then, the test evaluate whether the element [gmd:DQ_ConformanceResult](#ConformanceResult) exists

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD),2.8.1, Req 28
* [TG MD](./README.md#ref_TG_MD),2.8
* [IR MD](README.md#ref_IR_MD) Part B. 2.8
* [ISO 19115] (README.md#user-content-ref_ISO_19115)

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/*/gmd:report/*/gmd:result
<a name="ConformanceResult"></a> Conformance Result   | gmd:dataQualityInfo/*/gmd:report/*/gmd:result/gmd:DQ_ConformanceResult
