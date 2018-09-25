# Limitations on Public Sccess 

**Purpose**: Provide information on the existence of some limitation of public access to spatial data sets and spatial data services.

**Prerequisites**

**Test method**

Check the information about the existence and its reasons in the limitations of public access to the data set. To do this, the element [Legal Constraints](#legalConstraints) will be used.
This limitations on public access based on reasons referred to Article 13 of INSPIRE Directive quoted above:

     (a) the confidentiality of the proceedings of public authorities, where such confidentiality is provided for by law;
     (b) international relations, public security or national defence;
     (c) the course of justice, the ability of any person to receive a fair trial or the ability of a public authority to conduct an enquiry of a criminal or disciplinary nature;
     (d) the confidentiality of commercial or industrial information, where such confidentiality is provided for by national or Community law to protect a legitimate economic interest, including the public interest in maintaining statistical confidentiality and tax secrecy;
     (e) intellectual property rights;
     (f) the confidentiality of personal data and/or files relating to a natural person where that person has not consented to the disclosure of the information to the public, where such confidentiality is provided for by national or Community law;
     (g) the interests or protection of any person who supplied the information requested on a voluntary basis without being under, or capable of being put under, a legal obligation to do so, unless that person has consented to the release of the information concerned;
     (h) the protection of the environment to which such information relates, such as the location of rare species.

The MD_LegalConstraints element shall include a combination of:

* An [Restriction Code](#restrictionCode) element will be given with a value from the "otherRestrictions" [Code List Value](#codeListValue)
* And at least one instance [Other Constraints](#otherConstraints) that points to one of the values in the code list for [Limitations On Public Access](#http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/). In the case of no access limitations, this element must point to the value of the "noLimitations" code list.

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD), 2.3.6 , Req c.17


**Test type**: Automated

**Notes**

This element shall not be the same one as used for describing conditions applying to [conditions-applying-to-access-and-use](#http://inspire.ec.europa.eu/id/ats/metadata/2.0/sds-interoperable/conditions-applying-to-access-and-use).

An example of its implementation:
     <gmd:MD_LegalConstraints>
          <gmd:accessConstraints>
               <gmd:MD_RestrictionCode codeList="http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_RestrictionCode" codeListValue="otherRestrictions" />
          </gmd:accessConstraints>
          <gmd:otherConstraints>
               <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1a"> Limitation d’accés public basé sur l’article 13(1) de la directive INSPIRE
               </gmx:Anchor>
          </gmd:otherConstraints>
     </gmd:MD_LegalConstraints>

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/metadata/2.0/common/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints  | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints
<a name="restrictionCode"></a> Restriction Code | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:accessConstraints/gmd:MD_RestrictionCode/@codeListValue
<a name="codeListValue"></a> Code List Value | doc("http://standards.iso.org/iso/19139/resources/gmxCodelists.xml")/gmx:CodeListDictionary[@gml:id='MD_RestrictionCode']//gml:identifier/text()
<a name="otherConstraints"></a> Other Constraints | ./gmd:identificationInfo/\*/gmd:resourceConstraints/gmd:MD_LegalConstraints/gmd:otherConstraints/gmx:Anchor/@xlink:href='http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1a'





