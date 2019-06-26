# Free Text

**Purpose**: Test the use of free text elements of type gco:CharacterString_PropertyType in the INSPIRE metadata meet one of the 3 defined ways.

**Prerequisites**

**Test method**

* Check that free text elements meet one of the next options:

    * It uses the [Character String](#characterString) child element.

    * It uses [Anchor](#anchor) child element.

    * It uses the xsi:type attribute and provide both [Character String](#characterString) and [Free Text](#freeText) child elements. 

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.1.2 , Req c.4
* [ISO 19115](./README.md#ref_ISO_19115)


**Test type**: Automated

**Notes**

For options 1 and 2 the character string content of elements shall be provided in the language of the metadata.

For option 3 the definition of the used locale shall be provided either using an URI pointing to a [Locale](#locale) element within the same document or to an externally provided gmd:PT_Locale element.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="characterString"></a> Character String | /gmd:MD_Metadata/\*/gco:CharacterString
<a name="anchor"></a> Anchor | /gmd:MD_Metadata/\*/gmx:Anchor
<a name="freeText"></a> Free Text | /gmd:MD_Metadata/\*/gmd:PT_FreeText
<a name="locale"></a> Locale | /gmd:MD_Metadata/gmd:locale/gmd:PT_Locale(@id)
