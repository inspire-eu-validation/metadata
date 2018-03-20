# Only One DataIdentification

**Purpose**:
The objective of this test is to harmonize the structure of the metadata for data sets and data set series declaring 
that although more than one IdentificationInfo can be given within the MD_Metadata element, only the first instance
 is used for the identification of the INSPIRE resource.

**Prerequisites**
* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/datasets-and-series/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'data'.

The test first checks if a property of gmd:MD_Metadata element shall contain only 
one [dataIdentification](#dataIdentification) element.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_TG_MD),3.1.2, Req 1.2
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The test method does not mention that the language independent codes should be used.

A unique identifier of the gmd:MD_DataIdentification element is not necessary when building 
the [Coupled resource](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/coupled-resource) 
link by providing a Unique Resource Identifier that is resolved to a URL containing an abstract pointer 
to the gmd:MD_DataIdentification element.

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
dataidentification <a name="dataIdentification"></a>   | ./gmd:identificationInfo[count(gmd:MD_DataIdentification)=1]
