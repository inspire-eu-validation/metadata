# Resource Abstract


**Purpose**: Describe the content of the metadata through a brief narrative summary.

**Prerequisites**

**Test method**

* Provide a brief narrative summary on the content of the data set, data series or services described.
* It will be coded using an [abstract](#abstract) element with a non-empty free text element content in the metadata language.

* The multiplicity of this element is one.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.2 , Req c.9


**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="abstract"></a> Abstract  | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/gmd:title[1]/text()

