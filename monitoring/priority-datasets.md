# Priority Datasets Code List

**Purpose**: Test that the priority datasets provide the corresponding keyword.

**Prerequisites**

**Test method**

* If exactly one [MD_Keywords](#mdKeywords) for priority datasets is provided:

    * Check that exactly one [Keyword Anchor](#keywordanchor) is provided with xlink:href attribute pointing to a valid value from [Priority Datasets Code List](http://inspire.ec.europa.eu/metadata-codelist/PriorityDataset) OR exactly one [Keyword CharacterString](#keywordcharacterstring) is provided with a valid value from [Priority Datasets Code List](http://inspire.ec.europa.eu/metadata-codelist/PriorityDataset).

    * Check that exactly one [MD_Keywords](#mdKeywords) element has a [Citation Title](#citationtitle) child element with value "INSPIRE priority data set".

    * Check that the [Citation Date](#citationdate) for the thesaurus is exactly '2018-04-04'.

    * Check that the [Citation Date Type](#citationdate) codeListValue is 'publication'.

* Else if more than one [MD_Keywords](#mdKeywords) for priority datasets is provided the test fails.

* Else a manual test is requested asking the user to provide the keyword with in case it is a priority dataset.

**Reference(s)**

* [MIWP action](https://ies-svn.jrc.ec.europa.eu/projects/2016-5/wiki/Implementation)
* [Priority Datasets Code List](http://inspire.ec.europa.eu/metadata-codelist/PriorityDataset)

**Test type**: Automated

**Notes**

_Option 1: Using the gmx:Anchor element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/PriorityDataset/Agglomerations-dir-2002-49" >Agglomerations (Noise Directive)</gmx:Anchor>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/PriorityDataset" >INSPIRE priority data set</gmx:Anchor>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2018-04-04</gco:Date>
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

_Option 2: Using the gco:CharacterString element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gco:CharacterString>Agglomerations (Noise Directive)</gco:CharacterString>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gco:CharacterString>INSPIRE priority data set</gco:CharacterString>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2018-04-04</gco:Date>
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

More information regarding this requirement might be found in [MIWP action](https://ies-svn.jrc.ec.europa.eu/projects/2016-5/wiki/Implementation).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keywordanchor"></a> Keyword Anchor | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor
<a name="keywordcharacterstring"></a> Keyword CharacterString | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gco:CharacterString
<a name="mdKeywords"></a> MD_Keywords | gmd:descriptiveKeywords/gmd:MD_Keywords
<a name="citationtitle"></a> Citation Title | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="citationdate"></a> Citation Date | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date