# Title

**Purpose**: Checks that a resource title is provided

**Prerequisites**

**Test method**

Validates if a [title](#title) is provided and not an [empty characterstring](./README.md#emptychar)

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), Chap. 2.2.1

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
