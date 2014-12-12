
# Resource abstract

**Purpose**	

Validates if a resource abstract is provided 

**Test method**	

Checks if an abstract is provided (not empty string)  for each of the advertised languages 
and is provided as either gco:CharacterString, gmx:Anchor or gmd:PT_FreeText. 
In case of gmx:Anchor, the URL in the anchor should [resolve](./README.md#resolve) to a document.
In case of PT_FreeText, a schema validation is performed depending on the GML version. 

**Reference(s)**	 

* IR, Chap. 2.2.2

**Test type:** Automated
	
**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | gmd:identificationInfo[1]/*/gmd:abstract
