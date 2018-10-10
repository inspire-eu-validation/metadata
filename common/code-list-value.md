# Code List Value

**Purpose**: Test that the coded values are encoded using the Code List Value attribute.

**Prerequisites**

**Test method**

* Check that the elements that are assigned to the [Code Lists](#codeList) in [ISO 19139](http://standards.iso.org/iso/19139/resources/) using the [Code List Value](#value) attribute must identify the code list corresponding to the value (as defined in the tables in [ISO 19115](https://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115)).

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD), 2.1.1 , Req c.3
* [ISO 19115](./README#ref_ISO_19115)
* [ISO 19139](http://standards.iso.org/iso/19139/resources/)


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="codeList"></a> Code List | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")/\*/
<a name="value"></a> Code List Value | /gmd:MD_Metadata/\*/@codeListValue
