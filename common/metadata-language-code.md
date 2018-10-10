# Metadata Language

**Purpose**: Test that a resource language is given pointing to one of the official languages of the Community expressed in conformity with ISO 639-2.

**Prerequisites**

**Test method**

* Check that exactly one [LanguageCode](#langcode) node exists. If it does:

    * Check that the attribute codeList is "http://www.loc.gov/standards/iso639-2/"

    * Check that the attribute codeListValue is one of the three-letter language codes of the [ISO 639-2/B](./README.md#ref_ISO_639_2)
    
* If any of the checks fails the test fails.

**Reference(s)**	 

* [TG MD](./READM.mdE#ref_TG_MD), 2.2.2 , Req c.5
* [ISO 639-2/B](./README.md#ref_ISO_639_2)

**Test type**: Automated

**Notes**

The multiplicity of [gmd:LanguageCode](#langcode) is 1.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="langcode"></a> LanguageCode  | /gmd:MD_Metadata/gmd:language/gmd:LanguageCode
