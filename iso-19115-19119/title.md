# Title

**Purpose**: Checks that a resource title is provided

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/schema-validation)

**Test method**

Validates if a [title](#title) is provided and not an [empty characterstring](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#emptychar)

**Reference(s)**	 

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD), Chap. 2.2.1

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
title <a name="title"></a>   | ./gmd:identificationInfo[1]/\*/gmd:citation/\*/title
