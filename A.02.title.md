#A.02.title

**Purpose**: Checks that a resource title is provided

**Prerequisites**

* [A.01.validate](A.01.validate.md) must be passed

**Test method**

If [A.01.validate](A.01.validate.md) is passed, no further checks are required.

**Reference(s)**	 

* [IR MD](./README.md#ref_IR_MD), Part B, 1.1

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
