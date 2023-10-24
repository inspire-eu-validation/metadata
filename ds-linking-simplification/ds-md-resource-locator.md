# Data set Metadata Resource Locator

**Purpose**: Test that at least two Resource Locator elements are present in the data set metadata pointing to the URLs where the related network services can be contacted. Additionally, test the presence of <gmd:protocol> and <gmd:applicationProfile> elements, paired with the defined codelist values from the INSPIRE Registry. 

**Prerequisites**: TG Requirement 1.8 of INSPIRE MD TG expresses the obligation to provide online access, if available, to the described data set or data set series. Furthermore, the INSPIRE legal framework requires that data sets are made available through View and Download services, which in turn implies that at least two locators need to be expressed in the data set metadata: one for a View Service and one for a Download Service.

**Test method**:

Check that at least the following two Resource Locator elements are provided:

**Resource Locator for View Service linkage**

* Check that a [Resource Locator](#ResourceLocator) element is present and contains the following sub-elements:
  * element [`gmd:URL`](#ResourceLocatorURL) that point to the response of the Get View Service Metadata request of the View Service.
    * If the URL doesn't work the test is failed ([Broken link](#brokenLink) message).
    * If the URL works and contains the string `request=GetCapabilities&service=WMS` the test is passed.
    * If the URL works and does not contain the string `request=GetCapabilities&service=WMS`, check manually that it points to the response of the Get View Service Metadata request of the View Service ([Resource locator URL](#resourcelocatorurlcheck) message). 
  * element `gmd:protocol`:
    * if the element is encoded using `gmx:Anchor`, check that the attribute [`gmx:Anchor/@xlink:href`](#protocolanchor) points to the URI of one of the values in [Protocol values](https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue) codelist.
    * if the element is encoded using `gco:CharacterString`, check that the text value of [`gco:CharacterString`](#protocolstring) matches the label of one of the values in [Protocol values](https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue) codelist, in the language of the metadata language. See the related [note regarding the labels](#labelnote).
  * element `gmd:applicationProfile`:
    * if the element is encoded using `gmx:Anchor`, check that the attribute [`gmx:Anchor/@xlink:href`](#appproanchor) points to the [View Service](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view) value of the [Spatial data service type](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/) codelist.
    * if the element is encoded using `gco:CharacterString`, check that the text value of [`gco:CharacterString`](#appprostring) matches the label of the [View Service](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view) value of the [Spatial data service type](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/) codelist, in the language of the metadata language.


**Resource Locator for Download Service linkage**

* Check that a [Resource Locator](#ResourceLocator) element is present and contains the following sub-elements:
  * element [`gmd:URL`](#ResourceLocatorURL) that point to the response of the Get Download Service Metadata request of the Download Service.
    * If the URL doesn't work the test is failed ([Broken link](#brokenLink) message).
    * If the URL works and contains the string `request=GetCapabilities&service=WFS` the test is passed.
    * If the URL works and does not contain the string `request=GetCapabilities&service=WFS`, check manually that it points to the response of the Get Download Service Metadata request of the Download Service ([Resource locator URL](#resourcelocatorurlcheck) message). 
  * element `gmd:protocol`:
    * if the element is encoded using `gmx:Anchor`, check that the attribute [`gmx:Anchor/@xlink:href`](#protocolanchor) points to the URI of one of the values in [Protocol values](https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue) codelist.
    * if the element is encoded using `gco:CharacterString`, check that the text value of [`gco:CharacterString`](#protocolstring) matches the label of one of the values in [Protocol values](https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue) codelist, in the language of the metadata language. See the related [note regarding the labels](#labelnote).
  * element `gmd:applicationProfile`:
    * if the element is encoded using `gmx:Anchor`, check that the attribute [`gmx:Anchor/@xlink:href`](#appproanchor) points to the [Download Service](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download) value of the [Spatial data service type](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/) codelist.
    * if the element is encoded using `gco:CharacterString`, check that the text value of [`gco:CharacterString`](#appprostring) matches the label of the [Download Service](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download) value of the [Spatial data service type](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/) codelist, in the language of the metadata language.



**Test type**: Automated + Manual

**Notes**

_Examples:_

Encoding examples of the Resource Locator element can be found in the [Annex A: Examples](https://github.com/INSPIRE-MIF/gp-data-service-linking-simplification/blob/main/good-practice/data-service-linking-simplification-spec.md#annex-a-examples-) of the Data Service Linking Simplification: Good Practice guidelines.

<a name="labelnote"></a>_Labels of _Protocol values_ codelist_:

Since there is a mismatch between INSPIRE labels and OGC preferred labels ([See related issue](https://github.com/INSPIRE-MIF/gp-data-service-linking-simplification/issues/68)), the related test is relaxed and all the values are considered valid by the Validator (e.g. "OGC Web Map Service" and "wms"). The test is also case-insensitive (e.g. "WMS" is considered as valid).



## Messages (automated)

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
Broken link <a name="brokenLink"/> | XML document '{filename}', {featureType} '{gmlid}': The property '{propertyName}' has a value '{value}' that cannot be retrieved using HTTP.


## Messages (manual)

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
Resource locator URL<a name="resourcelocatorurlcheck"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that the Resource locator URL points to the response of the Get View Service Metadata request of the View Service.


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity  
---------------------------------------------------------- | ------------------------------------- | -------------
<a name="ResourceLocator"></a> Resource Locator | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource |  0..*
<a name="ResourceLocatorURL"></a> Resource Locator URL | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL |  1
<a name="protocolanchor"></a> Protocol Anchor | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:protocol/gmx:Anchor/@xlink:href |  0..1
<a name="protocolstring"></a> Protocol CharacterString | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:protocol/gco:CharacterString |  0..1
<a name="appproanchor"></a> Application Profile Anchor | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:applicationProfile/gmx:Anchor/@xlink:href |  0..1
<a name="appprostring"></a> Application Profile CharacterString | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:applicationProfile/gco:CharacterString |  0..1