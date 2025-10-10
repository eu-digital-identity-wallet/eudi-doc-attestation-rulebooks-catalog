
# Attestation Rulebook for attestations of type  *ADD THE ATTESTATION TYPE HERE*

* Author(s): 
    * Gerd Bauer, DC4EU WP6
    * Katharina Hilmar, DC4EU WP6
* Previous Authors
    * [NAME SURNAME, AFFILIATION (versions)]
    * [NAME SURNAME, AFFILIATION (versions)]

*Provide versioning information about the Rulebook in the following form:*

| Version | Date | Description |
|---------|------------|------------|
| 0.1 | 2025-06-02 | 1st version of the document for comments provided |
| 1.0 | 2025-06-27 | 2nd version of the document for comments provided |
| 1.1 | 2025-07-01 | Template adapted |


*Provide a contact email address and/or a link to an issue tracking system that can be used for
providing feedback, e.g.:* 

**Feedback:**
  *  https://example.com/tracker 

## 1 Introduction

### 1.1 Document scope and purpose

This rulebook defines the requirements and constrains pertaining to EHIC PuB-EAAs as used within social security coordination in Europe.

### 1.2 Document structure

- Chapter 2, which describes the attestation attributes and metadata in an 
encoding-independent manner. 
- Chapter 3, which specifies how the attestation
attributes and metadata are encoded in case the attestation complies with [ISO/IEC
18013-5] and/or [SD-JWT VC] and/or [W3C VCDM v2.0]. 
- Chapter 4, which specifies attestation usage.
- Chapter 5, which defines trust anchors
- Chapter 6, which defines revocation mechanisms
- Chapter 7, which provides compliance information

### 1.3 Key words

This document uses the capitalised key words 'SHALL', 'SHOULD' and 'MAY' as
specified in [RFC 2119], i.e., to indicate requirements, recommendations and
options specified in this document.

In addition, 'must' (non-capitalised) is used to indicate an external
constraint, i.e., a requirement that is not mandated by this document, but, for
instance, by an external document. The word 'can' indicates a capability,
whereas other words, such as 'will', and 'is' or 'are' are intended as
statements of fact.

### 1.4 Terminology

This document uses the terminology specified in Annex 1 of the ARF.

## 2 Attestation attributes and metadata

The European Health Insurance Card (EHIC) credential is a specialised instance of the common PuB-EAAS attribute block defined in the Rulebook `attestation-rulebook-wp6-common.md`. 

It does *not* introduce additional attributes or metadata.


# 3 Attestation encoding 

## 3.1 ISO/IEC 18013-5-compliant encoding 
Finally, illustrative examples SHALL be included. 

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF FULL OR PARTIAL mDOC OF THE ATTESTATION]

[RULEBOOK AUTHOR TO PROVIDE THE ATTRIBUTES AND THEIR VALUES INCLUDED IN THE EXAMPLE]

### 3.2 SD-JWT VC-based encoding 

Finally, illustrative examples SHALL be included. 

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF THE JWT CLAIM SET USED BY THE PROVIDER]

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF THE ISSUED SD-JWT (IN base64 ENCODING)]

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF A HUMAN READABLE VERSION OF THE SD-JWT PAYLOAD
AND A DESCRIPTION OF THE DISCLOSURES INCLUDED IN THE EXAMPLE]


## 4 Attestation usage
*Briefly describe the primary use cases or scenarios for which this attestation 
type is intended*

*Additionally, in this section it SHOULD  be specified whether a Relying Party receiving the attestation
must request and verify a PID (see ARB_27 in [Topic 12]). Also beyond PID verification, 
it SHOULD be defined what other key obligations does a Relying Party have when processing 
this attestation type (e.g., signature verification, freshness checks)*

*Furthermore, provide potential presentation requirements, e.g., are there specific 
requirements for how this attestation must be presented (e.g., online, offline, specific protocols)?"*

*Finally, in this section information about potential transactional data
SHALL be defined (see [Topic 20] of Annex 2 of the ARF).*

## 5 Trust anchors

Trust anchors for EHIC PuB-EAAs are the same as defined in the common rulebook.

## 6 Revocation

Revocation patterns for EHIC PuB-EAAs are the same as defined in the common rulebook.

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








 
