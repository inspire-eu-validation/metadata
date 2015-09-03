
# Keywords from vocabulary 

**Purpose**	

Keyword values originating from a single version of a single controlled vocabulary
shall be grouped in a single instance

**Test method**	

In order to be consistent with ISO 19115, all the keyword values
originating from a single version of a single controlled vocabulary
shall be grouped in a single instance of the ISO 19115
descriptiveKeywords property. 

For each [descriptiveKeywords](#keyword) element, the referenced controlled vocabulary should be unique

**Reference(s)**	 

* [IR](./README.md#IR), Annex B. 3.2
* [TG](./README.md#TG) Req 19 

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keyword"></a> Keyword   | gmd:identificationInfo[1]/*/gmd:descriptiveKeywords

