# Spatial Data Service category Keywords

**Purpose**: 
**Prerequisites**

* [Resource Type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The test should verify if at least one gmd:keyword is available and matches a concept in the thesaurus.

For each INSPIRE Spatial Data Theme, a gmd:keyword element shall be included with the title of the theme as a 
Non-empty Free Text Element [empty CharacterString](http://inspire.ec.europa.eu/id/ats/metadata/2.0/iso-19115-19119/README#emptychar) content in the language of the metadata.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_TG_MD),4.1.2.2, Req 3.4
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type**: Automated

**Notes**

The test method is not clear on how a specific code list is referenced in a gmd:thesaurusName.
The ETS assumes that the gmd:thesaurusName/\*/gmd:title/\*/text() equals 'GEMET - INSPIRE themes, version 1.0'. 

##Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> Hierarchy Level | ./gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="keyword"></a> keyword   | ./gmd:identificationInfo[1]/\*/gmd:descriptiveKeywords/\*/gmd:keyword