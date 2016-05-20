#A.04.IR01.IR02.hierarchy

**Purpose**: Checks that a resource type is provided

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

Checks if a resource type ([hierarchyLevel](#hierarchyLevel)) is provided and is taken from the [MD_ScopeCode]() codelist.

The test succeeds if the value is either 'dataset', 'service' or 'series'

# Context

**Reference(s)**	 

* [IR MD](./README.md#ref_IR_MD), Part B 1.3, Part D 1
* [TG MD](./README.md#ref_TG_MD),2.2.3, Req 1 & 2
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type:** Automated

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
hierarchyLevel <a name="hierarchyLevel"></a>   | ./gmd:hierarchyLevel/*/@codeListValue
