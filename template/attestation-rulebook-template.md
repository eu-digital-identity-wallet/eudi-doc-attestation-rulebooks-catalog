| Version | Date | Description |
|---------|------------|------------|
| 1.0 | 24-06-2025 | First version |
| 1.1 | 20-08-2025 | Allowing private names specific to the attestation type for JSON claims; adding requirements to specify whether a claim is selectively disclosable. |
| 1.2 | 07-10-2025 | Fixing markdown issues; adding requirement to Chapter 4 regarding the need to specify whether an attestation is device-bound or non device-bound. |
| 1.3 | 02-12-2025 | Add complete change history; include the optional ``cryptographically_bound_to`` attribute specified in ARB_28; removed recommendation to define a JSON schema for SD-JWT VC-based attestations. |

# Attestation Rulebook for attestations of type  *ADD THE ATTESTATION TYPE HERE*

*Provide information about the author(s) of this Rulebook in the following form:*

* Author(s):
    * [NAME SURNAME, AFFILIATION]
    * [NAME SURNAME, AFFILIATION]
* Previous Authors
    * [NAME SURNAME, AFFILIATION (versions)]
    * [NAME SURNAME, AFFILIATION (versions)]

*Provide versioning information about the Rulebook in the following form:*

| Version | Date | Description |
|---------|------------|------------|
| [VERSION NUMBER] | [PUBLICATION DATE] | [DESCRIPTION OR LINK TO THE CHANGELOG] |
| [VERSION NUMBER] | [PUBLICATION DATE] | [DESCRIPTION OR LINK TO THE CHANGELOG] |

*Provide a contact email address and/or a link to an issue tracking system that can be used for
providing feedback, e.g.:*

**Feedback:**

* <https://example.com/tracker>

## 1 Introduction

### 1.1 Document scope and purpose

*Provide a concise explanation of the purpose of the defined attestation type, explicitly stating
why it exists and what its primary objective is within the context of the EUDI Wallet ecosystem*

[RULEBOOK AUTHOR TO DEFINE]

### 1.2 Document structure

*Provide a brief overview of the Rulebook's sections and their purpose. The main
sections of the Rulebook SHOULD be*

* Chapter 2, which describes the attestation attributes and metadata in an
encoding-independent manner.
* Chapter 3, which specifies how the attestation
attributes and metadata are encoded in case the attestation complies with [ISO/IEC
18013-5] and/or [SD-JWT VC] and/or [W3C VCDM v2.0]. Each encoding SHALL be specified in a separate section, or even in a separate chapter.
* Chapter 4, which specifies attestation usage.
* Chapter 5, which defines how trust anchors for attestation verification can be obtained.
* Chapter 6, which defines attestation revocation mechanisms.
* Chapter 7, which provides compliance information.

### 1.3 Key words

*The following are the recommended keywords. Modify if necessary*

This document uses the capitalised key words 'SHALL', 'SHOULD' and 'MAY' as
specified in [RFC 2119], i.e., to indicate requirements, recommendations and
options specified in this document.

In addition, 'must' (non-capitalised) is used to indicate an external
constraint, i.e., a requirement that is not mandated by this document, but, for
instance, by an external document. The word 'can' indicates a capability,
whereas other words, such as 'will', and 'is' or 'are' are intended as
statements of fact.

### 1.4 Terminology

*It is recommended to use the terminology defined in Annex 1 of ARF. For example
the following text can be used.*

This document uses the terminology specified in Annex 1 of the ARF.

## 2 Attestation attributes and metadata

### Chapter overview and requirements

*This chapter is used for defining all attributes that an
attestation of the defined type may contain. In this section
the attributes SHALL be defined in an encoding-independent manner (see ARB_06 in [Topic 12]).
Each attribute can be mandatory, optional, or conditional
and this SHALL be specified in the corresponding section (see ARB_09 in [Topic 12]).*

*When attributes are defined, referring to attributes that
already exist in a catalogue of attestation attributes
SHOULD be considered (see ARB_07 in [Topic 12]).*

