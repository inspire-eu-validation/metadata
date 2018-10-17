# Resource Language

**Purpose**: Test that a resource language is provided.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* For every [Language](#lang) node,

    * Check that [Language Code](#langCode) exists.

    * For every [Language Code](#langCode) node,

        * Check that the attribute codeList is "http://www.loc.gov/standards/iso639-2/" and the attribute codeListValue is one of the three-letter bibliographic language code values [ISO 6392B](http://inspire.ec.europa.eu/schemas/common/1.0/common.xsd) or "zxx" value.

* If any of the checks fails, the test fails.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 3.1.2.4, Req 1.6
* [ISO 639-2](./README.md#ref_ISO_639_2)

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="lang"></a> Language  | gmd:language
<a name="langCode"></a> Language Code | gmd:language/gmd:LanguageCode
