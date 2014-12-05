
# Resource title

### Purpose	

The title by which the cited resource is known

### Test method	

Validates if a [title](#title) is provided (available and not empty) and is formatted as either gco:CharacterString, gmx:Anchor or gmd:PT_FreeText. 
In the latter case, a schema validation is performed depending on the GML version (see About schema validation).

### Reference(s)	 

INSPIRE Metadata Implementing Rules, Chap. 2.2.1

**Test type:** Automated

### Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