*[Topic 12] of Annex 2 of the ARF defines the following High-Level Requirements with
respect to the Attestation Rulebooks:*

**Requirements for QEAA**

* An attribute as meant in Annex V point a)  of the [European Digital Identity Regulation]
SHALL be included (see ARB_11 in [Topic 12]). See also section 2.1.
* One or more attributes or metadata representing the set of data meant in Annex
V point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_13 in [Topic 12])
* One or more attributes representing the set of data meant in Annex V point c)  
of the [European Digital Identity Regulation] SHALL be included (see ARB_16 in [Topic 12]).
* One or more attributes or metadata representing the set of data meant in Annex V point e)
of the [European Digital Identity Regulation] SHALL be included (see ARB_18 in [Topic 12]).
* One or more attributes or metadata representing the location meant in Annex V point h)
of the [European Digital Identity Regulation] SHALL be included. This location SHALL
indicate at least the URL at which a machine-readable version of the trust anchor to be
used for verifying the QEAA can be found or looked up (see ARB_20 in [Topic 12]).

**Requirements for PuB-EAA**

* Αn attribute as meant in  Annex VII point a) of the [European Digital Identity Regulation]
SHALL be included (see ARB_11 in [Topic 12]). See also section 2.1.
* Οne or more attributes or metadata representing the set of data meant in Annex
 VII point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_14 in [Topic 12]).
* Οne or more attributes representing the set of data meant in Annex VII point c)
of the [European Digital Identity Regulation] SHALL be included (see ARB_16 in [Topic 12]).
* Οne or more attributes or metadata representing the set of data meant in Annex VII point e)
of the [European Digital Identity Regulation] SHALL be included (see ARB_18 in [Topic 12]).
* one or more attributes or metadata representing the location meant in Annex VII point h)
of the [European Digital Identity Regulation] SHALL be included. This location SHALL
indicate at least the URL at which a machine-readable version of the qualified
certificate that signed the PuB-EAA can be found or looked up. (see ARB_20 in [Topic 12])

**Requirements for non-qualified EAA**

* An attribute indicating that the attestation is an EAA should be included (see ARB_12 in [Topic 12]).
See also section 2.1.
* Οne or more attributes or metadata representing the set of data meant in Annex
V point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_15 in [Topic 12]).
* Οne or more attributes representing the set of data meant in Annex V point c) of the
[European Digital Identity Regulation] SHOULD be included (see ARB_17 in [Topic 12])
* Οne or more attributes representing the set of data meant in Annex V point e) of
the [European Digital Identity Regulation] SHOULD be defined (see ARB_19 in [Topic 12]).
* Οne or more attributes or metadata representing the location at which a machine-readable
version of the trust anchor to be used for verifying the EAA can be found or
looked up SHOULD be defined. What this location indicates precisely is dependent
on the nature of the mechanism used for distributing trust anchors, detailed in section
5 (see ARB_21 in [Topic 12])

### 2.1 Introduction

*In this section, briefly introduce the overall design and purpose of the specific attestation type
defined by this Rulebook, including key decisions regarding its attributes and
legal categorization.*

*According to Annex V point a) and  Annex VII point a) of the [European Digital Identity Regulation]
an indication, at least in a form suitable for automated processing, that the attestation
has been issued as a QEAA or Pub-EAA SHALL be defined. Similarly, according to ARB_12
of [Topic 12] of Annex 2 of the ARF a similar indication SHOULD be defined for non-qualified EAA.

This document defines the attribute "attestation_legal_category" which SHALL have
the value "QEAA" or "PuB-EAA" or "non-qualified-EAA".*

*In the following subsections 2.1 - 2.7 define in an encoding independent manner all
mandatory, optional, and conditional attributes and metadata. In each subsection
provide a table of the following form:*

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a unique attribute identifier* | *Briefly describe the semantic of this attribute*|*Provide a type, e.g., integer, string, boolean, date.*|*Give an example value* |

