
# Resource type

	

md_IR223

**Purpose**	

Type of the cited resource must be provided

**Test method**	

Checks if a resource type ([hierarchyLevel](#hierarchyLevel)) is provided and is taken from the [MD_ScopeCode](http://inspire.ec.europa.eu/metadata-codelist/ResourceType/) codelist.

To be relevant for INSPIRE the value should be either 'dataset', 'service' or 'series' 
  
# Context 

**Reference(s)**	 

* [IR](./README.md#IR), Annex B. 1.3
* [TG](./README.md#TG), Req 1 & 2

**Test type:** Automated

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
hierarchyLevel <a name="hierarchyLevel"></a>   | ./gmd:hierarchyLevel/*/@codeListValue