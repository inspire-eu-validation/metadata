# Metadata Structure and Encoding: Free Text

**Purpose**: Define the basic element to provide text of unrestricted length without internal XML structure.

**Prerequisites**

**Test method**

Check the use of free text elements of type gco:CharacterString_PropertyType in the 
INSPIRE metadata and see if they meet any of the 3 ways to be defined:

* Using the [gco:CharacterString](#characterString) child element.
* Using [gmx:Anchor](#anchor) child element, or 
* Using the xsi:type attribute and provide both [gco:CharacterString](#characterString) and [gmd:PT_FreeText](#freeText) child elements. 

For options 1 and 2 the character string content of elements shall be provided in the language of the metadata.

For option 3 the definition of the used locale shall be provided either using an URI pointing to a [Locale](#locale) element within the same document or to an externally provided gmd:PT_Locale element.

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_TG_MD), 2.1.2 , Req c.4
* [ISO 19115](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#ref_ISO_19115)


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression ()
-----------------------------------------------| -------------------------------------------------------------------------
<a name="characterString"></a> Character String   | <gmd:MD_Metadata>/\*/<gco:CharacterString>
<a name="anchor"></a> Anchor   | <gmd:MD_Metadata>/\*/<gmx:Anchor>
<a name="freeText"></a> Free Text   | <gmd:MD_Metadata>/\*/<gmd:PT_FreeText>
<a name="locale"></a> Locale  | <gmd:MD_Metadata>/<gmd:locale>/<gmd:PT_Locale>(@id)
