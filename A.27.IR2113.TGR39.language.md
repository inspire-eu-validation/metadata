
# Metadata language

**Purpose**	

A metadata language is given.

**Test method**	

The test first check is if a [gmd:LanguageCode](#lang) object is given at gmd:language and contains a codeListValue attribute. It is then checked if the codeListValue attribute 
contains a valid 3-letter language code according to [ISO 639-2](http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

**Reference(s)**	 

* [INSPIRE Metadata Implementing Rules](./README.md#IR), Chap. 2.11.3
* ISO 639-2

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="lang"></a> language   | gmd:language

