# Access Point

**Purpose**: Test that is provided the access point of the service.

**Prerequisites**

**Test method**

* Check if each access point of the Invocable Spatial Data Service is described using an [Online Access](#onlineAccess) element.

* For each [Online Access](#onlineAccess) element,

    * Check if is provided a gmd:linkage element containing the [Access URL](#accessUrl) element containing a detailed description of a spatial data service including a list of end points to allow its execution.

    * Check if is provided a [description](#accessDescription) element containing the value "accessPoint" of the code list OnLineDescriptionCode in the INSPIRE Registry.

    * Check if the description element has a "xlink:href" attribute with the value "http://inspire.ec.europa.eu/metadata-codelist/OnLineDescriptionCode/accessPoint".

**Reference(s)**

* [TG MD](./README.md#ref_TG_MD) 4.3.2.1, Req 5.2

**Test type**: Automated

**Notes**

The multiplicity of this [Online access](#onlineAccess) element is one or more.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions)
-----------------------------------------------| ------------------------------------------------------------------
<a name="onlineAccess"></a> Online Access | gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource
<a name="accessUrl"></a> Access URL | gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL
<a name="accessDescription"></a> Access description | gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:description/gmd:Anchor
