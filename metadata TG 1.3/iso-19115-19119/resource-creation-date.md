#Resource creation date

**Purpose**: There cannot be more than one creation date.

**Prerequisites**

**Test method**

Check that at most one [Creation date](#creationDate) exists. If it does, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG MD](./README#ref_TG_MD) 2.6.4, TG Requirement 25

**Test type**: Automated

**Notes**

The test method indicates that there is no more than one creation date per metadata resource. It is not clear, if that means that there must be exactly one creation date. In other words, it is not clear, if the creation date is optional. TG MD 2.6.4 is not entirely clear on this, either. In requirement 25 it says that there shall be a single creation date. However, in the table above it says that "at least one date of publication / date of creation / date of revision is required" - which is confusing since that section of the TG MD is only about the date of creation. The ETS currently checks that there is 0..1 creation date.

The Xpath below also incorporates a specific value for the @codeList (http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode). In metadata records we have frequently seen 'CI_DateTypeCode' as value for this attribute.
The ETS currently allows both http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode and CI_DateTypeCode as values of @codeList.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
Creation date <a name="creationDate"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date[gmd:dateType/gmd:CI_DateTypeCode/(@codeList='http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode' and (@codeListValue='creation'))]/gmd:date/gco:Date
