# Group Keywords by CV

**Purpose**: Control grouping of keywords in the same controlled vocabulary of origin.

**Prerequisites**

**Test method**
*  The keywords that come from the same vocabulary controlled under an element [Keywords](#keywords) will be grouped.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.5 , Req c.16


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keywords"></a> Keywords  | ./gmd:identificationInfo[1]/\*/descriptiveKeywords/gmd:MD_Keywords

