# Metadata Structure and Encoding: Code List Value

**Purpose**: The encoding of the metadata must be encoded from a specific root element, MD_Metadata.

**Prerequisites**

**Test method**

* The INSPIRE metadata elements that are assigned to the [code lists](#codeList) in [ISO 19139] using the [Code List Value](#value) attribute must identify the code list * corresponding to the value (as defined in the tables in [ISO 19115]).

**Reference(s)**	 

* [TG MD](https://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.1.1 , Req c.3
* [ISO 19115](https://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115)


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](https://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression ()
-----------------------------------------------| -------------------------------------------------------------------------
<a name="codeList"></a> Code List | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")//\*/
<a name="value"></a> Value   | <gmd:MD_Metadata>/\*/@codeListValue
