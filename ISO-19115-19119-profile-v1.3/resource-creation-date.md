#Resource creation date

**Purpose**: There cannot be more than one creation date.

**Prerequisites**
* [Schema validation](schema-validation.md) must be passed

**Test method**

Check that at most one [Creation date](#creationDate) exists. If it does, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG MD](README.md#ref_TG_MD) 2.6.4, TG Requirement 25


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
Creation date <a name="creationDate"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date[gmd:dateType/gmd:CI_DateTypeCode/(@codeList='http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode' and (@codeListValue='creation'))]/gmd:date/gco:Date
