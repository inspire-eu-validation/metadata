#A.19.IR28.ds.conformity

**Purpose**: The metadata shall include information on the degree of conformity with the implementing
rules on interoperability of spatial data sets and services.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

For every conformity statement, one conformance result indicated by a boolean value must be given.

The test first checks if there is at least one conformance [result](#result) of type gco:Boolean.
It then performs the following actions for every element at ./*/gmd:result:
*	If the element has an element ./*/gmd:pass, it must contain a value of type gco:Boolean.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD),2.8.1, Req 28
* [IR MD](README.md#ref_IR_MD) Part B. 2.8

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="result"></a> Result   | gmd:dataQualityInfo/*/gmd:report/*/gmd:result