*NOTE Data identifiers should be unambiguous, machine-readable where possible, and
avoid natural-language ambiguities.*

### 2.2 Mandatory attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

### 2.3 Optional attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

### 2.4 Conditional attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

### 2.5 Mandatory metadata

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

### 2.6 Optional metadata

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

### 2.7 Conditional metadata

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a value* | *Provide succinct text*|*Provide a value*|*Provide a value* |

# 3 Attestation encoding

## 3.1 ISO/IEC 18013-5-compliant encoding

*If the attestation type supports the the format specified in ISO/IEC 18013-5,
then in this section the  ISO/IEC 18013-5-compliant encoding of attributes and metadata
should be defined.*

*It is noted that (see ARB_02 in [Topic 12]) the Schema Provider SHALL analyse whether it must
be possible for a User to present that type of attestation when the Wallet Unit
and the Relying Party are in proximity and attestations are presented without
using the internet. If so,the attestations must be issued in the ISO/IEC 18013-5-compliant
mdoc format.*

*Furthermore, in this section a document type SHALL be defined, which SHALL be
unique within the scope of the EUDI Wallet ecosystem (see ARB_05 in [Topic 12]).*

[RULEBOOK AUTHOR TO DEFINE THE ATTESTATION TYPE]

*Provide a list of available encoding formats and their specifications (e.g., encoding, maximum lengths,
date formats, etc). For example:*

* tstr, uint, bstr, bool and tdate are CDDL representation types defined in
  [RFC 8610].
    * Regarding type tstr: this document confirms that, as specified in [RFC
    8949], a tstr SHALL be encoded in UTF-8 and SHALL support the full Unicode
    range.
    * All attributes having encoding type tstr SHALL have a maximum length of
    150 characters.
    * This document specifies full-date as full-date = #6.1004(tstr), where tag
    1004 is specified in [RFC 8943].
    * In accordance with [RFC 8949], section 3.4.1, a tdate attribute SHALL
    contain a date-time string as specified in [RFC 3339]. In accordance with
    [RFC 8943], a full-date attribute SHALL contain a full-date string as
    specified in [RFC 3339].
    * The following requirements apply to the representation of dates in
    attributes, unless otherwise indicated:
        * Fractions of seconds SHALL NOT be used;
        * A local offset from UTC SHALL NOT be used; the time-offset defined in
        [RFC 3339] SHALL be to "Z".
    * [RFC 8949], section 4.2, describes four rules for canonical CBOR. Three of
    those rules SHALL be implemented for all CBOR structures, as
    follows:
        * integers (major types 0 and 1) SHALL be as small as possible;
        * the expression of the length in a bstr, tstr, array or map SHALL be as
        short as possible;
        * indefinite-length items SHALL be made into definite-length items.

*This section should include a table the data identifier specified in
Chapter 2,  the corresponding attribute identifier to be used in
presentation requests and responses according to [ISO/IEC 18013-5] and the encoding
of each attribute.*

*Additionally, the following rules should be followed:*

* When specifying new attributes, existing conventions
for attribute identifier values and attribute syntaxes SHOULD
be considered (see ARB_07 in [Topic 12]).
* Each attribute SHALL be defined within an attribute namespace.
    * An attribute namespace
SHALL fully define the identifier, the syntax, and the semantics of each attribute
within that namespace.
    * An attribute namespace SHALL have an identifier that is
unique within the scope of the EUDI Wallet ecosystem, and each attribute
identifier SHALL be unique within that namespace (see ARB_06a in [Topic 12])
    * A domestic namespace MAY defined
to specify attributes that are specific to this Rulebook and are not included in
the applicable EU-wide or sectoral namespace (see ARB_10 in [Topic 12]).

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Namespace**|
|------------------------|--------------|------------------|------------------|
| family_name | family_name | tstr | com.example.att.1|

*The corresponding entry for the "attestation_legal_category" attribute defined
in Section 2.1 SHALL be:*

