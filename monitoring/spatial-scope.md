# Spatial Scope Keyword

**Purpose**: Test that the spatial scope of the data set or data set series is provided.

**Prerequisites**

**Test method**

* If exactly one [MD_Keywords](#mdKeywords) for spatial scope is provided:

    * Check that exactly one [Keyword Anchor](#keywordanchor) is provided with xlink:href attribute pointing to a valid value from [Spatial Scope Code List](http://inspire.ec.europa.eu/metadata-codelist/SpatialScope) (see _Option 1_) OR exactly one [Keyword CharacterString](#keywordcharacterstring) is provided with a valid value from [Spatial Scope Code List](http://inspire.ec.europa.eu/metadata-codelist/SpatialScope) (see _Option 2_).

    * Check that exactly one [MD_Keywords](#mdKeywords) element has a [Citation Title](#citationtitle) child element with value "Spatial scope".

    * Check that the [Citation Date](#citationdate) for the thesaurus is exactly '2019-05-22'.

* Else if more than one [MD_Keywords](#mdKeywords) for spatial scope is provided the test fails.

* Else a manual test is requested asking the user to provide the keyword with the spatial scope in case it is _National_ or _Regional_.

**Reference(s)**

* [Spatial Scope Code List Implementation guidance and support](https://webgate.ec.europa.eu/fpfis/wikis/display/InspireMIG/Spatial+scope+code+list)
* [Spatial Scope Code List in the INSPIRE Registry](http://inspire.ec.europa.eu/metadata-codelist/SpatialScope)

**Test type**: Automated

**Notes**

#_Option 1: Using the gmx:Anchor element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/SpatialScope/national">National</gmx:Anchor>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/SpatialScope">Spatial scope</gmx:Anchor>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2019-05-22</gco:Date>
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

#_Option 2: Using the gco:CharacterString element_
```
<gmd:descriptiveKeywords>
    <gmd:MD_Keywords>
        <gmd:keyword>
            <gco:CharacterString>National</gco:CharacterString>
        </gmd:keyword>
        <gmd:thesaurusName>
            <gmd:CI_Citation>
                <gmd:title>
                    <gco:CharacterString>Spatial scope</gco:CharacterString>
                </gmd:title>
                <gmd:date>
                    <gmd:CI_Date>
                        <gmd:date>
                            <gco:Date>2019-05-22</gco:Date>
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

More information regarding this requirement might be found in [MIWP action](https://webgate.ec.europa.eu/fpfis/wikis/display/InspireMIG/Spatial+scope+code+list).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="keywordanchor"></a> Keyword Anchor | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gmx:Anchor
<a name="keywordcharacterstring"></a> Keyword CharacterString | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:keyword/gco:CharacterString
<a name="mdKeywords"></a> MD_Keywords | gmd:descriptiveKeywords/gmd:MD_Keywords
<a name="citationtitle"></a> Citation Title | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:title
<a name="citationdate"></a> Citation Date | gmd:descriptiveKeywords/gmd:MD_Keywords/gmd:thesaurusName/gmd:CI_Citation/gmd:date
