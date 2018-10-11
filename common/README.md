# Common requirements for XML Encoded INSPIRE metadata

This group describes metadata elements that shall be used in the same way in all the Conformance Classes.

This set of requirements does not comprise a Conformance Class, but it is referred to from the others Conformance Classes of the implementation of "INSPIRE dataset and service metadata based on ISO/TS 19139:2007" [INSPIRE Metadata](../README.md) based on the corresponding technical guidance [TG MD](#ref_TG_MD).

*Note*: It is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

## Standardization target type

 ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

*There is not direct dependencies for this set of requirements.*

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

 *There is not indirect dependencies for this set of requirements.*
 
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
| C.1      | XML Schema | [xml-schema](./xml-schema.md) ||
| C.2      | Root Element | [root-element](./root-element.md) ||
| C.3      | Encoding of Code List Values | [code-list-value](./code-list-value.md) ||
| C.4      | Encoding of Free Text Values | [free-text](./free-text.md) ||
| C.5      | Language Code | [metadata-language-code](./metadata-language-code.md) ||
| C.6      | Metadata Point of Contact  | [md-point-of-contact](./md-point-of-contact.md) ||
| C.7      | Metadata Date | [md-date](./md-date) ||
| C.8      | Resource Title | [resource-title](./resource-title.md) ||
| C.9      | Resource Abstract | [resource-abstract](./resource-abstract.md) ||
| C.10      | Responsible Organisation | [responsible-organisation](./responsible-organisation.md) ||
| C.11      | Temporal References | [temporal-reference](./temporal-reference.md) ||
| C.12      | Not More than one Date of Creation | [max-1-date-of-creation](./max-1-date-of-creation.md) ||
| C.13      | Not More than one Date of Last Revision | [max-1-date-of-last-revision](./max-1-date-of-last-revision.md) ||
| C.14      | Temporal Extent | [temporal-extent](./temporal-extent.md) ||
| C.15      | Keyword Originating CV | [keyword-originating-cv](./keyword-originating-cv.md) ||
| C.16      | Group Keywords by CV | [group-keywords-by-cv](./group-keywords-by-cv.md) ||
| C.17      | Limitations on Public Access | [limitations-on-public-access](./limitations-on-public-access.md) ||
| C.18      | Conditions for Access and Use | [conditions-for-access-and-use](./conditions-for-access-and-use.md) ||
| C.19      | Geographical Bounding Box | [bounding-box](./bounding-box.md) ||
| C.20      | Conformity Statement | [conformity](./conformity.md) ||
| C.21      | Conformity Specification | [conformity-specification](./conformity-specification.md) ||
| C.22      | Conformity Degree | [conformity-degree](./conformity-degree.md) ||

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [xml-schema](./xml-schema.md) | Ready for Review |
| [root-element](./root-element.md) | Ready for Review |
| [code-list-value](./code-list-value.md) | Ready for Review |
| [free-text](./free-text.md) | Ready for Review |
| [metadata-language-code](./metadata-language-code.md) | Ready for Review |
| [md-point-of-contact](./md-point-of-contact.md) | Ready for Review |
| [md-date](./md-date.md) | Ready for Review |
| [resource-title](./resource-title.md) | Ready for Review |
| [resource-abstract](./resource-abstract.md) | Ready for Review |
| [responsible-organisation](./responsible-organisation.md) | Ready for Review |
| [temporal-reference](./temporal-reference.md) | Ready for Review |
| [max-1-date-of-creation](./max-1-date-of-creation.md) | Ready for Review |
| [max-1-date-of-last-revision](./max-1-date-of-last-revision.md) | Ready for Review |
| [temporal-extent](./temporal-extent.md) | Ready for Review |
| [keyword-originating-cv](./keyword-originating-cv.md) | Ready for Review |
| [group-keywords-by-cv](./group-keywords-by-cv.md) | Ready for Review |
| [limitations-on-public-access](./limitations-on-public-access.md) | Ready for Review |
| [conditions-for-access-and-use](./conditions-for-access-and-use.md) | Ready for Review |
| [bounding-box](./bounding-box.md) | Ready for Review |
| [conformity](./conformity.md) | Ready for Review |
| [conformity-specification](./conformity-specification.md) | Ready for Review |
| [conformity-degree](./conformity-degree.md) | Ready for Review |


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