| **Data Identifier** | **Attribute identifier** | **Encoding format** |**Namespace**|
|------------------------|--------------|------------------|------------------|
| attestation_legal_category | attestation_legal_category | tstr |com.example.att.1|

Finally, illustrative examples SHALL be included.

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF FULL OR PARTIAL mDOC OF THE ATTESTATION]

[RULEBOOK AUTHOR TO PROVIDE THE ATTRIBUTES AND THEIR VALUES INCLUDED IN THE EXAMPLE]

### 3.2 SD-JWT VC-based encoding

*If the attestation type supports the format specified in "SD-JWT-based Verifiable
Credentials (SD-JWT VC)", then in this section the SD-JWT VC-compliant encoding
of attributes and metadata SHALL be defined. It SHALL be ensured that the attestations
comply with the 'SD-JWT VCs' profile specified in [HAIP] (see ARB_01b in [Topic 12]).*

*It is noted that a Schema Provider MAY specify in the Attestation
Rulebook that that type of attestation must be issued in the [SD-JWT VC]-compliant
format, provided the [SD-JWT VC] specification has been approved by an EU standardisation
body or by the European Digital Identity Cooperation Group established pursuant to
Article 46e(1) of the [European Digital Identity Regulation] (see ARB_03 in [Topic 12]).*

*In this section, a Verifiable Credential Type (`vct`) SHALL be defined,
which SHALL be unique within the scope of the EUDI Wallet ecosystem (see ARB_05 in [Topic 12]).*

[RULEBOOK AUTHOR TO DEFINE THE ATTESTATION TYPE]

*Additionally, when specifying new attributes, existing conventions
for attribute identifier values and attribute syntaxes SHOULD
be considered (see ARB_07 in [Topic 12]).*

*Rulebook authors SHALL ensure that each claim name is either

* included in the IANA registry for JWT claims,
* is a Public Name as defined in [RFC 7519], or
* or is a Private Name specific to the attestation type. (see ARB_06b in [Topic 12]).*

*For all claims (i.e., all top-level properties, all nested properties, and all array entries),
the Rulebook SHALL specify whether an Attestation Provider MUST, MAY, or MUST NOT make that
claim selectively disclosable (see ARB_30 in [Topic 12]).*

*Rulebook authors SHOULD consider defining a Type Metadata Document for the attestation type
specified in the Rulebook, as defined in Chapter 6 of [SD-JWT VC]. If such a document is defined,
it SHOULD contain the Claim Selective Disclosure Metadata (defined in Section 9.3 of [SD-JWT VC])
for each of the claims, in order to specify if that claim is selectively disclosable (see ARB_31
in [Topic 12]).*

*IANA-registered claims should be presented in table that
includes their data identifier, attribute identifier,
encoding format, and reference or note. For example,*

| **Data Identifier** | **Attribute identifier** | **Encoding format** |**Reference/Notes** |**Disclosable**|
|-------------------- |--------------------------|---------------------|--------------------|---------------|
| family_name | family_name | string | Section 5.1 of [OIDC] | MUST |

*A similar table should be used for Public Names and for Private Names specific
to the attestation type defined in this document. For
example:*

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |**Disclosable**|
|---------------------|--------------------------|---------------------|-----------|---------------|
| trust_anchor | trust_anchor | string | The trust anchor defined in Section 5 | MUST NOT |

*The corresponding entry for the "attestation_legal_category" attribute defined
in Section 2.1 SHALL be:*

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |**Disclosable**|
|---------------------|--------------------------|---------------------|-----------|---------------|
| attestation_legal_category | attestation_legal_category | string | Defined in Attestation Rulebook template |MUST NOT|

Finally, illustrative examples SHALL be included.

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF THE JWT CLAIM SET USED BY THE PROVIDER]

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF THE ISSUED SD-JWT (IN base64 ENCODING)]

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF A HUMAN READABLE VERSION OF THE SD-JWT PAYLOAD
AND A DESCRIPTION OF THE DISCLOSURES INCLUDED IN THE EXAMPLE]

