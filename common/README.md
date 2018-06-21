# 2	Common Requirements for ISO/TC 19139:2007 based INSPIRE metadata records 

This group describing metadata elements that shall be used in the same way in more than one of the mentioned Conformance Classes.

This chapter does not comprise a Conformance Class, but is referred to from the others Conformance Class chapters of the [INSPIRE Metadata](http://inspire.ec.europa.eu/id/ats/metadata/2.0) Technical Guidance based on ISO/TS 19139:2007.

*Note*: This ATS is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

## Standardization target type

 ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| | | |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007](#ref_TG_MD) |
 
 
## External document references


| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007, version 2.0](https://inspire.ec.europa.eu/sites/default/files/documents/metadata/inspire-tg-metadata-iso19139-2.0.1.pdf)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)

| ISO 639-2/B  <a name="ref_ISO_639_2"></a> | [ISO 639-2/B: Codes for the Representation of Names of Languages](http://www.loc.gov/standards/iso639-2/)


## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| C.1      | XML Schema               | [xml-schema](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/xml-schema) ||
| C.2      | Root Element              | [root-element](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/root-element) ||
| C.3      | Encoding of Code List Values               | [code-list-value](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/code-list-value) ||
| C.4      | Encoding of Free Text Values               | [free-text](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/free-text) ||
| C.5      | Language Code               | [metadata-languaje-code](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/metadata-languaje-code) ||
| C.6      | Metadata Point of Contact                | [md-point-of-contact](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/md-point-of-contact) ||
| C.7      | Metadata Date               | [md-date](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/md-date) ||
| C.8      | Resource Title               | [resource-title](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/resource-title) ||
| C.9      | Resource Abstract               | [resource-abstract](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/resource-abstract) ||
| C.10      | Responsible Organisation               | [responsible-organisation](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/responsible-organisation) ||
| C.11      | Temporal References               | [temporal-reference](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/temporal-reference) ||
| C.12      | Not More than one Date of Creation               | [max-1-date-of-creation](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/max-1-date-of-creation) ||
| C.13      | Not More than one Date of Last Revision               | [max-1-date-of-last-revision](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/max-1-date-of-last-revision) ||
| C.14      | Temporal Extent               | [temporal-extent](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/temporal-extent) ||
| C.15      | Keyword Originating CV               | [keyword-originating-cv](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/keyword-originating-cv) ||
| C.16      | Group Keywords by CV               | [group-keywords-by-cv](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/group-keywords-by-cv) ||
| C.17      | Limitations on Public Access               | [limitations-on-public-access](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/limitations-on-public-access) ||
| C.18      | Conditions for Access and Use               | [conditions-for-access-and-use](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conditions-for-access-and-use) ||
| C.19      | Geographical Bounding Box               | [bounding-box](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/bounding-box) ||
| C.20      | Conformity Statement               | [conformity](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity) ||
| C.21      | Conformity Specification               | [conformity-specification](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-specification) ||
| C.22      | Conformity Degree               | [conformity-degree](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-degree) ||

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [xml-schema](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/xml-schema) | Ready for Review |
| [root-element](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/root-element) | Ready for Review |
| [code-list-value](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/code-list-value) | Ready for Review |
| [free-text](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/free-text) | Ready for Review |
| [metadata-languaje-code](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/metadata-languaje-code) | Ready for Review |
| [md-point-of-contact](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/md-point-of-contact) | Ready for Review |
| [md-date](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/md-date) | Ready for Review |
| [resource-title](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/resource-title) | Ready for Review |
| [resource-abstract](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/resource-abstract) | Ready for Review |
| [responsible-organisation](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/responsible-organisation) | Ready for Review |
| [temporal-reference](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/temporal-reference) | Ready for Review |
| [max-1-date-of-creation](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/max-1-date-of-creation) | Ready for Review |
| [max-1-date-of-last-revision](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/max-1-date-of-last-revision) | Ready for Review |
| [temporal-extent](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/temporal-extent) | Ready for Review |
| [keyword-originating-cv](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/keyword-originating-cv) | Ready for Review |
| [group-keywords-by-cv](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/group-keywords-by-cv) | Ready for Review |
| [limitations-on-public-access](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/limitations-on-public-access) | Ready for Review |
| [conditions-for-access-and-use](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conditions-for-access-and-use) | Ready for Review |
| [bounding-box](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/bounding-box) | Ready for Review |
| [conformity](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity) | Ready for Review |
| [conformity-specification](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-specification) | Ready for Review |
| [conformity-degree](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/conformity-degree) | Ready for Review |


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

## Open issues


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
