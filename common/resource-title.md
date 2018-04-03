# Resource Title


**Purpose**: Know the title of the resource in a clearly understandable way.

**Prerequisites**

**Test method**

* Check the readability and clarity of the metadata [title](#title). Its content will be a free text element not empty in the metadata language. 
* The multiplicity of the element is one.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.1 , Req c.8


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="title"></a> Title  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:title[1]/text()

