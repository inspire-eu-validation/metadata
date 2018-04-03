# Resource Locator

**Purpose**: Tested if it provides the access point of the service through an 
Internet address containing a detailed description of a spatial data service.

**Prerequisites**
* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds/resource-type)

**Test method**

* Check that access point of the Invocable Spatial Data Service is described in the using a gmd:CI_OnlineResource element. 

* - The child element gmd: linkage must contain the access point URL that contains a detailed description of a spatial data service
* - The child element gmd: description must contain a [Url Access Text](#urlAccessText) element that points to the "accessPoint" value of the OnLineDescriptionCode codelist in the INSPIRE66 registry.

* The multiplicity of this element is one or more.

**Reference(s)**

* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#ref_TG_MD) 4.3.2.1, Req 5.2

**Test type**: Automated

**Notes**
If no online access is available, but there is a publicly available online resource providing additional information about the described service, 
the URL pointing to this resource shall be given instead.

A Resource Locator encoded using the gmd:CI_OnlineResource element may also include gmd:name, gmd:description, and gmd:function properties.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-invocable/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="onlineAccess"></a> Online Access |  ./gmd:distributionInfo/\*/gmd:transferOptions/gmd:MD_DigitalTransferOptions/ \*/gmd:CI_OnlineResource[1]
<a name="urlAccess"></a> URL Access |  ./gmd:distributionInfo/\*/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/ \*/gmd:linkage/gmd:URL
<a name="urlAccessText"></a> URL Access Text |  ./gmd:distributionInfo/\*/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/ \*/gmd:description/gmd:Anchor/@xlink:href='http://inspire.ec.europa.eu/metadata-
codelist/OnLineDescriptionCode/accessPoint'