### 3.3 W3C Verifiable Credentials Data Model-based encoding

*If the attestation type supports the the format specified in W3C Verifiable Credentials
Data Model, then in this section the  corresponding encoding  of attributes and
metadata should be defined.*

*It is noted that only a a non-qualified EAA can use this format (see ARB_01a in [Topic 12])*

*Tables similar to the ones specified in section 4 SHALL be defined.*

*This section SHALL reference one or more documents specifying in detail how a
Relying Party can request attributes from a such an attestation, and how a User
can selectively disclose attributes from such an attestation. Moreover, these
referenced documents SHALL be approved by an EU standardisation body or by the European
Digital Identity Cooperation Group established pursuant to Article 46e(1) of the
[European Digital Identity Regulation] (see ARB_04 in [Topic 12]).*

*Finally, illustrative examples SHALL be included.*

[RULEBOOK AUTHOR TO PROVIDE HUMAN READABLE EXAMPLE OF THE ISSUED ATTESTATION]

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF THE PROOF TYPE]

## 4 Attestation usage

*Briefly describe the primary use cases or scenarios for which this attestation
type is intended*

*Additionally, in this section it SHOULD  be specified whether a Relying Party receiving the attestation
must request and verify a PID (see ARB_27 in [Topic 12]). Also beyond PID verification,
it SHOULD be defined what other key obligations does a Relying Party have when processing
this attestation type (e.g., signature verification, freshness checks)*

*Furthermore, provide potential presentation requirements, e.g., are there specific
requirements for how this attestation must be presented (e.g., online, offline, specific protocols)?"*

*Specify whether an attestation of this type must be device-bound or non device-bound, see ARB_34 in [Topic 12]*

