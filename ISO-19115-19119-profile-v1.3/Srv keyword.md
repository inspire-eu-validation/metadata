# Srv keyword

**Purpose**: Srv keyword. If the resource is a service, the type of service should be specified

**Prerequisites**
* [Schema validation](Schema validation.md) must be passed
* [Keyword](Keyword.md) must be passed

**Test method**

If the resource is a service, at least one [keyword](#keyword) must originate from [EU commission regulation No. 1205/2008, Annex part D, No. 4.](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory)

If the type of the resource is not service, this test is omitted.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.3, Req 15


**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> keyword   | ./gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
