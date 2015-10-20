#A.02.title

**Purpose**: The title by which the cited resource is known

**Prerequisites**

* [A.01.validate](A.01.validate.md) must be passed

**Test method**

Validates if a [title](#title) is provided and not an [empty characterstring](./README.md#emptychar)

**Reference(s)**	 

* [IR MD](./README.md#ref_IR_MD), Part B, 1.1

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