*If an attestation of this type is device-bound, include the optional attribute  ``cryptographically_bound_to`` (as defined in ARB_28) in [Section 2.5](#26-optional-metadata). If present in an Attestation Rulebook, the identifier for this attribute SHALL be "`cryptographically_bound_to" for both ISO/IEC 18013-5 and SD-JWT VC-compliant attestations, and its contents SHALL be tstr or string (as applicable) containing an attestation type or vct (see ARB_05).*

*Finally, in this section information about potential transactional data
SHALL be defined; see [Topic 20] of Annex 2 of the ARF.*

## 5 Trust anchors

*Mechanisms for the provision of a trust anchor that SHALL
be used for the verification of an attestation SHALL be defined in this section.*

*It is noted that the ARF specifies the following for QEAAs and Pub-EAAs:*

> To do this for [...] QEAAs the Relying Party Instance uses a trust anchor of
the Provider obtained from a Trusted List. Note that the PID Provider or QEAA
Provider may use an intermediate signing certificate to sign the PID or
attestation, and use the trust anchor to sign the signing certificate, instead
of signing the PID or attestation directly with the trust anchor.
>
> For PuB-EAAs, the Relying Party Instance verifies a PuB-EAA by first
verifying the signature of the PuB-EAA Provider over the PuB-EAA, using the
PuB-EAA Provider certificate issued by a QTSP. Subsequently, the Relying Party
Instance verifies the signature over this certificate, using the corresponding
trust anchor from the QTSP Trusted List. Note that both the PuB-EAA Provider
and the QTSP may use an intermediate signing certificate. All other things
being equal, the verification of a PuB-EAA will therefore involve one or more
extra certificates, compared to the verification of a PID or QEAA.

*For non-qualified EAA in this section it SHOULD  be defined (see ARB_26 in [Topic 12])
how the attributes or metadata representing the location at which a machine-readable
version of the trust anchor to be used for verifying the attestation can be found,
specified in section 2, are used. This includes a detailed description about how
a Relying Party can obtain the trust anchors, as well as a detailed description about
how this trust anchor can be used for verifying that the provider is authorized
to issue the attestation. Additionally, for non-qualified EAA Providers this section
MAY include a description of mechanisms that can be used by a Wallet Unit for
verifying that the provider is authorized to issue this type of attestation (see
ISSU_34 in [Topic 10])*

## 6 Revocation

(Refer to [Topic 7] of the ARF for a list of High-Level Requirements related to Revocation)

*In this section information about the revocation mechanism used SHALL be defined.*

*For PID, QEAA, or PuB-EAA it SHALL  be defined whether  only short-lived attestations
will be used, having a validity period of 24 hours or less, such that revocation
will never be necessary, or that the attestations are revocable.*

*For revocable attestations it SHALL be defined which of the following methods must be implemented:*

* Use an Attestation Status List mechanism included in a Technical Specification
that will be specified by the Commission.
* Use an Attestation Revocation List mechanism included in a Technical Specification
that will be specified by the Commission.

## 7 Compliance

*In this section explicitly state how this specific rulebook complies with the
general EUDI framework, ARF, and relevant regulations*

[RULEBOOK AUTHOR TO DEFINE]

## 8 References

| **Item Reference** | **Standard name/details**|
|--------------------|---------------------------|
| [European Digital Identity Regulation] | [Regulation (EU) 2024/1183](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202401183) of the European Parliament and of the Council of 11 April 2024 amending Regulation (EU) No 910/2014 as regards establishing the European Digital Identity Framework |
| [HAIP] | Yasuda, K. *et al,* OpenID4VC High Assurance Interoperability Profile, OpenId Foundation, Version draft-03 |
| [IANA-JWT-Claims] | IANA JSON Web Token Claims Registry. Available: <https://www.iana.org/assignments/jwt/jwt.xhtml> |
| [ISO/IEC 18013-5] |  ISO/IEC 18013-5, Personal identification --- ISO-compliant driving licence - Part 5: Mobile driving licence (mDL) application, First edition, 2021-09 |
| [OIDC] | Sakimura, N. et al., "OpenID Connect Core 1.0", OpenID Foundation. Available: <https://openid.net/specs/openid-connect-core-1_0.html> |
| [RFC 3339] | RFC 3339  - Date and Time on the Internet: Timestamps, G. Klyne et al., July 2002 |
| [RFC 8610] | RFC 8610  - Concise Data Definition Language (CDDL): A Notational Convention to Express Concise Binary Object Representation (CBOR) and JSON Data Structures, H. Birkholz et al., June 2019 |
| [RFC 8943] | RFC 8943  - Concise Binary Object Representation (CBOR) Tags for Date, M. Jones et al., November 2020 |
| [RFC 8949] | RFC 8949 - Concise Binary Object Representation (CBOR), C. Bormann et al., December 2020 |
| [SD-JWT VC] |  SD-JWT-based Verifiable Credentials (SD-JWT VC). Available: <https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/>, version draft-ietf-oauth-sd-jwt-vc-09  |
| [Topic 7] | ARF Annex 2 - Topic 7 - Attestation revocation and revocation checking Available: <https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/annexes/annex-2/annex-2-high-level-requirements/#a237-topic-7-attestation-revocation-and-revocation-checking>|
| [Topic 10] | ARF Annex 2 - Topic 10 - Issuing a PID or attestation to a Wallet Unit: <https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/annexes/annex-2/annex-2-high-level-requirements/#a2310-topic-10-issuing-a-pid-or-attestation-to-a-wallet-unit>|
| [Topic 12] | ARF Annex 2 - Topic 12 - Attestation Rulebooks, Available: <https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/annexes/annex-2/annex-2-high-level-requirements/#a2312-topic-12-attestation-rulebooks>|
| [Topic 20] | ARF Annex 2 - Strong User authentication for electronic payments, Available: <https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/annexes/annex-2/annex-2-high-level-requirements/#a2320-topic-20-strong-user-authentication-for-electronic-payments>|
| [W3C VCDM v2.0] | Sporny, M. *et al,* Verifiable Credentials Data Model v2.0, W3C Recommendation.  |
