# Dataset spatial resolution

**Purpose**: If the type of the resource was dataset or series, Each [spatial resolution](#spatialResolution) is either an [equivalentScale](#equivalentScale) OR a ground sample [distance](#distance).

**Prerequisites**

**Test method**

Each [spatialResolution](#spatialResolution) element must contain either an [equivalentScale](#equivalentScale) or a [distance](#distance) but not both.

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD) 2.7.2, Req 27

**Test type**: Automated

**Notes**

This test is already covered by the XML Schema validation (the content of an MD_Resolution element is a choice between an 'equivalentScale' or 'distance').

The Xpath references for equivalentScale and distance shown below are misleading. They should show the full path starting from MD_Metadata.

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="spatialResolution"></a> spatialResolution | ./gmd:identificationInfo/\*/gmd:MD_DataIdentification/\*/gmd:spatialResolution
<a name="equivalentScale"></a> equivalentScale  | ./gmd:spatialResolution/gmd:MD_Resolution/gmd:equivalentScale
<a name="distance"></a> distance   | ./gmd:spatialResolution/gmd:MD_Resolution/gmd:distance
