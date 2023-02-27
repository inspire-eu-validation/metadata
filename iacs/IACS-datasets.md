# IACS Keyword information

**Purpose**: Test that keyword(s) for IACS data sets are provided in the metadata.

**Prerequisites**
* For every [MD_Keywords](#mdKeywords) element:

  **Test method** 
  * Check that [Keyword Anchor](#keywordanchor) is provided with xlink:href attribute pointing to [GEMET - Concepts, common agricultural policy](https://www.eionet.europa.eu/gemet/en/concept/1600) value and at least one these values related to an INSPIRE data theme: [Land cover](http://inspire.ec.europa.eu/theme/lc) for LPIS datasets OR [Land use](http://inspire.ec.europa.eu/theme/lu) for GSAA datasets (see [Option 1](#option1)).
  
  
    OR [Keyword CharacterString](#keywordcharacterstring) is provided with *"Common Agricultural Policy"* value and at least one these values related to an INSPIRE data theme: *"Land cover"* for LPIS datasets OR *"Land use"* for GSAA datasets (see [Option 2](#option2)).
  
  **Test method**  
  * Check that [Keyword Anchor](#keywordanchor) is provided with xlink:href attribute pointing to [IACS](http://inspire.ec.europa.eu/metadata-codelist/IACSData/iacs) value and at least one these values: [LPIS](http://inspire.ec.europa.eu/metadata-codelist/IACSData/lpis) for LPIS datasets OR [GSAA](http://inspire.ec.europa.eu/metadata-codelist/IACSData/gsaa) for GSAA datasets, from [IACS data controlled vocabulary](https://inspire.ec.europa.eu/metadata-codelist/IACSData) (see [Option 1](#option1)).
    
    OR [Keyword CharacterString](#keywordcharacterstring) is provided with *"IACS"* value and at least one these values: *"LPIS"* for LPIS datasets OR *"GSAA"* for GSAA datasets (see [Option 2](#option2)).
    
    In addition: 
    * Check that the [Thesaurus Name Title](#thesaurusNameTitle) contains the xlink:href attribute pointing to [IACS data controlled vocabulary](https://inspire.ec.europa.eu/metadata-codelist/IACSData) (for [Option 1](#option1)) OR contains the *"IACS Data"* value (for [Option 2](#option2)).
    * Check that the [Thesaurus Name Date](#thesaurusNameDate) is exactly '2021-06-08'.
    * Check that the [Thesaurus Date type](#thesaurusDateType) is exactly 'publication'.

  Otherwise report [Keyword error](#keyworderrormessage) message.

# IACS Identification information

**Purpose**: Test that Identification information for IACS data sets are provided in the metadata.

**Prerequisites**

**Test method**
* Check *manually* that in case the Resource title [Citation Title](#citationtitle) is present, has a unambiguous title. [Manual message](#manualcitationtitle)
  * LPIS: name of the Member State
  * GSAA: claim year, the Member state and and if applicable, the region.

**Test method**
* Verify that the [Resource locator](#resourcelocator) metadata pointing to valid URI.
  * In case of valid URI, check manually that is pointing to a spatial data service (to a download service WMS, WFS view service, etc). It should not point to a general information web page. [Resource locator](#manualresourcelocatormessage) message. 
  * Otherwise report [brokenLink](#brokenLink). 

**Test method**
* Check that at least one [Topic category](#topiccategory) is equal to *"farming"* value. Otherwise report [Topic category error](#topiccategoryerror) message.

# IACS Temporal reference

**Test method**
* Check that the Temporal reference of the dataset contains at least the date of last revision:
	* Check that the [Citation Date](#citationdate) element contains at least a date
	* Check that for the [Citation Date Type](#citationdatetype) element the attribute codeListValue is equal to *"revision"*. Otherwise report [Temporal reference error message](#temporalreferenceerror).

**Test method**
* Check *manually* that when publishing an updated a LPIS datasets in INSPIRE, the [Citation Date](#citationdate) value is updated with the value of the last revision. [Manual Review Citation Date Updated](#manualcitationdate1)

**Test method**
* Check *manually* that LPIS datasets together with the updated metadata are published at least once and in the [Citation Date](#citationdate) element the value of the last revision date is within 6 month from the start of the campaign year. [Manual Review Citation Date](#manualcitationdate2)

**Test method**
* Check *manually* that GSAA datasets in the [Citation Date](#citationdate) element the value of the last revision date is within the campaign year. [Manual Review Citation Date Campaign](#manualcitationdate3)

**Test method**
* Check *manually* that GSAA datasets contains in the [Citation Date](#citationdate) element the value of the last revision date  within 6 month from the validation of the last change in the dataset. [Manual Review Citation Date Last Revision](#manualcitationdate4)

**Reference(s)**
* [GEMET - INSPIRE themes, Land cover](http://inspire.ec.europa.eu/theme/lc)
* [GEMET - INSPIRE themes, Land use](http://inspire.ec.europa.eu/theme/lu)
* [GEMET - Concepts, Common agricultural policy](https://www.eionet.europa.eu/gemet/en/concept/1600)
* [IACS data controlled vocabulary](http://inspire.ec.europa.eu/metadata-codelist/IACSData)

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
<a name="citationdate"></a> Citation Date | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date | 0..1 
<a name="citationdatetype"></a> Citation Date Type | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode/@codeListValue |  0..1

