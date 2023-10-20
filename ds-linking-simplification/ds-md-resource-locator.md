# Data set Metadata Resource Locator

**Purpose**: Test that at least two Resource Locator elements are present in the data set metadata pointing to the URLs where the related network services can be contacted. Additionally, test the presence of <gmd:protocol> and <gmd:applicationProfile> elements, paired with the defined codelist values from the INSPIRE Registry. 

**Prerequisites**: TG Requirement 1.8 of INSPIRE MD TG expresses the obligation to provide online access, if available, to the described data set or data set series. Furthermore, the INSPIRE legal framework requires that data sets are made available through View and Download services, which in turn implies that at least two locators need to be expressed in the data set metadata: one for a View Service and one for a Download Service.

**Test method**:

Check that at least the following two Resource Locator elements are provided:

**Resource Locator for View Service linkage**

* Check that a [Resource Locator](#ResourceLocator) element is present and contains the following sub-elements:
  * element gmd:URL that point to the response of the Get View Service Metadata request of the View Service
  * element gmd:protocol:
    * if the element gmd:protocol is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to the URI of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue.
    * If the element gmd:protocol is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue in the language of the metadata language.
  * element gmd:applicationProfile:
    * if the element gmd:applicationProfile is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view.
    * if the element gmd:applicationProfile is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view in the language of the metadata language.


**Resource Locator for Download Service linkage**

* Check that a [Resource Locator](#ResourceLocator) element is present and contains the following sub-elements:
  * element gmd:URL that point to the response of the Get Download Service Metadata  request of the Download Service
  * element gmd:protocol:
    * if the element gmd:protocol is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to the URI of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue.
    * If the element gmd:protocol is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue in the language of the metadata language.
  * element gmd:applicationProfile:
    * if the element gmd:applicationProfile is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download.
    * if the element gmd:applicationProfile is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download in the language of the metadata language.



**Test type**: Automated + Manual

**Notes**

* Examples of Resource Locator for INSPIRE View Service

<a name="option1"></a> 
_Encoding Option 1: Resource Locator to a "Get View Service Metadata" operation - WMS GetCapabilities_

```xml
<gmd:transferOptions>
  <gmd:MD_DigitalTransferOptions>
      [...]
    <gmd:onLine>
      <gmd:CI_OnlineResource>
        <gmd:linkage>
          <gmd:URL>http://.../wms?request=GetCapabilities&amp;service=WMS&amp;version=1.3.0</gmd:URL>
        </gmd:linkage>
        <gmd:protocol>
          <gmx:Anchor xlink:href="http://www.opengis.net/def/serviceType/ogc/wms">OGC Web Map Service</gmx:Anchor>
        </gmd:protocol>
        <gmd:applicationProfile>
          <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view">View Service</gmx:Anchor>
        </gmd:applicationProfile>
        <gmd:name>
          <gco:CharacterString>INSPIRE WMS</gco:CharacterString>
        </gmd:name>
      </gmd:CI_OnlineResource>
    </gmd:onLine>
      [...]
  </gmd:MD_DigitalTransferOptions>
</gmd:transferOptions>
```

* Examples of Resource Locator for INSPIRE Download Service

<a name="option2"></a> 
_Encoding Option 2: Resource Locator to a "Get Download Service Metadata" operation - ATOM topfeed_
```
<gmd:transferOptions>
  <gmd:MD_DigitalTransferOptions>
      [...]
    <gmd:onLine>
      <gmd:CI_OnlineResource>
        <gmd:linkage>
          <gmd:URL>http://.../atom/INSPIRE_DW_dataset_2021</gmd:URL>
        </gmd:linkage>
        <gmd:protocol>
          <gmx:Anchor xlink:href="https://tools.ietf.org/html/rfc4287">ATOM Syndication Format</gmx:Anchor>
        </gmd:protocol>
        <gmd:applicationProfile>
          <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download">Download Service</gmx:Anchor>
        </gmd:applicationProfile>
        <gmd:name>
          <gco:CharacterString>INSPIRE Download Service (ATOM)</gco:CharacterString>
        </gmd:name>
      </gmd:CI_OnlineResource>
    </gmd:onLine>
      [...]
  </gmd:MD_DigitalTransferOptions>
</gmd:transferOptions>

```
## Messages (automated)

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword error <a name="keyworderrormessage"/> | XML document '{filename}', {featureType} '{gmlid}': Keyword(s) '{value/value or value}' for IACS data sets are not provided in the metadata.
Broken link <a name="brokenLink"/> | XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.
Topic category error <a name="topiccategoryerror"/> | XML document '{filename}', {featureType} '{gmlid}': The topic category is not equal to “farming” value.
Temporal reference error <a name="temporalreferenceerror"/> | XML document '{filename}', {featureType} '{gmlid}': Citation Date does not contain at least  the date of the last revision

## Messages (manual)

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
Resource locator <a name="manualresourcelocatormessage"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that the Resource locator metadata pointing to a spatial data service.
Manual Review Citation title <a name="manualcitationtitle"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that the property '{property}' has a unambiguous title. For LPIS datasets, the name of the Member State and for GSAA datasets the claim year, the Member state and if applicable, the region.
Manual Review Citation Date Updated <a name="manualcitationdate1"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that when publishing an updated a LPIS datasets in INSPIRE, the Citation Date value is updated with the value of the last revision.
Manual Review Citation Date <a name="manualcitationdate2"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that LPIS datasets together with the updated metadata are published at least once and in the Citation Date element, the value of the last revision date is within 6 month from the start of the campaign year. 
Manual Review Citation Date Campaign <a name="manualcitationdate3"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that GSAA datasets in the Citation Date element, the value of the last revision date is within the campaign year.
Manual Review Citation Date Last Revision <a name="manualcitationdate4"/> | XML document '{filename}', {featureType} '{gmlid}': Please review that GSAA datasets contains in the Citation Date element, the value of the last revision date  within 6 month from the validation of the last change in the dataset.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity  
---------------------------------------------------------- | ------------------------------------- | -------------
<a name="ResourceLocator"></a> Resource Locator | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource |  0..1

