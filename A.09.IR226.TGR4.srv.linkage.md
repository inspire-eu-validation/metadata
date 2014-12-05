
# Coupled resource

**Purpose**	

If the type of the resource was service, a resource type should be given.

**Test method**	

Test method	The test first checks if coupling type is given at gmd:identificationInfo[1]/*/srv:couplingType/srv:SV_CouplingType 
and if it has a codeList and a codeListValue attribute, codeListValue must be either tight, coupled or mixed. If this codeListValue 
attribute doesn't exist, an gco:nilReason attribute must be given at gmd:identificationInfo[1]/*/srv:couplingType and must have a 
value of missing, inapplicable, template, unknown or withheld (This will lead to a warning).
If the type of the resource is not service, this test is omitted.

Any of the onlineresources shuold be checked if they are a valid url
if wms/wfs/sos there should be a link vack to the metadata, it should be the same metadata.
if atom 
if soap

# Context

//srv:

**Reference(s)**	 

IR, Chap. 2.2.6
TG req 4 

**Test type:** Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name=""></a>   |


