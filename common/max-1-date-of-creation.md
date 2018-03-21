# Not More than one Date of Creation


**Purpose**: Not more than one date of creation for the metadata shall be given.

**Prerequisites**

**Test method**

Check that at most one [Creation date](#creationDate) exists.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.3.4 , Req c.12
* [ISO 8601](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_ISO_8601)

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="creationDate"></a> Creation Date  | ./gmd:identificationInfo[1]/\*/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date[gmd:dateType/gmd:CI_DateTypeCode/(@codeList='http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode' and (@codeListValue='creation'))]/gmd:date/gco:Date
