# Limitations on Public Access 

**Purpose**: Test that information on the existence of some limitation of public access to spatial data sets and spatial data services is provided.

**Prerequisites**

**Test method**

* Check that at least one [Legal Constraints](#legalConstraints) element exists.

* For every [Legal Constraints](#legalConstraints) element,

    * Check that [Restriction Code](#restrictionCode) element exists. Then, 

        * Check that the attribute codeList is "http://standards.iso.org/iso/19139/resources/gmxCodelists.xml" and attribute codeListValue is "otherRestrictions".

    * Check that at least one [Anchor](#anchor) element exists. Then,

        * Check that attribute xlink:href is a URL starting with "http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/" and postfixed with one of values of code list LimitationsOnPublicAccess of the [TG MD](./README#ref_TG_MD) Annex D.1.

* If any of the checks fails, the test fails. 

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.3.6 , Req c.17


**Test type**: Automated

**Notes**

The multiplicity of [Legal Constraints](#legalConstraints) is one.

The limitations on public access based on reasons referred to Article 13 of INSPIRE Directive quoted above:

     (a) the confidentiality of the proceedings of public authorities, where such confidentiality is provided for by law;
     (b) international relations, public security or national defence;
     (c) the course of justice, the ability of any person to receive a fair trial or the ability of a public authority to conduct an enquiry of a criminal or disciplinary nature;
     (d) the confidentiality of commercial or industrial information, where such confidentiality is provided for by national or Community law to protect a legitimate economic interest, including the public interest in maintaining statistical confidentiality and tax secrecy;
     (e) intellectual property rights;
     (f) the confidentiality of personal data and/or files relating to a natural person where that person has not consented to the disclosure of the information to the public, where such confidentiality is provided for by national or Community law;
     (g) the interests or protection of any person who supplied the information requested on a voluntary basis without being under, or capable of being put under, a legal obligation to do so, unless that person has consented to the release of the information concerned;
     (h) the protection of the environment to which such information relates, such as the location of rare species.

This element shall not be the same one as used for describing conditions applying to [conditions-applying-to-access-and-use](../sds-interoperable/conditions-applying-to-access-and-use).

An example of its implementation:
     
     <gmd:MD_LegalConstraints>
          <gmd:accessConstraints>
               <gmd:MD_RestrictionCode codeList="http://standards.iso.org/iso/19139/resources/gmxCodelists.xml#MD_RestrictionCode" codeListValue="otherRestrictions" />
          </gmd:accessConstraints>
          <gmd:otherConstraints>
               <gmx:Anchor xlink:href="http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/INSPIRE_Directive_Article13_1a"> Limitation d acc s public bas  sur l article 13(1) de la directive INSPIRE
               </gmx:Anchor>
          </gmd:otherConstraints>
     </gmd:MD_LegalConstraints>
     
## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to /gmd:MD_Metadata/gmd:identificationInfo/gmd:MD_DataIdentification/gmd:resourceConstraints)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="legalConstraints"></a> Legal Constraints  | gmd:MD_LegalConstraints
<a name="restrictionCode"></a> Restriction Code | gmd:MD_LegalConstraints/gmd:accessConstraints/gmd:MD_RestrictionCode
<a name="anchor"></a> Anchor | gmd:MD_LegalConstraints/gmd:accessConstraints/gmd:otherConstraints/gmx:Anchor
