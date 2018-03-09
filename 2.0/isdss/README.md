# Conformance class: INSPIRE Profile based on EN ISO 19115 and EN ISO 19119 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Metadata Technical Guidance based on ISO/TS 19139:2007](http://inspire.ec.europa.eu/id/ats/metadata/2.0/2.0).

## Standardization target type

 ISO/TS 19139:2007 metadata for datasets and services.

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
| [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007](#ref_TG_MD) |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007, version 2.0](http://inspire.ec.europa.eu/file/1705/download?token=iSTwpRWd)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)


## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 2.1      | Coordinate Reference System               | [crs](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/crs) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1 |
| 2.2      | Coordinate Reference System Identifiers                  | [crs-id](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/crs-id) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1  |
| 2.3      | Temporal Reference System    | [temportal-rs](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/temportal-rs) |[IR MD](#ref_IR_MD), Part B 1.4 |
| 2.4      | Spatial Representation Type | [spatial-representation-type](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/spatial-representation-type) | [IR MD](#ref_IR_MD), Part B 1.4 |
| 2.5      | Character Encoding | [character-encoding](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/character-encoding)|[IR MD](#ref_IR_MD) Part B 1.5 |
| 2.6      | Data Encoding |[data-encoding](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/data-encoding) | [IR MD](#ref_IR_MD) Part B 1.5 |
| 2.7      | Topological Consistency Descriptive Results     | [topological-consistency-quantitative-results](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/topological-consistency-quantitative-results) | |
| 2.8      | Topological Consistency Quantitative Results        | [topological-consistency-descriptive-results](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/topological-consistency-descriptive-results) |[IR MD](#ref_IR_MD) Part B 1.7 |

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [crs](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/crs)           | Ready for review  |
| [crs-id](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/crs-id)                   | Ready for review  |
| [temportal-rs](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/temportal-rs)                   | Ready for review  |
| [spatial-representation-type](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/spatial-representation-type) | Ready for review  |
| [character-encoding](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/character-encoding)                   | Ready for review  |
| [data-encoding](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/data-encoding)                 | Ready for review  |
| [topological-consistency-quantitative-results](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/topological-consistency-quantitative-results)       | Ready for review  |
| [topological-consistency-descriptive-results](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/topological-consistency-descriptive-results)                       | Ready for review  |

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

* There is no explicit Implementation Requirement in [TG MD](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/README#ref_TG_MD) for the following tests:
  * [Check title](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/title)
  * [Check abstract](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/abstract)
  * [Responsible party role](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/responsible-party-role)
  
Should these be excluded or included in the ATS? Or added as requirements in the [TG MD](#ref_TG_MD)?

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco
