ats-metadata
============

Abstract Test Suite for the Metadata (implicit) Conformance Class.

*Note*: This ATS is in ready for review stage, none of the tests have an official INSPIRE MIG approval.

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
| 1      | hierachyLevel mandated               | [A.04.IR01.IR02.hierarchy](A.04.IR01.IR02.hierarchy.md) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1 |
| 2      | MD_ScopeCode values                  | [A.04.IR01.IR02.hierarchy](A.04.IR01.IR02.hierarchy.md) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1  |
| 3      | Resource Locator for data linkage    | [A.08.IR03.ds.linkage](A.08.IR03.ds.linkage.md) |[IR MD](#ref_IR_MD), Part B 1.4 |
| 4      | Resource Locator for service linkage | [A.09.IR04.srv.linkage](A.09.IR04.srv.linkage.md) | [IR MD](#ref_IR_MD), Part B 1.4 |
| 5      | Unique Resource Identifier code is mandatory | [A.07.IR05.IR06.ds.identification](A.07.IR05.IR06.ds.identification.md)|[IR MD](#ref_IR_MD) Part B 1.5 |
| 6      | Use RS_Identifier if URI codeSpace provided |[A.07.IR05.IR06.ds.identification](A.07.IR05.IR06.ds.identification.md) | [IR MD](#ref_IR_MD) Part B 1.5 |
| 7      | operatesOn as a reference     | [A.29.IR07.srv.identification](A.29.IR07.srv.identification.md)| [IR MD](#ref_IR_MD) Part B 1.6 |
| 8      | Resource language is mandated        | [A.10.IR08.IR09.ds.language](A.10.IR08.IR09.ds.language.md) |[IR MD](#ref_IR_MD) Part B 1.7 |
| 9      | ISO 19139 codes used for language    | [A.10.IR08.IR09.ds.language](A.10.IR08.IR09.ds.language.md) | [IR MD](#ref_IR_MD) Part B 1.7 |
| 10     | Use MD_TopicCategoryCode values in topicCategory |[A.11.IR10.IR11.ds.topic](A.11.IR10.IR11.ds.topic.md) |[IR MD](#ref_IR_MD) Part B 2.1 |
| 11     | Use language neutral name in topicCategory | [A.11.IR10.IR11.ds.topic](A.11.IR10.IR11.ds.topic.md) |[IR MD](#ref_IR_MD) Part B 2.1|
| 12     | Use language neutral name for serviceType | [A.12.IR12.srv.type](A.12.IR12.srv.type.md) |[IR MD](#ref_IR_MD) Part B 2.2 |
| 13     | Provide at least one keyword         |[A.13.IR13.keyword](A.13.IR13.keyword.md) |[IR MD](#ref_IR_MD) Part B 3.1 |
| 14     | Use theme for the only dataset keyword | [A.05.IR14.ds.keyword](A.05.IR14.ds.keyword.md) |[IR MD](#ref_IR_MD) Part B 3.1  |
| 15     | Use category for the inly service keyword | [A.06.IR15.srv.keyword](A.06.IR15.srv.keyword.md) |[IR MD](#ref_IR_MD) Part B 1.5, Article 4, part D  |
| 16     | Use citation for other controlled keywords | [A.14.IR16.IR17.IR18.vocab](A.14.IR16.IR17.IR18.vocab.md) |[IR MD](#ref_IR_MD) Part B  3.2|
| 17     | Cite the originating controlled vocabulary |[A.14.IR16.IR17.IR18.vocab](A.14.IR16.IR17.IR18.vocab.md) |[IR MD](#ref_IR_MD) Part B 3.2|
| 18     | At least title and date for controlled vocabulary citations |[A.14.IR16.IR17.IR18.vocab](A.14.IR16.IR17.IR18.vocab.md) |[IR MD](#ref_IR_MD) Part B 3.2 |
| 19     | Group keywords from the same controlled vocabulary | [A.15.IR19.kws-in-vocab](A.15.IR19.kws-in-vocab.md) | [IR MD](#ref_IR_MD) Part B 3.2|
| 20     | Use the minimum geographic bounding box  | [A.16.IR20.IR21.ds.bounds](A.16.IR20.IR21.ds.bounds.md) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 21     | At least two decimals for coordinates | [A.16.IR20.IR21.ds.bounds](A.16.IR20.IR21.ds.bounds.md) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 22     | Use at least one of INSPIRE temporal reference types | [A.17.IR22.IR23.ds.temporal](A.17.IR22.IR23.ds.temporal.md) | [IR MD](#ref_IR_MD) Part B. 5.1|
| 23     | Use at least one ISO 19115 temporal reference types |[A.17.IR22.IR23.ds.temporal](A.17.IR22.IR23.ds.temporal.md) |[IR MD](#ref_IR_MD) Part B. 5.1 |
| 24     | Gregorian calendar and ISO 8601 date as defaults | not testable | [IR MD](#ref_IR_MD) Part B 5 |
| 25     | Single creation date mandatory       | [A.31.IR25.resource.creation.date](A.31.IR25.resource.creation.date) | [IR MD](#ref_IR_MD) Part B 5.4|
| 26     | Only one dataQualityInfo             | [A.18.IR26.lineage](A.18.IR26.lineage.md) |[IR MD](#ref_IR_MD) Part B. 2.6 |
| 27     | Spatial resolution as either scale or ground sample distance | [A.30.IR27.ds.spatial.resolution](A.30.IR27.ds.spatial.resolution.md) | [IR MD](#ref_IR_MD) Part B. 2.6|
| 28     | Degree of conformity mandatory       |[A.19.IR28.ds.conformity](A.19.IR28.ds.conformity.md) | [IR MD](#ref_IR_MD) Part B. 2.8|
| 29     | Use DQ_DomainConsistency for spec. conformity |[A.20.IR29.ds.specification](A.20.IR29.ds.specification.md) | [IR MD](#ref_IR_MD) Part B. 7.2|
| 30     | Declare both limitations on "public access" and "constraints on access and use" |[A.21.IR30.IR31.IR31.ds.public.access](A.21.IR30.IR31.IR31.ds.public.access.md) | [INSPIRE](#ref_INSPIRE), Article 13|
| 31     | At least one MD_Contraints even if no limitations |[A.21.IR30.IR31.IR31.ds.public.access](A.21.IR30.IR31.IR31.ds.public.access.md) | - |
| 32     | Expressing limitations on public access |[A.21.IR30.IR31.IR31.ds.public.access](A.21.IR30.IR31.IR31.ds.public.access.md) | - |
| 33     | No conditions and unknown conditions |[A.22.IR33.IR34.ds.access](A.22.IR33.IR34.ds.access.md) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 34     | Terms and conditions either embedded or linked |[A.22.IR33.IR34.ds.access](A.22.IR33.IR34.ds.access.md) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 35     | Responsible organisation name and email |[A.23.IR35.IR36.responsible.party.contact.info](A.23.IR35.IR36.responsible.party.contact.info.md) |[IR MD](#ref_IR_MD) Part B. 3.5 |
| 36     | MD_DataIdentification and SV_ServiceIdentification for responsible party info |[A.23.IR35.IR36.responsible.party.contact.info](A.23.IR35.IR36.responsible.party.contact.info.md) | [IR MD](#ref_IR_MD) Part B. 3.5 |
| 37     | Metadata point of contact organisation name and email | [A.25.IR37.md.contact](A.25.IR37.md.contact.md) |[IR MD](#ref_IR_MD) Part B. 10.1 |
| 38     | Metadata point of contact role code 'pointOfContact'| [A.26.IR38.md.contact.role](A.26.IR38.md.contact.role.md) | - |
| 39     | Metadata language is mandatory | [A.26.IR39.language](A.26.IR39.language.md) | [IR MD](#ref_IR_MD) Part B. 10.3|

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [A.01.validate](A.01.validate.md)  	                              | Ready for review  |
| [A.04.IR01.IR02.hierarchy](A.04.IR01.IR02.hierarchy.md)           | Ready for review  |
| [A.05.IR14.ds.keyword](A.05.IR14.ds.keyword.md)                   | Ready for review  |
| [A.06.IR15.srv.keyword](A.06.IR15.srv.keyword.md)                   | Ready for review  |
| [A.07.IR05.IR06.ds.identification](A.07.IR05.IR06.ds.identification.md) | Ready for review  |
| [A.08.IR03.ds.linkage](A.08.IR03.ds.linkage.md)                   | Ready for review  |
| [A.09.IR04.srv.linkage](A.09.IR04.srv.linkage.md)                 | Ready for review  |
| [A.10.IR08.IR09.ds.language](A.10.IR08.IR09.ds.language.md)       | Ready for review  |
| [A.11.IR10.ds.topic](A.11.IR10.ds.topic.md)                       | Ready for review  |
| [A.12.IR12.srv.type](A.12.IR12.srv.type.md)                       | Ready for review  |
| [A.13.IR13.keyword](A.13.IR13.keyword.md)                         | Ready for review  |
| [A.14.IR16.vocab](A.14.IR16.vocab.md)                             | Ready for review  |
| [A.15.IR19.kws-in-vocab](A.15.IR19.kws-in-vocab.md)               | Ready for review  |
| [A.16.IR20.IR21.ds.bounds](A.16.IR20.IR21.ds.bounds.md)           | Ready for review  |
| [A.17.IR22.IR23.ds.temporal](A.17.IR22.IR23.ds.temporal.md)       | Ready for review  |
| [A.18.IR26.ds.lineage](A.18.IR26.ds.lineage.md)                   | Ready for review  |
| [A.19.IR28.ds.conformity](A.19.IR28.ds.conformity.md)             | Ready for review  |
| [A.20.IR29.ds.specification](A.20.IR29.ds.specification.md)       | Ready for review  |
| [A.21.IR30.IR31.IR32.ds.public.access.md](A.21.IR30.IR31.IR32.ds.public.access.md) | Ready for review  |
| [A.22.IR33.IR34.ds.access.use](A.22.IR33.IR34.ds.access.use.md)   | Ready for review  |
| [A.23.IR35.responsible.party.contact.info.md](A.23.IR35.responsible.party.contact.info.md) | Ready for review  |
| [A.25.IR37.md.contact](A.25.IR37.md.contact.md)                   | Ready for review  |
| [A.26.IR38.md.contact.role](A.26.IR38.md.contact.role.md)         | Ready for review  |
| [A.27.IR39.language](A.27.IR39.language.md)                       | Ready for review  |
| [A.29.IR07.srv.identification](A.29.IR07.srv.identification.md)   | Ready for review  
| [A.30.IR27.ds.spatial.resolution](A.30.IR27.ds.spatial.resolution.md) | Ready for review  |
| [A.31.IR25.resource.creation.date](A.31.IR25.resource.creation.date) | missing |

Some additional metadata tests are available at [ats-interoperability-metadata](https://github.com/inspire-eu-validation/ats-interoperability-metadata). These tests are separated from above because they have a different timeline for implementation.

## Vocabulary

<a name="emptychar"></a>
**Empty characterstring:** iso19139 allows (if proper namespaces are available) to express any characterstring as either gco:CharacterString, gmd:Anchor or gmd:PT_FreeText.
To check an element for having an empty characterstring, each of these representations should be considered. The PT_freetext element can be used to supply multilingual values for a characterstring.
If only PT_FreeText is used the validator should check if a value of the string is available in the main language of the document. gmx:Anchor is typically used to reference a URI on which additional information is available.
The validator could resolve the URI in the gmx:Anchor to validate if that content is available.

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
  <gmd:keyword>
    <gmd:PT_FreeText>
       <gmd:textGroup>
         <gmd:LocalisedCharacterString locale="#EN">Addresses</gmd:LocalisedCharacterString>
       </gmd:textGroup>
    </gmd:PT_FreeText>
  </gmd:keyword>
```

<a name="resolve"></a>
**Resolve:** Goal is to check if a URL references an existing document. First the URL can be checked on syntactical correctness. Then a [http head operation](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.4)
can give an indication of the availability of the document without fully downloading it. The operation might fail due to a number of reasons: the service is
(temporarily) unavailable, the service is protected (status 403).

## Open questions

* There is no explicit Implementation Requirement in [TG MD](README.md#ref_TG_MD) for the following tests:
  * [A.02.title](A.02.title.md)
  * [A.03.abstract](A.03.abstract.md)
  * [A.24.responsible.party.role](A.24.responsible.party.role.md)
  * [A.28.md.creation.date](A.28.md.creation.date.md)

Should these be excluded or included in the ATS? Or added as requirements in the [TG MD](#ref_TG_MD)?

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
