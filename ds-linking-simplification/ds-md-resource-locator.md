# Data set Metadata Resource Locator

**Purpose**: Test that at least two Resource Locator elements are present in the data set metadata pointing to the URLs where the related network services can be contacted. Additionally, test the presence of <gmd:protocol> and <gmd:applicationProfile> elements, paired with the defined codelist values from the INSPIRE Registry. 

**Prerequisites**: TG Requirement 1.8 of INSPIRE MD TG expresses the obligation to provide online access, if available, to the described data set or data set series. Furthermore, the INSPIRE legal framework requires that data sets are made available through View and Download services, which in turn implies that at least two locators need to be expressed in the data set metadata: one for a View Service and one for a Download Service.

**Test method**:

* Check that at least the following two Resource Locator elements are provided:

  **Resource Locator for View Service linkage**
  
A	A Resource Locator to an INSPIRE View Service providing view access to the described data set or data set series SHALL be given. It SHALL be encoded using the /gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource element.
B	The element gmd:URL SHALL point to the response of the Get View Service Metadata request of the View Service
C	The element gmd:protocol SHALL be present.
D	If the element gmd:protocol is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to the URI of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue.
E	If the element gmd:protocol is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue in the language of the metadata language.
F	The element gmd:applicationProfile SHALL be present.
G	If the element gmd:applicationProfile is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view.
H	If the element gmd:applicationProfile is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/view in the language of the metadata language.
  
  
    
  **Resource Locator for Download Service linkage**
  
A	A Resource Locator to an INSPIRE Download Service providing download access to the described data set or data set series SHALL be given. It SHALL be encoded using the /gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource element.
B	The element gmd:URL SHALL point to the response of the Get Download Service Metadata request of the Download Service
C	The element gmd:protocol SHALL be present.
D	If the element gmd:protocol is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to the URI of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue.
E	If the element gmd:protocol is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of one of the values in https://inspire.ec.europa.eu/metadata-codelist/ProtocolValue in the language of the metadata language.
F	The element gmd:applicationProfile SHALL be present.
G	If the element gmd:applicationProfile is encoded using gmx:Anchor, the attribute gmx:Anchor/@xlink:href SHALL point to https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download.
H	If the element gmd:applicationProfile is encoded using gco:CharacterString, the text value of gco:CharacterString SHALL match the label of https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType/download in the language of the metadata language.
  




**Test type**: Automated + Manual

**Notes**

<a name="option1"></a> 
_Encoding Option 1: Using the gmx:Anchor element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/IACSData/lpis">LPIS</gmx:Anchor>
        </gmd:keyword>
        <gmd:keyword>
            <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/IACSData/iacs">IACS</gmx:Anchor>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/IACSData">IACS Data</gmx:Anchor>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2021-06-08</gco:Date>
                        </gmd:date>
                        <gmd:dateType>
                            <gmd:CI_DateTypeCode codeList="http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication">publication</gmd:CI_DateTypeCode>
                        </gmd:dateType>
                    </gmd:CI_Date>
                </gmd:date>
            </gmd:CI_Citation>
        </gmd:thesaurusName>
    </gmd:MD_Keywords>
</gmd:descriptiveKeywords>
```

<a name="option2"></a> 
_Encoding Option 2: Using the gco:CharacterString element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gco:CharacterString>LPIS</gco:CharacterString>
        </gmd:keyword>
        <gmd:keyword>
            <gco:CharacterString>IACS</gco:CharacterString>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gco:CharacterString>IACS Data</gco:CharacterString>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2021-06-08</gco:Date>
                        </gmd:date>
                        <gmd:dateType>
                            <gmd:CI_DateTypeCode codeList="http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/ML_gmxCodelists.xml#CI_DateTypeCode" codeListValue="publication">publication</gmd:CI_DateTypeCode>
                        </gmd:dateType>
                    </gmd:CI_Date>
                </gmd:date>
            </gmd:CI_Citation>
        </gmd:thesaurusName>
    </gmd:MD_Keywords>
</gmd:descriptiveKeywords>

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
<a name="mdKeywords"></a> MD_Keywords | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor |  0..1
<a name="keywordanchor"></a> Keyword Anchor | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor | 1 
<a name="keywordcharacterstring"></a> Keyword CharacterString | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gco:CharacterString | 1 
<a name="thesaurusNameTitle"></a> Thesaurus Name Title | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title | 0..1 
<a name="thesaurusNameDate"></a> Thesaurus Name Date | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date | 0..1 
<a name="thesaurusDateType"></a> Thesaurus Date Type | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode | 0..1
<a name="citationtitle"></a> Citation Title | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:title/gco:CharacterString | 0..1 
<a name="resourcelocator"></a> Resource locator | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL | 0..*  
<a name="topiccategory"></a> Topic Category | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:topicCategory/gmd:MD_TopicCategoryCode | 1..* for datasets and dataset series 0 for services 
<a name="citationdate"></a> Citation Date | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date OR gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:DateTime | 0..1 
<a name="citationdatetype"></a> Citation Date Type | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode/@codeListValue |  0..1

