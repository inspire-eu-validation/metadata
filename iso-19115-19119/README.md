# Conformance class: INSPIRE Profile based on EN ISO 19115 and EN ISO 19119 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Metadata Technical Guidance](http://inspire.ec.europa.eu/id/ats/metadata/1.3).

## Standardization target type

ISO 19115/19119 metadata record

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ISO 19115](#ref_ISO_19115) | n/a | n/a |
| [ISO 19119](#ref_ISO_19119) | n/a | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119](#ref_TG_MD) | [XML encoding](http://inspire.ec.europa.eu/id/ats/metadata/1.3/xml-encoding) | XML document (MD_Metadata) |  `encoding` = `ISO/TS 19139` or `CSW ISO AP 1.0.0` |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119, version 1.3](http://inspire.jrc.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)


## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | hierachyLevel mandated               | [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1 |
| 2      | MD_ScopeCode values                  | [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1  |
| 3      | Resource Locator for data linkage    | [Dataset linkage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-linkage) |[IR MD](#ref_IR_MD), Part B 1.4 |
| 4      | Resource Locator for service linkage | [Service linkage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-linkage) | [IR MD](#ref_IR_MD), Part B 1.4 |
| 5      | Unique Resource Identifier code is mandatory | [Dataset identification](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-identification)|[IR MD](#ref_IR_MD) Part B 1.5 |
| 6      | Use RS_Identifier if URI codeSpace provided |[Dataset identification](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-identification) | [IR MD](#ref_IR_MD) Part B 1.5 |
| 7      | operatesOn as a reference     | [Coupled resource](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/coupled-resource) | |
| 8      | Resource language is mandated        | [Dataset language](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-language) |[IR MD](#ref_IR_MD) Part B 1.7 |
| 9      | ISO 19139 codes used for language    | [Dataset language](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-language) | [IR MD](#ref_IR_MD) Part B 1.7 |
| 10     | Use MD_TopicCategoryCode values in topicCategory |[Dataset topic](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-topic) |[IR MD](#ref_IR_MD) Part B 2.1 |
| 11     | Use language neutral name in topicCategory | [Dataset topic](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-topic) |[IR MD](#ref_IR_MD) Part B 2.1|
| 12     | Use language neutral name for serviceType | [Service type](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-type) |[IR MD](#ref_IR_MD) Part B 2.2 |
| 13     | Provide at least one keyword         |[Keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keyword) |[IR MD](#ref_IR_MD) Part B 3.1 |
| 14     | Use theme for the only dataset keyword | [Dataset keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-keyword) |[IR MD](#ref_IR_MD) Part B 3.1  |
| 15     | Provide at least one service category keyword | [Service keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-keyword) |[IR MD](#ref_IR_MD) Part B 1.5, Article 4, part D  |
| 16     | Use citation for other controlled keywords | [Vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/vocabulary) |[IR MD](#ref_IR_MD) Part B  3.2|
| 17     | Cite the originating controlled vocabulary |[Vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/vocabulary) |[IR MD](#ref_IR_MD) Part B 3.2|
| 18     | At least title and date for controlled vocabulary citations |[Vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/vocabulary) |[IR MD](#ref_IR_MD) Part B 3.2 |
| 19     | Group keywords from the same controlled vocabulary | [Keywords in vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keywords-in-vocabulary) | [IR MD](#ref_IR_MD) Part B 3.2|
| 20     | Use the minimum geographic bounding box  | [Geographic bounding box](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/geographic-bounding-box) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 21     | At least two decimals for coordinates | [Geographic bounding box](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/geographic-bounding-box) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 22     | Use at least one of INSPIRE temporal reference types | [Ds temporal](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-temporal) | [IR MD](#ref_IR_MD) Part B. 5.1|
| 23     | Use at least one ISO 19115 temporal reference types |[Ds temporal](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-temporal) |[IR MD](#ref_IR_MD) Part B. 5.1 |
| 24     | Gregorian calendar and ISO 8601 date as defaults | nothing to test, always true | [IR MD](#ref_IR_MD) Part B 5 |
| 25     | Single creation date mandatory       | [Resource creation date](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/resource-creation-date) | [IR MD](#ref_IR_MD) Part B 5.4|
| 26     | Only one dataQualityInfo             | [Lineage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/lineage) |[IR MD](#ref_IR_MD) Part B. 2.6 |
| 27     | Spatial resolution as either scale or ground sample distance | [Ds spatial resolution](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-spatial-resolution) | [IR MD](#ref_IR_MD) Part B. 2.6|
| 28     | Degree of conformity mandatory       |[Dataset conformity](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-conformity) | [IR MD](#ref_IR_MD) Part B. 2.8|
| 29     | Use DQ_DomainConsistency for spec. conformity |[Ds specification](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-specification) | [IR MD](#ref_IR_MD) Part B. 7.2|
| 30     | Declare both limitations on "public access" and "constraints on access and use" |[Dataset public access](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-public-access) | [INSPIRE](#ref_INSPIRE), Article 13|
| 31     | At least one MD_Contraints even if no limitations |[Dataset public access](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-public-access) | n/a |
| 32     | Expressing limitations on public access |[Dataset public access](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-public-access) | n/a |
| 33     | No conditions and unknown conditions |[Dataset access use](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-access-use) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 34     | Terms and conditions either embedded or linked |[Dataset access use](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-access-use) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 35     | Responsible organisation name and email |[Responsible party contact info](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/responsible-party-contact-info) |[IR MD](#ref_IR_MD) Part B. 3.5 |
| 36     | MD_DataIdentification and SV_ServiceIdentification for responsible party info |[Responsible party contact info](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/responsible-party-contact-info) | [IR MD](#ref_IR_MD) Part B. 3.5 |
| 37     | Metadata point of contact organisation name and email | [Metadata contact](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/md-contact) |[IR MD](#ref_IR_MD) Part B. 10.1 |
| 38     | Metadata point of contact role code 'pointOfContact'| [Metadata contact role](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/md-contact-role) | n/a |
| 39     | Metadata language is mandatory | [Language](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/language) | [IR MD](#ref_IR_MD) Part B. 10.3|

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Hierarchy](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/hierarchy)           | Ready for review  |
| [Dataset keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-keyword)                   | Ready for review  |
| [Service keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-keyword)                   | Ready for review  |
| [Dataset identification](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-identification) | Ready for review  |
| [Dataset linkage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-linkage)                   | Ready for review  |
| [Service linkage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-linkage)                 | Ready for review  |
| [Dataset language](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-language)       | Ready for review  |
| [Dataset topic](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-topic)                       | Ready for review  |
| [Service type](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/srv-type)                       | Ready for review  |
| [Keyword](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keyword)                         | Ready for review  |
| [Vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/vocabulary)                             | Ready for review  |
| [Keywords in vocabulary](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/keywords-in-vocabulary)               | Ready for review  |
| [Geographic bounding box](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/geographic-bounding-box)           | Ready for review  |
| [Dataset temporal](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-temporal)       | Ready for review  |
| [Lineage](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/lineage)                   | Ready for review  |
| [Dataset conformity](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-conformity)             | Ready for review  |
| [Dataset specification](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-specification)       | Ready for review  |
| [Dataset public access](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-public-access) | Ready for review  |
| [Dataset access use](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-access-use)   | Ready for review  |
| [Responsible party contact info](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/responsible-party-contact-info) | Ready for review  |
| [Metadata contact](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/md-contact)                   | Ready for review  |
| [Metadata contact role](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/md-contact-role)         | Ready for review  |
| [Language](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/language)                       | Ready for review  |
| [Dataset spatial resolution](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/ds-spatial-resolution) | Ready for review  |
| [Resource creation date](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/resource-creation-date) | Ready for review |

Some additional metadata tests are available in the [conformance class 'Metadata for interoperability'](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/Metadata-for-interoperability). These tests are separated from above because they have a different timeline for implementation.

## Vocabulary

<a name="emptychar"></a>
**Empty characterstring:** ISO/TS 19139 allows (if proper namespaces are available) to express any characterstring as either gco:CharacterString, gmd:Anchor or gmd:PT_FreeText.

To check an element for having an empty CharacterString, each of these representations should be considered. The PT_FreeText element can be used to supply multilingual values for a CharacterString.
If only PT_FreeText is used the validator should check if a value of the string is available in the main language of the document. gmx:Anchor is typically used to reference a URI on which additional information is available.
The validator could retrieve the resource at the URI in the gmx:Anchor to validate, if that content is available.

Some examples for valid string content:
```
  <gmd:keyword>
    <gco:CharacterString>Addresses</gco:CharacterString>
  </gmd:keyword>
```
  or
```
  <gmd:keyword>
    <gmx:Anchor xlink:href="http://www.eionet.europa.eu/gemet/en/inspire-theme/5297/">Addresses</gmx:Anchor>
  </gmd:keyword>
```
  or
```  
<abstract xsi:type="PT_FreeText_PropertyType">
  <gco:CharacterString>Brief narrative summary of the content of the
resource</gco:CharacterString>
  <!--== Alternative values ==-->
  <PT_FreeText>
    <textGroup>
      <LocalisedCharacterString locale="locale-fr">Résumé succint du contenu du jeu de données</LocalisedCharacterString>
    </textGroup>
    <textGroup>
      <LocalisedCharacterString locale="locale=it">
        Succinta descrizione del contenuto della risorsa
      </LocalisedCharacterString>
    </textGroup>
  </PT_FreeText>
</abstract>
```

## Open questions

* There is no explicit Implementation Requirement in [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/README#ref_TG_MD) for the following tests:
  * [Check title](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/title)
  * [Check abstract](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/abstract)
  * [Responsible party role](http://inspire.ec.europa.eu/id/ats/metadata/1.3/iso-19115-19119/responsible-party-role)
  
Should these be excluded or included in the ATS? Or added as requirements in the [TG MD](#ref_TG_MD)?

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
