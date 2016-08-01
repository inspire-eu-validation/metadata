# Service keyword

**Purpose**: Service keyword. If the resource is a service, the category or subcategory of the service should be specified.

**Prerequisites**

* [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) 
* [Keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keyword)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

If the resource is a service, at least one [keyword](#keyword) must originate from [EU commission regulation No. 1205/2008, Annex part D, No. 4.](http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory)

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), 2.2.3, Req 15

**Test type**: Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="keyword"></a> keyword   | ./gmd:identificationInfo[1]/*/gmd:descriptiveKeywords/*/gmd:keyword
