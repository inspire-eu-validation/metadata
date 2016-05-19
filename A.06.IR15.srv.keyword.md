#A.06.IR15.srv.keyword

**Purpose**: Keywords for Resource type Service. If the resource is a service, the type of service should be specified

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.13.IR13.keyword](A.13.IR13.keyword.md) must be passed

**Test method**

If the resource is a service, at least one [keyword](#keyword) must originate from [EU commission regulation No. 1205/2008, Annex part D, No. 4.](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory)

If the type of the resource is not service, this test is omitted.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.3, Req 15
* [IR MD](README.md#ref_IR_MD) Part B. 1.5, Article 4, part D

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | ./gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
