# Character Encoding

**Purpose**: Test that the character encoding for data sets and series is provided correctly.

**Prerequisites**

**Test method**

* For every [Character Set Code](#characterSetCode),

    * Check that it has an attribute codeListValue with value from [ISO 19139](http://standards.iso.org/iso/19139/resources/).

**Reference(s)**	 
* [TG MD](./README.md#ref_TG_MD) 3.2.2.2, Req 2.5
* [ISO 19139](http://standards.iso.org/iso/19139/resources/)

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

This element is mandatory only if an encoding is used that is not based on UTF-8.

If more than one character encoding is used within the described data set or data sets series, all used character 
encodings, including UTF-8 (code list value "utf8"), shall be given using this element.

According to ISO/TS 19139:2007, it is also recommended that the [Character Set Code](#characterSetCode) element has a non-empty free text value.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:characterSet)
-----------------------------------------------| ------------------------------------------------------------------
<a name="characterSetCode"></a> Character Set Code | gmd:MD_CharacterSetCode
