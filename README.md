ats-metadata
============

Abstract Test Suite for the Metadata (implicit) Conformance Class.

References
* [INSPIRE Metadata Technical Guidance version 1.3](http://inspire.jrc.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
* [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards
metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)

*Note*: This ATS is in draft stage, none of the tests have an official INSPIRE MIG approval.

This Conformance Class contains the following tests:

| Identifier                                                        | Origin | Mechanical | Status   |
| ----------------------------------------------------------------- | ------ | ---------- | -------- |
| [A.01.validate](A.01.validate.md)  	    | IR     | Yes        | Draft  |
| [A.02.IR221.title](A.02.IR221.title.md)  	    | IR     | Yes        | Draft  |
| [A.03.IR222.abstract](A.03.IR222.abstract.md)  	    | IR     | Yes        | Draft  |
| [A.04.IR223.TGR1.hierarchy](A.04.IR223.TGR1.hierarchy.md)  	    | IR     | Yes        | Draft  |
| [A.05.IR223.TGR14.ds.keyword](A.05.IR223.TGR14.ds.keyword.md)  	    | IR     | Yes        | Draft  |
| [A.06.IR223.TGR15.srv.keyword](A.06.IR223.TGR15.srv.keyword.md)  	    | IR     | Yes        | Draft  |
| [A.07.IR225.TGR5.ds.identification](A.07.IR225.TGR5.ds.identification.md)  	    | IR     | Yes        | Draft  |
| [A.08.IR224.TGR3.ds.linkage](A.08.IR224.TGR3.ds.linkage.md)  	    | IR     | Yes        | Draft  |
| [A.09.IR226.TGR4.srv.linkage](A.09.IR226.TGR4.srv.linkage.md)  	    | IR     | Yes        | Draft  |
| [A.10.IR227.TGR8.ds.language](A.10.IR227.TGR8.ds.language.md)  	    | IR     | Yes        | Draft  |
| [A.11.IR231.TGR10.ds.topic](A.11.IR231.TGR10.ds.topic.md)  	    | IR     | Yes        | Draft  |
| [A.12.IR232.TGR12.srv.type](A.12.IR232.TGR12.srv.type.md)  	    | IR     | Yes        | Draft  |
| [A.13.IR241.TGR13.keyword](A.13.IR241.TGR13.keyword.md)  	    | IR     | Yes        | Draft  |
| [A.14.IR242.TGR16.vocab](A.14.IR242.TGR16.vocab.md)  	    | IR     | Yes        | Draft  |
| [A.15.IR242.TGR19.kws-in-vocab](A.15.IR242.TGR19.kws-in-vocab.md)  	    | IR     | Yes        | Draft  |
| [A.16.IR251.TGR20.ds.bounds](A.16.IR251.TGR20.ds.bounds.md)  	    | IR     | Yes        | Draft  |
| [A.17.IR261.TGR22.ds.temporal](A.17.IR261.TGR22.ds.temporal.md)  	    | IR     | Yes        | Draft  |
| [A.18.IR271.TGR26.ds.lineage](A.18.IR271.TGR26.ds.lineage.md)  	    | IR     | Yes        | Draft  |
| [A.19.IR281.TGR28.ds.conformity](A.19.IR281.TGR28.ds.conformity.md)  	    | IR     | Yes        | Draft  |
| [A.20.IR282.TGR29.ds.specification](A.20.IR282.TGR29.ds.specification.md)  	    | IR     | Yes        | Draft  |
| [A.21.IR291.TGR30.ds.limitation](A.21.IR291.TGR30.ds.limitation.md)  	    | IR     | Yes        | Draft  |
| [A.22.IR292.TGR33.ds.access](A.22.IR292.TGR33.ds.access.md)  	    | IR     | Yes        | Draft  |
| [A.23.IR2101.TGR35.contact](A.23.IR2101.TGR35.contact.md)  	    | IR     | Yes        | Draft  |
| [A.24.IR2102.TGR36.role](A.24.IR2102.TGR36.role.md)  	  | IR     | Yes        | Draft  |
| [A.25.IR2111.TGR37.md.contact](A.25.IR2111.TGR37.md.contact.md)  	    | IR     | Yes        | Draft  |
| [A.26.IR2112.TGR38.md.role](A.26.IR2112.TGR38.md.role.md)  	 | IR     | Yes        | Draft  |
| [A.27.IR2113.TGR39.date](A.27.IR2113.TGR39.date.md)    | IR     | Yes        | Draft  |

## Vocabulary

<a name="emptychar"></a>
**Empty characterstring:** iso19139 allows (if proper namespaces are available) to express any characterstring as either gco:CharacterString, gmd:Anchor or gmd:PT_FreeText. 
To check an element for having an empty characterstring, each of these representations should be considered. The PT_freetext element can be used to supply multilingual values for a characterstring. 
If PT_FreeText is used the validator should check if a value of the string is available in the main language of the document. gmx:Anchor is typically used to reference a URI on which the characterstring content is available.
The validator should resolve the URI in the gmx:Anchor to validate if the content is available.

<a name="resolve"></a>
**Resolve:** Goal is to check if a URL references to an existing document. First the url can be checked on syntactical correctness. Then a [http head operation](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html#sec9.4) 
can give an indication of the availability of the document without fully downloading it. The operation might fail due to a number of reasons: the service is 
(temporarily) unavailable, the service is protected (status 403).   



## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd


