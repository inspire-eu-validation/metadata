# IACS Datasets Keyword

**Purpose**: Test that keyword(s) for IACS data sets are provided in the metadata.

**Prerequisites**

**Test method**
* Check that LPIS datasets [Keyword CharacterString](#keywordcharacterstring) is provided with valid values
*“Land cover”*, *“LPIS”* and *“IACS”* (see Option 2).

> *Or Keyword Anchor is provided with xlink:href attribute pointing to a valid value from IACS data controlled vocabulary CodeList (see Option 1).* This option is not mentioned in the TG, not sure if it is valid.

Otherwise report [Keyword error message](#keyworderrormessage).

**Test method**
* Check that GSAA datasets [Keyword CharacterString](#keywordcharacterstring) is provided with valid values
*“Land use”*, *“GSAA”* and *“IACS”* (see Option 2).

> *Or Keyword Anchor is provided with xlink:href attribute pointing to a valid value from IACS data controlled vocabulary CodeList (see Option 1).* This option is not mentioned in the TG, not sure if it is valid.

Otherwise report [Keyword error message](#keyworderrormessage).

**Test method**
* Check that [Keyword CharacterString](#keywordcharacterstring) is provided with the value *“Common Agricultural Policy”* from GEMET (see Option 2).

> *Or Keyword Anchor is provided with xlink:href attribute pointing to a valid value from IACS data controlled vocabulary CodeList (see Option 1).* This option is not mentioned in the TG, not sure if it is valid.

Otherwise report [Keyword error message](#keyworderrormessage).

# IACS Identification information

**Purpose**: Test that Identification information for IACS data sets are provided in the metadata.

**Prerequisites**

**Test method**
* Check that the Resource title [Citation Title](#citationtitle) has a unambiguous title 
  * LPIS: name of the Member State
  * GSAA: claim year, the Member state.
>From where can we obtain de values of the Member State? For claim year maybe the check can be manually?

**Test method**
* Verify that the [Resource locator metadata](#resourcelocator) pointing to a valid url, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

**Test method**
* Check that the [Topic category](#topiccategory) is equal to *"farming"* value. Otherwise report [Topic category error message](#topiccategoryerror).
>In Anex D of TG, Land cover Value for LPIS and Land Use for GSAA is also mandatory value.

**Test method**
* Check that the [Citation Date](#citationdate) contains at least the date of the last revision and the [Citation Date Type](#citationdatetype) codeListValue is equal to *"publication"*. Otherwise report [Temporal reference error message](#temporalreferenceerror).

**Test method**
* Check *manually* that when publishing an updated a LPIS datasets in INSPIRE, the [Citation Date](#citationdate) value is updated with the value of the last revision.

**Test method**
* Check *manually* that LPIS datasets together with the updated metadata are published at least once and in the [Citation Date](#citationdate) element the value of the last revision date is within 6 month from the start of the campaign year.

**Test method**
* Check *manually* that GSAA datasets in the [Citation Date](#citationdate) element the value of the last revision date is within the campaign year.

**Test method**
* Check *manually* that GSAA datasets contains in the [Citation Date](#citationdate) element the value of the last revision date  within 6 month from the validation of the last change in the dataset

**Reference(s)**

* [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData)

**Test type**: Automated + Manual

**Notes**

<a name="option1"></a> 
> _Option 1: Using the gmx:Anchor element_
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
_Option 2: Using the gco:CharacterString element_
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
## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword error <a name="keyworderrormessage"/> | XML document '{filename}', {featureType} '{gmlid}': Keyword(s) for IACS data sets are not provided in the metadata.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry.
Topic category error <a name="topiccategoryerror"/> | XML document '{filename}', {featureType} '{gmlid}': The topic category is not equal to “farming” value
Temporal reference error <a name="temporalreferenceerror"/> | XML document '{filename}', {featureType} '{gmlid}': Citation Date does not contain at least  the date of the last revision

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression
-----------------------------------------------| -------------------------------------------------------------------------
<a name="mdKeywords"></a> MD_Keywords | gmd:descriptiveKeywords/gmd:MD_Keywords
<a name="keywordanchor"></a> ?? Keyword Anchor | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor
<a name="keywordcharacterstring"></a> Keyword CharacterString | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gco:CharacterString
<a name="citationtitle"></a> Citation Title | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:citation/gmd:CI_Citation/gmd:title/gco:CharacterString         
<a name="resourcelocator"></a> Resource locator | gmd:MD_Metadata/gmd:distributionInfo/gmd:MD_Distribution/gmd:transferOptions/gmd:MD_DigitalTransferOptions/gmd:onLine/gmd:CI_OnlineResource/gmd:linkage/gmd:URL
<a name="topiccategory"></a> Topic Category | gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:topicCategory/gmd:MD_TopicCategoryCode
<a name="citationdate"></a> Citation Date | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date
<a name="citationdatetype"></a> Citation Date Type | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
