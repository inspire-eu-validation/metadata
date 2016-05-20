#A.07.IR05.IR06.ds.identification

**Purpose**: Unique resource identifier. If the type of the resource was dataset or series, a unique identifier identifying the resource must be given.

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed
* [A.04.IR01.IR02.hierarchy](A.04.IR01.IR02.hierarchy.md) must be passed

**Test method**

If the type of the resource is dataset or series, it is checked whether at least one unique [identifier](#identifier) is given. For each gmd:identifier block, a check is performed to see whether it is of type MD_Identifier or RS_Identifier. The contained code element must not be an empty characterstring. In case of RS_identifier, the codespace element is not an empty characterstring either.

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.5, Req 5 & 6
* [IR MD](README.md#ref_IR_MD) Part B. 1.5
* [ISO 19115](README.md#ref_ISO_19115), B.2.7.3

**Test type:** Automated

**Notes**

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="identifier"></a> identifier   | gmd:identificationInfo[1]/*/gmd:citation/*/gmd:identifier
