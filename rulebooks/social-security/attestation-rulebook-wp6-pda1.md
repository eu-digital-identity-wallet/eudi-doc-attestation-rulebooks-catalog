
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

This rulebook defines the requirements and constrains pertaining to PDA1 PuB-EAAs as used within social security coordination in Europe.

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

The European Health Insurance Card (PDA1) credential is a specialised instance of the common PuB-EAAS attribute block defined in the Rulebook `attestation-rulebook-wp6-common.md`. 

The PDA1 adds a number of private namespace attributes to the set inherited from the common.

### 2.1 Mandatory attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| employer.id	|	Unique identifier of the employer. | string |	urn:dgempl:pubeaas:pda1:v1:attribute:employer:id |
| employer.name |	Name of the employer. | string |	urn:dgempl:pubeaas:pda1:v1:attribute:employer:name |
| employer.country	| Country where the employer is registered. | string (ISO 3166-1 alpha-2) |urn:dgempl:pubeaas:pda1:v1:attribute:employer:country |
| work_address.locality |	City, town, or locality of the workplace. | string |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:locality |
| work_address.country |Country of the workplace. | string (ISO 3166-1 alpha-2) |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:country |
| legislation_country |	Country whose legislation applies. | string (ISO 3166-1 alpha-2) |	urn:dgempl:pubeaas:pda1:v1:attribute:legislation_country |
| status_confirmation	|	Legal status category code applicable to the worker. |string |	urn:dgempl:pubeaas:pda1:v1:attribute:status_confirmation |


### 2.2 Optional attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| work_address.region |	Region or state of the workplace. | string |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:region |
| work_address.formatted | Full formatted workplace address. |string | urn:dgempl:pubeaas:pda1:v1:attribute:work_address:formatted |
| work_address.street_address	|	Street name of the workplace. | string |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:street_address
| work_address.building_number | Building number of the workplace. | string	|urn:dgempl:pubeaas:pda1:v1:attribute:work_address:building_number |
| work_address.postal_code	|	Postal or ZIP code of the workplace.	| string |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:postal_code |





# 3 Attestation encoding 

## 3.1 ISO/IEC 18013-5-compliant encoding 

| **Data Identifier** | **Attribute identifier** | **Encoding format** |**Namespace**|
|------------------------|--------------|------------------|------------------|
| employer.id	|	employer.id | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:employer:id |
| employer.name |	employer.name | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:employer:name |
| employer.country	| employer.country | tstr (ISO 3166-1 alpha-2) |urn:dgempl:pubeaas:pda1:v1:attribute:employer:country |
| work_address.locality |	work_address.locality | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:locality |
| work_address.country |work_address.country | tstr (ISO 3166-1 alpha-2) |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:country |
| legislation_country |	legislation_country | tstr (ISO 3166-1 alpha-2) |	urn:dgempl:pubeaas:pda1:v1:attribute:legislation_country |
| status_confirmation	|	status_confirmation | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:status_confirmation |
| work_address.region |	work_address.region | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:region |
| work_address.formatted | work_address.formatted | tstr | urn:dgempl:pubeaas:pda1:v1:attribute:work_address:formatted |
| work_address.street_address	|	work_address.street_address | tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:street_address
| work_address.building_number | work_address.building_number | tstr	|urn:dgempl:pubeaas:pda1:v1:attribute:work_address:building_number |
| work_address.postal_code	|	work_address.postal_code	| tstr |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:postal_code |


Finally, illustrative examples SHALL be included. 

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF FULL OR PARTIAL mDOC OF THE ATTESTATION]

[RULEBOOK AUTHOR TO PROVIDE THE ATTRIBUTES AND THEIR VALUES INCLUDED IN THE EXAMPLE]

### 3.2 SD-JWT VC-based encoding 

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |
|---------------------|--------------------------|---------------------|-----------|
| employer.id	|	urn:dgempl:pubeaas:pda1:v1:attribute:employer:id | string |	 |
| employer.name |	urn:dgempl:pubeaas:pda1:v1:attribute:employer:name | string |	 |
| employer.country	| urn:dgempl:pubeaas:pda1:v1:attribute:employer:country | string | (ISO 3166-1 alpha-2) |
| work_address.locality |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:locality | string |	 |
| work_address.country | urn:dgempl:pubeaas:pda1:v1:attribute:work_address:country | string | (ISO 3166-1 alpha-2)	 |
| legislation_country |	urn:dgempl:pubeaas:pda1:v1:attribute:legislation_country | string |(ISO 3166-1 alpha-2) |
| status_confirmation	|	urn:dgempl:pubeaas:pda1:v1:attribute:status_confirmation | string |	 |
| work_address.region |	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:region | string |	 |
| work_address.formatted | urn:dgempl:pubeaas:pda1:v1:attribute:work_address:formatted | string |  |
| work_address.street_address	|	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:street_address | string |	
| work_address.building_number | urn:dgempl:pubeaas:pda1:v1:attribute:work_address:building_number | string	| |
| work_address.postal_code	|	urn:dgempl:pubeaas:pda1:v1:attribute:work_address:postal_code	| string |	 |


The PD A1 credential implements selective disclosure using the SD-JWT model. This allows a credential holder to disclose only the minimum required claims to a verifier, supporting GDPR-compliant privacy by design.
-	Claims marked "always" in the SD policy must be selectively disclosed by the holder.
-	Claims marked "never" are always publicly visible and required for verification.

|Claim Path |	Disclosure (sd) |	Purpose |
|-----------|-----------------|---------|
| personal_administrative_number |	always	| Protected identifier; disclosed only when required for verification|
| document_number	| always	| PD A1 document ID; disclosed only when required |
| issuing_authority (and subfields id, name) | never	| Issuance authority metadata; always visible |
| authentic_source (and subfields id, name) |	never	| Verification source; always visible |
| issuing_country	| never	| Jurisdiction and national policy context |
| date_of_expiry, date_of_issuance |	never |	Credential administrative validity |
| starting_date, ending_date	| never	| Coverage period for social security |
| employer (and subfields id, name, country) | never |	Workplace identification; mandatory for entitlement verification |
| work_address (all fields)	| never |	Location of work; mandatory for coverage assessment |
| legislation_country |	never |	Applicable legal framework |
| status_confirmation |	never |	Legal status code determining applicable law |

This embedded policy establishes a verifier-agnostic framework for enforcing disclosure behaviour, regardless of wallet implementation.



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








 
