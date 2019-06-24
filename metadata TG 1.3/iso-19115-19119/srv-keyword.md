# Service keyword

**Purpose**: Service keyword. If the resource is a service, the category or subcategory of the service should be specified.

**Prerequisites**

* [Hierarchy](./hierarchy) 
* [Keyword](./keyword)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

If the resource is a service, at least one [keyword](#keyword) must originate from [EU commission regulation No. 1205/2008, Annex part D, No. 4.](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory)

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD), 2.2.3, Req 15

**Test type**: Automated

**Notes**

The test method does not specify, if language independent codes shall be used or not (which would require support of language specific codes). However, MD TG requirement 15 only considers language independent codes. Dynamic access to all codes of codelist http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory in all languages is therefore not necessary. The test method should be updated to be more specific.

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available service metadata records.  

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="keyword"></a> keyword   | ./gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:keyword
