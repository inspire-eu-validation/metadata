ats-metadata
============

Abstract Test Suite for the Metadata (implicit) Conformance Class.

References
* [INSPIRE Metadata Technical Guidance version 1.3](http://inspire.jrc.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
* [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards
metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)

*Note*: This ATS is in ready for review stage, none of the tests have an official INSPIRE MIG approval.

This Conformance Class contains the following tests:

| Identifier                                                        | Origin | Mechanical | Status   |
| ----------------------------------------------------------------- | ------ | ---------- | -------- |
| [A.01.IR3.validate](A.01.validate.md)  	    | IR     | Yes        | Ready for review  |
| [A.02.IRB11.title](A.02.IRB21.title.md)  	    | IR     | Yes        | Ready for review  |
| [A.03.IRB12.abstract](A.03.IRB22.abstract.md)  	    | IR     | Yes        | Ready for review  |
| [A.04.IRB13.TGR1.hierarchy](A.04.IRB23.TGR1.hierarchy.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.05.IRB31.TGR14.ds.keyword](A.05.IRB23.TGR14.ds.keyword.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.06.IRB31.TGR15.srv.keyword](A.06.IRB23.TGR15.srv.keyword.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.07.IRB15.TGR5.ds.identification](A.07.IRB25.TGR5.ds.identification.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.08.IRB14.TGR3.ds.linkage](A.08.IRB24.TGR3.ds.linkage.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.09.IRB14.TGR4.srv.linkage](A.09.IRB26.TGR4.srv.linkage.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.09.IRB16.TGR7.srv.identification](A.09.IRB26.TGR7.srv.identification.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.10.IRB17.TGR8.ds.language](A.10.IRB27.TGR8.ds.language.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.11.IRB21.TGR10.ds.topic](A.11.IRB31.TGR10.ds.topic.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.12.IRB22.TGR12.srv.type](A.12.IRB32.TGR12.srv.type.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.13.IRB31.TGR13.keyword](A.13.IRB41.TGR13.keyword.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.14.IRB32.TGR16.vocab](A.14.IRB42.TGR16.vocab.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.15.IRB32.TGR19.kws-in-vocab](A.15.IRB42.TGR19.kws-in-vocab.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.16.IRB41.TGR20.ds.bounds](A.16.IRB51.TGR20.ds.bounds.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.17.IRB51.TGR22.ds.temporal](A.17.IRB61.TGR22.ds.temporal.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.18.IRB61.TGR26.ds.lineage](A.18.IRB71.TGR26.ds.lineage.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.18.IRB62.TGR27.ds.resolution](A.18.TGR27.ds.resolution.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.19.IRB71.TGR28.ds.conformity](A.19.IRB81.TGR28.ds.conformity.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.20.IRB72.TGR29.ds.specification](A.20.IRB82.TGR29.ds.specification.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.21.IRB81.TGR30.ds.limitation.md](A.21.IRB91.TGR30.ds.limitation.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.22.IRB82.TGR33.ds.access](A.22.IRB92.TGR33.ds.access.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.23.IRB91.TGR35.contact.md](A.23.IRB101.TGR35.contact.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.24.IRB92.TGR36.role](A.24.IRB102.TGR36.role.md)  	  | IR/TG     | Yes        | Ready for review  |
| [A.25.IRB101.TGR37.md.contact](A.25.IRB111.TGR37.md.contact.md)  	    | IR/TG     | Yes        | Ready for review  |
| [A.26.ISO.TGR38.md.role](A.26.IRB112.TGR38.md.role.md)  	 | IR/TG     | Yes        | Ready for review  |
| [A.27.IRB103.TGR39.language](A.27.IRB113.TGR39.language.md)    | IR/TG     | Yes        | Ready for review  |
| [A.28.IRB102.metadata.date](A.28.IRB112.metadata.date.md)    | IR/TG     | Yes        | Ready for review  |

Some additional metadata tests are available at [ats-interoperability-metadata](https://github.com/inspire-eu-validation/ats-interoperability-metadata). These tests are seperated from above because they have a different timeline for implementation.

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

## References
<a name="IR"></a>
* [Implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32008R1205&from=EN)
<a name="TG"></a>
* [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
<a name="REG"></a>
* [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
<a name="ISO19115"></a>
* [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
<a name="ISO19119"></a>
* [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
