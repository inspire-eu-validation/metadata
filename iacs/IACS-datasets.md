# IACS Datasets Keyword

**Purpose**: Test that keyword(s) for IACS data sets are provided in the metadata.

**Prerequisites**

**Test method**

* For every [MD_Keywords](#mdKeywords) element:

  * Check that at least one [Keyword Anchor](#keywordanchor) is provided with **xlink:href** attribute pointing to a valid value from [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData) (see [Option 1](#option1))
  **OR** at least one [Keyword CharacterString](#keywordcharacterstring) is provided with a valid **value** from [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData) (see [Option 2](#option2)).

  * Check that the [Citation Title](#citationtitle) has a child element with **xlink:href** attribute pointing to a valid value from [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData) (see [Option 1](#option1))
  **OR**
  at least one [Keyword CharacterString](#keywordcharacterstring) is provided with a valid **value** from [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData) (see [Option 2](#option2)).

  * Check that the [Citation Date](#citationdate) for the thesaurus is exactly '2021-06-08'.

  * Check that the [Citation Date Type](#citationdatetype) codeListValue is equal to 'publication'.

**Reference(s)**

* [IACS data controlled vocabulary CodeList](http://inspire.ec.europa.eu/metadata-codelist/IACSData)

**Test type**: Automated

**Notes**

<a name="option1"></a> 
_Option 1: Using the gmx:Anchor element_
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

??More information regarding this requirement might be found in [MIWP action](https://ies-svn.jrc.ec.europa.eu/projects/2016-5/wiki/Implementation).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="mdKeywords"></a> MD_Keywords | gmd:descriptiveKeywords/gmd:MD_Keywords
<a name="keywordanchor"></a> Keyword Anchor | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor
<a name="keywordcharacterstring"></a> Keyword CharacterString | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gco:CharacterString
<a name="citationtitle"></a> Citation Title | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="citationdate"></a> Citation Date | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:date/gco:Date
<a name="citationdatetype"></a> Citation Date Type | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date/gmd:CI_Date/gmd:dateType/gmd:CI_DateTypeCode
