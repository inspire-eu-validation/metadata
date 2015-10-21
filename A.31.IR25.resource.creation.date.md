#A.31.IR25.resource.creation.date

**Purpose**: It must be discoverable when the described resource was created.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

Check that at least one [Creation date](#creationDate) exists. Is it does, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG MD](README.md#ref_TG_MD) 2.6.4, TG Requirement 25
* [IR MD](README.md#ref_IR_MD), Part B 5.4

**Test type**: Automated

**Notes**

* It's not clear either of the code list values ```creation``` or ```publication``` is enough to pass the test. The table in [TG MD](README.md#ref_TG_MD) chapter 2.6.4 contains the code ```publication``` on the row "ISO/TS 19139 path", but on the other hand the
example XML snippet provided uses the value ```creation```.


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
Creation date <a name="creationDate"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date[gmd:dateType/gmd:CI_DateTypeCode/(@codeList='http://www.isotc211.org/2005/resources/codeList.xml#CI_DateTypeCode' and (@codeListValue='creation' or @codeListValue='publication'))]/gmd:date/gco:Date
