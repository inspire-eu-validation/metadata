
# Resource title

**Purpose**	

The title by which the cited resource is known

**Test method**	

Validates if a [title](#title) is provided and not an [empty characterstring](./README.md#emptychar)

**Reference(s)**	 

* [IR](./README.md#IR), Annex B 1.1

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
