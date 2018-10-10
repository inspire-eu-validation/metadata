# Resource Locator

**Purpose**: 

Test that a resource locator linking to the described Spatial Data Service is given if online access is available. If not, tests that is provided an URL pointing to an online resource providing additional information of the service, if available.

**Prerequisites**

* [Resource Type](./resource-type.md)

**Test method**

* If online access to the service is available:
    
    * Check if a resource locator linking to the described Spatial Data Service is given encoded using an [online access](#onlineAccess) element.

* If online access is NOT available, but there is a publicly available online resource providing additional information about the described service:

    * Check if the URL pointing to the resource is given encoded using an [online access](#onlineAccess) element.

**Reference(s)**

* [TG MD](*/README.md#ref_TG_MD) 4.1.3.1, Req 3.7

**Test type**: Automated

**Notes**

The multiplicity of this element is zero or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="onlineAccess"></a> Online Access |  gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL