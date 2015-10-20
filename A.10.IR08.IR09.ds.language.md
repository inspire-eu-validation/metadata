#A.10.IR08.IR09.ds.language

**Purpose**: If the type of the resource was dataset or series and the resource contains textual information, a resource language must be given.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

The test first checks if a [gmd:LanguageCode](#langcode) object is given  and contains a codeList and codeListValue attribute.
It is then checked if the codeListValue attribute contains a valid 3-letter language code according to ISO/TS 19139.
If the type of the resource is not dataset or series, this test is omitted.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.7, Req 8 & 9
* ISO 639-2

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="langcode"></a> LanguageCode  | gmd:identificationInfo[1]/*/gmd:language/gmd:LanguageCode
