
# Attestation Rulebook for attestations of type  *ADD THE ATTESTATION TYPE HERE*

*Provide information about the author(s) of this Rulebook in the following form:*

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

This Rulebook establishes a common framework for the issuance, management, and verification of Public Body Electronic Attribute Attestationss (PuB-EAAs)  within the EUDI wallet ecosystem and in support of social security coordination across the European Union. Its primary objective is to enable the secure, privacy-preserving, and interoperable exchange of Electronic Attestations of Attributes, such as the European Health Insurance Card (EHIC) and the Portable Document A1 (PD A1), which are developed within the context of the European ESSPASS project.

The Rulebook is designed to:
-	Standardise credential issuance in alignment with legal and technical requirements defined under the eIDAS framework.
-	Enable event-driven verification tailored to specific business contexts and lifecycle triggers.
-	Promote semantic and syntactic interoperability through harmonised data models, credential schemas, and trust frameworks.
-	Facilitate cross-border mobility by ensuring that digital credentials are verifiable and legally recognised across Member States and sectors.
-	Implement privacy by design, leveraging Selective Disclosure to support data minimisation, unlinkability, and user control in accordance with the revised eIDAS Regulation and the GDPR.
-	Support governance and trust through clearly defined roles, responsibilities, and quality assurance mechanisms.

This Rulebook is intended for public authorities, service providers, implementers, and governance bodies responsible for delivering and managing digital public services and social security rights in a cross-border, multi-sector EU context


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

*It is recommended to use the terminology defined in Annex 1 of ARF. For example
the following text can be used.* 

This document uses the terminology specified in Annex 1 of the ARF.

### 1.5 Governance
This chapter suggests a governance structure for the lifecycle management, oversight, and evolution of the Rulebook and related  services within the domain of EU social security coordination.
#### 1.5.1	 GOVERNANCE OBJECTIVES
-	Ensure transparent and inclusive oversight of rulebook updates and implementation.
-	Maintain consistency with EU legislation and cross-border trust frameworks provided by the EUDI wallet ecosystem.
-	Provide a clear allocation of responsibilities among EU-level and national-level stakeholders.
-	Support ongoing compliance, quality assurance, and incident management.
-	The governance structure should follow the established structure in social security coordination.

#### 1.5.2  GOVERNANCE STRUCTURE
|Entity | Responsibility |
|-------|----------------|
| European Commission (DG EMPL)	| Strategic oversight to ensure alignment between eIDAS and the social security coordination framework. |
|Administrative Commission on the Coordination of Social Security Systems | Periodic review and coordination of legal, operational, and policy frameworks. |
| Technical Commission on the Coordination of Social Security Systems |	Technical harmonisation of processes for issuance, revocation, representation and verification of ESSPASS documents implemented as Public Body Electronic Attestations of Attributes (PuB-EAAs), including interaction with digital identity and trust services provided by the EUDI framework. |
| National Competent Authorities |	PuB-EAA issuance according to Rulebook, compliance with national and EU law, and revocation at the Member State level. |
| Social Security  PuB-EAA Technical Maintenance Board | Management of data schemas, versioning, operational guidance, and interoperability updates. |
| Expert Groups on Social Security Coordination (e.g., Applicable Legislation, Sickness, Pensions)	| Definition of business requirements, attribute semantics, and operational rules for specific domains within the PuB-EAA framework of eIDAS. |

#### 1.5.3 CHANGE MANAGEMENT
-	Rulebook updates shall be proposed via a structured process coordinated by the Social Security PuB-EAA Technical Maintenance   Board.
-	All changes must undergo consultation and review involving both technical and policy committees.
-	Final approval lies with a joint governance body composed of representatives from the European Commission, selected Member States, and relevant expert groups.
#### 1.5.4	VERSIONING AND PUBLICATION
-	Rulebook versions are identified by a semantic versioning scheme (e.g., v1.0.0).
-	Version identifiers must be reflected in namespace URIs used across the data models (see Section 7.7).
-	A public registry of approved versions shall be maintained by DG EMPL or a delegated trusted authority.
-	Deprecated versions shall remain accessible for reference but must not be used for new attestation issuance.
#### 1.5.5	DISPUTE RESOLUTION AND ESCALATION
-	Disputes regarding compliance, trust breaches, or rule interpretation should first be handled by the National Competent Authority.
-	Escalation to EU-level governance (e.g., DG EMPL or the Administrative Commission) occurs when bilateral resolution fails.
-	Independent mediation or expert review may be convened if required.

This governance model ensures continued trust, legal integrity, and interoperability of PuB-EAA credentials in a pan-European context.

### 1.6 Legal & Regulatory framework
This chapter outlines the legal and regulatory environment that underpins the issuance and recognition of PuB-EAA credentials for social security coordination within the European Union and the members of the European Free Trade Association (EU/EFTA). It provides the foundation for ensuring that all technical and operational specifications are compliant with EU law and Member State obligations.
#### 1.6.1	PRIMARY LEGAL INSTRUMENTS
| Regulation / Directive | Description |
|------------------------|-------------|
| Regulation (EC) No 883/2004	| Governs the coordination of social security systems across the EU. Forms the legal basis for EHIC and PD A1 in traditional format. | 
| Implementing Regulation (EC) No 987/2009 |	Details the administrative procedures and data exchange mechanisms for Regulation 883/2004. |
| Decision No S1 of 12 June 2009 |	Sets general provisions for the “traditional”  EHIC, including its purpose, legal effects, and fallback procedures such as provisional replacement certificates. |
| Decision No S2 of 12 June 2009 |	Specifies the technical design, visible information, and model for the “traditional” EHIC and its provisional replacement certificate.|
| Revised eIDAS Regulation (Regulation (EU) 2024/1183) |	Revises and extends the eIDAS framework to support the EUDI wallet and verifiable credentials framework. Provides legal recognition of electronic attestations of attributes especially the PuB-EAA regime. |
| GDPR (Regulation (EU) 2016/679) |	Establishes rules on data protection and privacy. Ensures lawful processing of personal data. |
| Data Governance Act (Regulation (EU) 2022/868) |	Supports data sharing and reuse in the public sector under common European data spaces. | 
| Interoperable Europe Act (Regulation (EU) 2024/903) |	Lays down measures for a high level of public sector interoperability across the EU. |

#### 1.6.2	LEGAL BASIS FOR CREDENTIAL ISSUANCE
-	The issuance of traditional ESSPASS documents (e.g. EHIC and PD A1) by public bodies or entities acting on their behalf is grounded in national implementation of Regulation 883/2004 and 987/2009.
-	The use of electronic attestations must comply with trust and identity provisions under the revised eIDAS Regulation foreseen for attestations issued by or behalf of public bodies (PuB-EAAs).
-	Each PuB-EAA must carry legal validity across borders in line with mutual recognition principles defined in the revised eIDAS Regulation.
#### 1.6.3	DATA PROTECTION AND USER RIGHTS
-	All processing activities must be based on a legal basis (e.g., public interest, legal obligation).
-	The use of Embedded Selective Disclosure supports data minimisation, purpose limitation, and user control.
-	Citizens have the right to access, rectify, and control the dissemination of their personal information.
#### 1.6.4	LEGAL INTEROPERABILITY
-	Legal interoperability is achieved by aligning technical structures (e.g., schemas, namespaces) with recognised standards, legal requirements and responsibilities.
-	Institutions relying on ESSPASS documents must accept valid attestations issued under the attestation Rulebook in accordance with the revised eIDAS Regulation.

This framework ensures that all credential-based interactions are both technically robust and legally enforceable across jurisdictions.

### 1.7 Pub-EAA Service
The PuB-EAA service provides a legally valid, privacy-preserving, and interoperable mechanism to digitally attest attributes related to social security entitlements by public bodies or entities acting on their behalf across the EU. These credentials, developed in the context of the ESSPASS initiative, support the cross-border and cross-sectoral exchange of verifiable information between national public authorities, citizens, and service providers.
The PuB-EAA system functions within an open, cross-border, and cross-sector trust ecosystem, enabling the use and verification of attestations not only across both EU Member States and different administrative sectors, in line with the revised eIDAS Regulation.
#### 1.7.1	SUPPORTED CREDENTIALS
This DC4EU version of the Rulebook supports two key credentials central to social security coordination. The framework, however, is designed to be extensible and can be expanded to accommodate additional credentials foreseen in ESSPASS as digital transformation progresses.
-	European Health Insurance Card (EHIC): Proves entitlement to necessary healthcare services while temporarily staying in other EU Member States under the applicable conditions of the host Member State.
-	Portable Document A1 (PD A1): Confirms the applicable social security legislation for posted workers or persons working in multiple countries.
#### 1.7.2	LIFECYCLE SERVICES
The PuB-EAA trust framework supports the following credential lifecycle operations:
-	Issuance: Performed by public bodies or mandated institutions on behalf of them.
-	Selective Disclosure: Holders can, in some use-cases, share only the necessary attributes with relying parties in a flexible and user-friendly way.
-	Presentation: Credentials can be securely presented to relying parties. This ensures interoperability and trust across different systems.
-	Verification: Relying parties validate the credential and its digital signature using established trust anchors.
-	Revocation: Revocation mechanisms ensure that credentials can be invalidated when no longer applicable.
#### 1.7.3	INTEGRATION WITH EIDAS AND THE EUDI WALLET
The PuB-EAA service model is fully aligned with the revised eIDAS Regulation and designed for seamless integration with the EUDI Wallet ecosystem. If offers users a secure and trusted interface for managing and presenting Electronic Attestations of Attributes (EAAs) issued by or on behalf of public bodies—including those used in ESSPASS—in combination with Person Identification Data (PID) issued by national identity providers.
To ensure legal validity and personal attribution, the use of the electronic identification means embedded in the EUDI Wallet is mandatory at the time of credential issuance. This mechanism supports:
-	Verification of the holder’s identity
-	Proof of possession of the digital wallet, ensuring cryptographic binding of the credential to the rightful owner

As a mandatory policy, Person Identification Data (PID) from the EUDI Wallet must be requested and validated before issuing any PuB-EAA credential into a valid EUDI wallet. This ensures:
-	Unique and unambiguous identification of the holder
-	Credential binding to a verified digital identity
-	Prevention of identity fraud or mis-issuance

The PID fields required for issuance include the core attributes defined in the revised eIDAS Regulation:
-	Family name
-	Given name
-	Birth date
-	Birth place
-	Nationality

Note: While these attributes are harmonised at the EU level, differences in national identity systems, such as optional fields or privacy rules, may impact cross-border matching. The EUDI Wallet ecosystem aims to address these challenges through attribute mapping, normalisation, and transformation services.
In use cases which require identity information during credential verification, the PID from the EUDI Wallet must also be used. Other cases could rely simply on the valid credential and the device binding and control to confirm:
-	That the credential is being presented by its rightful holder
-	That the holder is eligible for the benefit or entitlement being requested
-	That credential use is protected from fraud, replay, or impersonation

The dual use of PID during both issuance and verification ensures legal certainty, operational integrity, and high assurance across Member States.
The presentation and verification of the PID is an integral part of the verification policy, which defines how the credential is validated in the context of a specific legal or business use case. This policy includes not only rules for data disclosure but also identity proof requirements that bind the credential to the individual presenting it. Such binding ensures trustworthyness and authentication across borders in accordance with the revised eIDAS framework. It must be highlighted that the (cryptographic) binding of attestation to the holder in the EUDI wallet makes the identity information less critical to verify in most business cases.
#### 1.7.4	BENEFITS FOR STAKEHOLDERS
| Stakeholder	| Benefits |
|---------------|----------|
| Citizens (Holders)	| Access to rights across borders, security, and control over data with a mobile device.|
| Issuing Authorities	| Standardised, secure issuance and auditability. |
| Relying Parties |	Fast, verifiable, and trusted data validation. |

This service related to PuB-EAAs issued under eIDAS underpins the secure and efficient coordination of social security entitlements across Member States, enabling digital mobility and reducing administrative burden.

### 1.8	Authentic Source and Issuer
In the context of PuB-EAA credential issuance for social security coordination, it is essential to differentiate between the Authentic Source and the Issuer. Both roles are critical to ensuring trust, legal compliance, and semantic clarity across Member States.
The Authentic Source is  defined in eIDAS as the business decision-making body and may differ from the Issuer, which is the technical entity generating the credential. 

This institution is:
-	Officially designated under national or EU law.
-	Registered in systems such as the EESSI Institution Repository.
-	Responsible for determining coverage entitlement, validity periods, and accurate identity linkage to benefits - in the form of a business decision.

Responsibilities:
-	Provide verified data about the citizen's entitlement (e.g., EHIC or PD A1 coverage).
-	Maintain accurate and up-to-date information on the insured person's status (coverage, revocation).
-	Serve as the legal reference for resolving data disputes or validating claims during verification.

Fields in credentials representing the authentic source include:
-	authentic_source.id
-	authentic_source.name

The Issuer is the digital entity that packages and signs the credential using cryptographic mechanisms. This entity ensures the technical trustworthiness and interoperability of the credential. While it may also be the authentic source in some implementations, separation of duties is often applied for efficiency, governance, and audit purposes in line with Section 2.2.2.3 of the eIDAS 2.0 Architecture Reference Framework (ARF).

Responsibilities:
-	Generate Verifiable Credentials based on business decision data from authentic source.
-	Bind the credential to the holder's EUDI Wallet, and thereby indirectly to the PID.
-	Ensure compliance with the eIDAS trust framework, this Rulebook, and versioned namespace definitions.
-	Use cryptographic signing keys that are referenced in national or EU Trusted Lists, establishing recognised trust anchors in accordance with the eIDAS Regulation.
-	Ensure that the associated Qualified Trust Service Provider (QTSP) and relevant trust services (e.g., electronic seals or signatures) are listed in the EU Trusted List or equivalent national trusted lists.

Fields in credentials representing the issuer include:
-	iss (Issuer URI)
-	issuing_authority.id
-	issuing_authority.name
-	issuing_authority.country

While the iss URI identifies the issuer at a logical level, trust in the credential is established through the Public Key Infrastructure (PKI) anchored in the Qualified Trust Service Provider certificates published in the trusted lists. The iss URI may resolve to metadata containing key information, but verification must rely on the certificate chain validated against trusted list entries, not on the URI alone.
Although in many Members States the same institution may serve as both the Authentic Source and the Issuer, these roles are functionally distinct.
This distinction follows the ARF principle of role separation between legal authority and cryptographic authority, ensuring auditability, traceability and accountability.



## 2 Attestation attributes and metadata

*This section is used for defining all attributes that an
attestation of the defined type may contain. In this section
the attributes SHALL be defined in an encoding-independent manner (see ARB_06 in [Topic 12]). 
Each attribute can be mandatory, optional, or conditional
and it SHALL be specified in the corresponding section (see ARB_09 in [Topic 12]).*

*When attributes are defined, referring to attributes that
already exist in a catalogue of attestation attributes 
SHOULD be considered (see ARB_07 in [Topic 12]).*

*[Topic 12] of Annex 2 of the ARF defines the following High-Level Requirements with
respect to the Attestation Rulebooks*

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

*Briefly introduce the overall design and purpose of the specific attestation type 
defined by this Rulebook, including key decisions regarding its attributes and 
legal categorization.* 

*According to Annex V point a) and  Annex VII point a) of the [European Digital Identity Regulation]
an indication, at least in a form suitable for automated processing, that the attestation 
has been issued as a QEAA or Pub-EAA SHALL be defined. Similarly, according to ARB_12
of [Topic 12] of Annex 2 of the ARF a similar indication SHOULD be defined for non-qualified EAA.
This document defines the attribute "attestation_legal_category" which SHALL have
the value "QEAA" or "PuB-EAA" or "non-qualified-EAA".* 

*In the following subsections define in an encoding independent manner all 
mandatory, optional, and conditional attributes and metadata. In each subsection
provide a table of the following form:*

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| *Provide a unique attribute identifier* | *Briefly describe the semantic of this attribute*|*Provide a type, e.g., integer, string, boolean, date.*|*Give an example value*

*NOTE Data identifiers should be unambiguous, machine-readable where possible, and 
avoid natural language ambiguities.*

---

The social security credentials share a set of common business data fields critical for social security coordination. These fields support consistent identification, issuance tracking, and institutional attribution across credential types. The shared fields below are harmonised to facilitate semantic and syntactic interoperability.

These data elements constitute the basic validation block required to validate eligibility of the credential. Together with additional, credential-specific business fields, they form the basis of a localised validation policy defined at the national level. This localised policy may reflect specific regulatory, operational, or contextual requirements, and governs how credentials are verified in real-world scenarios by competent authorities.

To ensure auditability and legal certainty, the verification proof generated during a successful credential verification event must also include the common business data fields. This block serves as a reference, linking the holder, the verified credential, the authentic source responsible for the business decision, and the issuer of the credential. Additionally, it incorporates the two validation periods required for business-level evaluation

The common business data block consist of:
- Mandatory attributes
- Optional attributes
- Mandatory metadata
- Optional metadata

### 2.2 Mandatory attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| attestation_legal_category | | string | PuB-EAA |
| personal_administrative_number | Unique personal identifier used by the issuing social security services. | string | 123456789 |
| issuing_authority.id | Identifier of the issuing authority. | string | DE:456789 |
| issuing_authority.name | Name of the issuing authority. | string | DRVB |
| issuing_authority.country | Country under whose jurisdiction the credential is issued. | string (ISO 3166-1 alpha-2) | DE |
| authentic_source.id | ID of the competent institution (EESSI). | string | DE:456789 |
| authentic_source.name | Name of the competent institution (EESSI). | string | DRVB |
| document_number | Unique document identifier. | string | 83e1442d-1e4b-477f-8aeb-632e29d19255 |



### 2.3 Optional attributes

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| starting_date | Start date of coverage/benefit validity. | date | 2025-07-04 |
| ending_date | End date of coverage/benefit validity. | date | 2025-08-01 |

### 2.5 Mandatory metadata 

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| date_of_issuance | Credential issuance/start date. | date | 2025-07-01 |


### 2.6 Optional metadata 

| **Data Identifier** | **Definition** |**Data type** |**Example value** |
|------------------------|--------------|--------------|--------------|
| date_of_expiry | Credential expiration date.| date | 2025-08-01 |


## 2.2 The three validity layers

| Layer | Purpose |	Fields |	Validation Responsibility |
|-------|---------|--------|------------------------------|
| Technical Validity (Token envelope) |	Ensures that the credential can be cryptographically verified and processed |	iat, nbf, exp (JWT fields or mdoc equivalents) |	Verifier system (automated check) |
| Document Validity (Credential lifecycle) | Determines the document’s issuance and expiry from an administrative point of view |	date_of_issuance, date_of_expiry |	Verifier |
| Coverage Validity (Entitlement timeframe) |	Defines the real-world period for which a benefit or entitlement is valid |	starting_date, ending_date (e.g., for insurance or employment) | Policy logic / domain-specific rules |


-	Technical validity defines the timeframe during which the credential can be securely processed as a cryptographically valid container. Once the exp value (expiration time) has passed, the credential is no longer considered to exist in a verifiable form. This period should be carefully chosen to support both security objectives (e.g. replay protection) and credential usability (e.g. caching, offline processing).
-	Document validity reflects the administrative lifecycle of the credential, such as its issuance and formal expiration, based on institutional policies or credential type. It allows relying parties to assess whether the credential is still administratively valid, even if it refers to past or future coverage periods. The document validity window should support validation scenarios that require checking both retrospective and prospective entitlements.
-	Coverage validity defines the real-world period during which a social security benefit or entitlement is applicable. This period is central to the legal effect of the credential and must be explicitly evaluated as part of the standard verification policy. Coverage dates determine whether the citizen is currently or historically eligible for specific services, such as healthcare or insurance, and should always be enforced at runtime.


# 3 Attestation encoding 
All attestations of attributes in the social security coordination space are to be encoded in both SD-JWT and mdoc format, such that both proximity and remote use cases are supported.

## 3.1 ISO/IEC 18013-5-compliant encoding 

*Furthermore, in this section a document type SHALL be defined, which SHALL be 
unique within the scope of the EUDI Wallet ecosystem (see ARB_05 in [Topic 12]).*

[RULEBOOK AUTHOR TO DEFINE THE ATTESTATION TYPE]

*Provide a list of available encoding formats and their specifications (e.g., encoding, maximum lengths, 
date formats, etc). For example:*

- tstr, uint, bstr, bool and tdate are CDDL representation types defined in
  [RFC 8610].
    - Regarding type tstr: this document confirms that, as specified in [RFC
    8949], a tstr SHALL be encoded in UTF-8 and SHALL support the full Unicode
    range.
    - All attributes having encoding type tstr SHALL have a maximum length of
    150 characters.
    - This document specifies full-date as full-date = #6.1004(tstr), where tag
    1004 is specified in [RFC 8943].
    - In accordance with [RFC 8949], section 3.4.1, a tdate attribute SHALL
    contain a date-time string as specified in [RFC 3339]. In accordance with
    [RFC 8943], a full-date attribute SHALL contain a full-date string as
    specified in [RFC 3339].
    - The following requirements apply to the representation of dates in
    attributes, unless otherwise indicated:
        - Fractions of seconds SHALL NOT be used;
        - A local offset from UTC SHALL NOT be used; the time-offset defined in
        [RFC 3339] SHALL be to "Z".
    - [RFC 8949], section 4.2, describes four rules for canonical CBOR. Three of
    those rules SHALL be implemented for all CBOR structures, as
    follows:
        - integers (major types 0 and 1) SHALL be as small as possible;
        - the expression of the length in a bstr, tstr, array or map SHALL be as
        short as possible;
        - indefinite-length items SHALL be made into definite-length items.

*This section should include a table the data identifier specified in
Chapter 2,  the corresponding attribute identifier to be used in
presentation requests and responses according to [ISO/IEC 18013-5] and the encoding 
of each attribute.*

*Additionally, the following rules should be followed:*

* When specifying new attributes existing conventions 
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

---------

| **Data Identifier** | **Attribute identifier** | **Encoding format** |**Namespace**|
|------------------------|--------------|------------------|------------------|
| attestation_legal_category | attestation_legal_category | tstr | urn:dgempl:pubeaas:v1:attribute:attestation_legal_category | 
| personal_administrative_number | personal_administrative_number | tstr | urn:dgempl:pubeaas:v1:attribute:personal_administrative_number |
| issuing_country | issuing_country | tstr | urn:dgempl:pubeaas:v1:attribute:issuing_country |
| document_number | document_number | tstr | urn:dgempl:pubeaas:v1:attribute:document_number |
| issuing_authority.id | issuing_authority.id | tstr | urn:dgempl:pubeaas:v1:attribute:issuing_authority:id |
| issuing_authority.name | issuing_authority.name | tstr | urn:dgempl:pubeaas:v1:attribute:issuing_authority:name |
| authentic_source.id | authentic_source.id | tstr | urn:dgempl:pubeaas:v1:attribute:authentic_source:id |
| authentic_source.name | authentic_source.name | tstr | urn:dgempl:pubeaas:v1:attribute:authentic_source:name |
| starting_date | starting_date | tdate | urn:dgempl:pubeaas:v1:attribute:starting_date |
| ending_date | ending_date | tdate | urn:dgempl:pubeaas:v1:attribute:ending_date |
| date_of_issuance | date_of_issuance | tdate | urn:dgempl:pubeaas:v1:attribute:date_of_issuance |
| date_of_expiry | date_of_expiry | tdate | urn:dgempl:pubeaas:v1:attribute:date_of_expiry |

Finally, illustrative examples SHALL be included. 

[RULEBOOK AUTHOR TO PROVIDE AN EXAMPLE OF FULL OR PARTIAL mDOC OF THE ATTESTATION]

[RULEBOOK AUTHOR TO PROVIDE THE ATTRIBUTES AND THEIR VALUES INCLUDED IN THE EXAMPLE]

### 3.2 SD-JWT VC-based encoding 
*If the attestation type supports the the format specified in "SD-JWT-based Verifiable 
Credentials (SD-JWT VC)", then in this section the  SD-JWT VC-compliant encoding 
of attributes and metadata should be defined. It SHALL be ensured that the attestations 
comply with the 'SD-JWT VCs' profile specified in [HAIP] (see ARB_01b in [Topic 12]).*

*It is noted that a  Schema Provider  MAY specify in the Attestation 
Rulebook that that type of attestation must be issued in the [SD-JWT VC]-compliant 
format, provided the [SD-JWT VC] specification has been approved by an EU standardisation 
body or by the European Digital Identity Cooperation Group established pursuant to 
Article 46e(1) of the [European Digital Identity Regulation] (see ARB_03 in [Topic 12]).*

*In this section, a Verifiable Credential Type (`vct`) SHALL be defined,
which SHALL be unique within the scope of the EUDI Wallet ecosystem (see ARB_05 in [Topic 12]).*

[RULEBOOK AUTHOR TO DEFINE THE ATTESTATION TYPE]

*Additionally,  when specifying new attributes existing conventions 
for attribute identifier values and attribute syntaxes SHOULD
be considered (see ARB_07 in [Topic 12]).*

*It SHALL be ensured that each claim name is either included in the IANA registry 
for JWT claims, or is a Public Name as defined in [RFC 7519] (see ARB_06b in [Topic 12]).* 

----------------

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |
|---------------------|--------------------------|---------------------|-----------|
| attestation_legal_category | attestation_legal_category | string | Defined in Attestation Rulebook template |
| personal_administrative_number | urn:dgempl:pubeaas:v1:attribute:personal_administrative_number | string | See section 2 |
| issuing_country | urn:dgempl:pubeaas:v1:attribute:issuing_country | string | See section 2 |
| document_number | urn:dgempl:pubeaas:v1:attribute:document_number | string | See section 2 |
| issuing_authority.id | urn:dgempl:pubeaas:v1:attribute:issuing_authority:id | string | See section 2 |
| issuing_authority.name | urn:dgempl:pubeaas:v1:attribute:issuing_authority:name | string | See section 2 |
| authentic_source.id | urn:dgempl:pubeaas:v1:attribute:authentic_source:id | string | See section 2 |
| authentic_source.name | urn:dgempl:pubeaas:v1:attribute:authentic_source:name | string | See section 2 |
| starting_date | urn:dgempl:pubeaas:v1:attribute:starting_date | string | ISO 8601-1 [ISO8601‑1] YYYY-MM-DD format |
| ending_date | urn:dgempl:pubeaas:v1:attribute:ending_date | string | ISO 8601-1 [ISO8601‑1] YYYY-MM-DD format |
| date_of_issuance | urn:dgempl:pubeaas:v1:attribute:date_of_issuance | string | ISO 8601-1 [ISO8601‑1] YYYY-MM-DD format |
| date_of_expiry | urn:dgempl:pubeaas:v1:attribute:date_of_expiry | string | ISO 8601-1 [ISO8601‑1] YYYY-MM-DD format|


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

-----------
The common PuB-EAA structure for social security coordination attestations, provides shared data elements essential for holder binding, institutional auditability, and administrative lifecycle control. These fields are harmonised with the generic namespace structure and enable semantic and syntactic interoperability across systems.

Specific credential types may introduce additional attributes and constraints as fits the specific purposes.

This modular approach ensures:
-	Reuse of harmonised field definitions across credentials.
-	Credential-specific validation and rendering policies.
-	Support for privacy-preserving selective disclosure.


### 4.1 Verification Policy and Guidelines
This chapter defines the principles and structure for verification policies applicable to PuB-EAA credentials, ensuring consistency across Member States while supporting localised implementations. It is agnostic to the specific technology used for policy enforcement.
#### 4.1.1	OBJECTIVES
-	Promote consistent verification practices for social security credentials.
-	Reflect national-specific legal and procedural frameworks.
-	Align disclosure expectations with the selective disclosure capabilities of SD-JWT. While SD-JWT enables highly granular disclosure, practical implementations must strike a balance between usability, data protection, security, and system performance
#### 4.1.2	STRUCTURE OF A VERIFICATION POLICY
Each policy should define:
-	**Purpose of Verification:** The specific entitlement or benefit tied to the credential use.
-	**Required Claims:** The minimum set of attributes needed for verification.
-	**Optional/Conditional Claims:** Contextual data required under certain legal or procedural conditions.
-	**Verifier Authorisation:** The institutions or roles allowed to perform verification.
-	**Selective Disclosure Guidance:** Expected behaviour for data presentation and embedded logic.

Verification policies shall be formally published and versioned according to the procedures in the ARF Section 3.4 and registered in a national or EU-wide repository as required by the Implementing Acts. 

The foundation for each verification policy is a common business data block that is used consistently across all social security credentials (e.g., EHIC, PD A1). This block ensures reliable identification and institutional attribution and serves as the baseline for trust and validation.

In addition, the embedded disclosure policy, defined at credential modelling level, captures trans-European requirements that apply uniformly across Member States. This embedded logic ensures that essential attributes are consistently disclosed when needed. At the same time, it allows Member States to build on top of this base with localised rules for verification, adapted to national legislation and implementation practices.

#### 4.1.3 Local adaptation and registration
-	Member States are responsible for defining and maintaining their specific verification policy profiles.
-	Each profile must be documented, versioned, and registered in a trusted EU-wide or accessible national registry.
-	Implementation of these policies should follow procedures and requirements defined in EU implementing acts.


#### 4.1.4 Verifier obligations
Verifiers must:
-	Query or interpret the credential's status before granting access or services
-	Validate that status information is cryptographically bound to the credential
-	Respect the policy-defined status interpretation rules and respond accordingly
-	Ensure fallback mechanisms are in place when real-time checks are not possible

#### 4.1.5 Auditability
Verification proofs (see below) must indicate the status of the credential at the time of verification, including the timestamp and the source of revocation information used. This ensures legal certainty and traceability in line with audit requirements under the implementing acts
All audit trails and verification proofs shall be compatible with the logging and evidence requirements set out in future Implementing Acts on verifiable credentials and integrated with national supervision mechanisms where required.

### 4.2 Verification Proof
This chapter defines the principles and structure of a verification proof, serving as auditable evidence that a credential verification was executed at a specific point in time. As it is produced by the relying party, for the relying party and relevant backend processes, it encapsulates the information required by those. For the credential holder, the EUDI Wallet transaction log will show that the exchange took place and which parties were involved. These two registrations of the transaction ensure that both relying parties and credential holders can demonstrate that a legitimate verification took place, in line with legal, procedural, and technical requirements of social security coordination across Member States. 
The verification proof is of utmost importance in the case of the cost reimbursement process triggered by a verification situation concerning the EHIC.
#### 4.2.1	OBJECTIVES
-	Enable provable and non-repudiable proof that a verification occurred.
-	Support alignment with Member State audit and accountability frameworks.
-	Build on the shared business data block structure used in social security credentials (see chapter 7).
-	Ensure compatibility with SD-JWT-based selective disclosure mechanisms.
#### 4.3.2	STRUCTURE OF A VERIFICATION PROOF
A verification proof must include the following components:
-	Verification Metadata: Timestamp
-	Identifiers of the authorised verifier or authorised intermediary, traceable to EU or national trusted list.
-	Presented Attestation Attributes: The common business data fields used in ESSPASS (see chapter 7.2.2) to reference the holder, the authentic source, the issuer and the document.
-	Cryptographic Signature: A digital signature by the verifier, binding all proof elements together and ensuring integrity and authenticity.
-	Status: An information on the status of the verification.
#### 4.3.3	TECHNOLOGICAL CONSIDERATIONS
-	Verification proofs must be cryptographically verifiable 
-	The proof can be optionally anchored in a distributed ledger or national registry, depending on Member State implementation choices.
-	Reuse of existing credential status endpoints may be leveraged for proof retrieval or audit trails, without exposing personal data.
#### 4.2.4	SECURITY AND PRIVACY
-	Verification proofs must not contain personal data; instead, they rely on references and pseudonymised elements.
-	Holders must be able to tetain local registrations of the interactions in their wallet for self-audit or to dispute resolution purposes. This is mandatory as part of the privacy dashboard according to eIDAS and ARF.
-	All verification proofs must comply with GDPR and relevant national data protection laws.
#### 4.2.5	INTEGRATION WITH VERIFICATION POLICY
Verification proofs are policy-bound. They inherit context from the applicable verification policy (see chapter 4.2) and must reference the policy version under which the verification was conducted. This binding ensures clarity on the expected data, verifier roles, and legal basis at the time of execution.



## 5 Trust anchors

*Mechanisms for the provision of a trust anchor that SHALL
be used for the verification of an attestation SHALL be defined in this section.*

*It is noted that the ARF specifies the following for QEAAs and Pub-EAAs*

> For PuB-EAAs, the Relying Party Instance verifies a PuB-EAA by first 
verifying the signature of the PuB-EAA Provider over the PuB-EAA, using the 
PuB-EAA Provider certificate issued by a QTSP. Subsequently, the Relying Party 
Instance verifies the signature over this certificate, using the corresponding 
trust anchor from the QTSP Trusted List. Note that both the PuB-EAA Provider 
and the QTSP may use an intermediate signing certificate. All other things 
being equal, the verification of a PuB-EAA will therefore involve one or more 
extra certificates, compared to the verification of a PID or QEAA.

----------------------

### 5.1	Core elements of Trust
-	Accredited Issuers: Only competent authorities designated under national and EU law may issue PuB-EAA credentials.
-	Credential Format: SD-JWT VC (Verifiable Credentials based on Selective Disclosure for JSON Web Token, see https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/), aligned with the revised eIDAS regulation.
-	mdoc Compatibility: Proximity flow implementations should support the issuance and verification of Electronic Attestation of Attributes aligned with ISO/IEC 18013-5, to enable offline or near-field scenarios.
-	Wallet Binding: All credentials must be bound to the EUDI Wallet instance to ensure authentic holder identification.
-	Signature Trust Anchors: Issuers use cryptographic keys listed in EU-level or national trusted lists.
-	Selective Disclosure: Enables minimisation of data while preserving trustworthiness.
-	Revocation and Expiry Handling: Verification flows must support real-time checks of credential status.
-	Mutual Verification: Builds trust by establishing identity and rights.
-	Legal Foundation: Transparent and understandable legal basis for interactions between citizens and relying parties.
### 5.2	INTEROPERABILITY ASSURANCE
Interoperability is achieved through:
-	Use of standardised data models and versioned namespaces.
-	Adherence to eIDAS-ARF, PuB-EAA and EUDI Wallet specifications.
-	Common processes for issuance (OpenID for Verifiable Credential Issuance), verification (OpenID for Verifiable Presentations), and trusted list publication.
### 5.3	TRUSTED LIST AND METADATA SERVICES
The trust infrastructure includes two types of trusted lists specifically related to the social security domain, which are essential for the validation and interoperability of PuB-EAA credentials:
-	Issuer Trusted List: A list of all entities legally authorised to issue EHIC resp. PD A1 credentials. Includes their legal basis, credential types, and cryptographic key material.
-	Verifier Trusted List: Lists entities authorised to request, validate and accept credentials for the purpose of service provision, such as public authorities, healthcare providers, and social security institutions.

These trusted lists not only enable verifiers to check issuer authenticity, but also empower holders to verify that:
-	A credential was issued by a legitimate, trusted authority
-	The entity requesting or verifying a credential is authorised to do so
This bidirectional trust validation is essential to protect users against misuse, fraud, or phishing attempts, and ensures confidence in interactions across the PuB-EAA ecosystem.

In addition to these, other trusted lists relevant to the broader eIDAS trust ecosystem, such as those for PID providers, wallet providers, and qualified trust service providers (QTSPs), also play a critical role in the end-to-end credential lifecycle, particularly for identity verification and cryptographic trust anchors.
The trusted lists for issuers and verifiers shall be:
- Maintained by a designated authority (e.g., DG EMPL or delegated national body)
- Accessible via standard endpoints (e.g., JSON-based well-known URLs)
- Versioned and timestamped for auditability

Each participating Member State must maintain or reference:
- A trusted list of authorised issuers and verifiers
- Public metadata describing schemas, namespaces, and PID requirements
- Technical endpoints for revocation status, key material, and wallet compatibility



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

------------------
This chapter defines the requirements and mechanisms for revocation and status verification of PuB-EAA credentials, ensuring their trustworthiness and lifecycle integrity in alignment with the eIDAS 2.0 Regulation and its relevant implementing acts.
### 6.1	OBJECTIVES
-	Ensure verifiers can reliably determine the validity status of a credential at the time of presentation.
-	Support real-time and offline revocation checking in both proximity and non-proximity flows. For offline checks, the definition of an acceptable cache age to ensure timely validation is required..
-	These revocation processes must align with the Implementing Acts adopted under Articles 24 and 45 of Regulation (EU) 2024/1183 and shall comply with technical specifications defined in the ARF and associated Commission acts on credential status checking mechanisms.
### 6.2	REVOCATION REQUIREMENTS
PuB-EAA credentials in social security must support revocation mechanisms that:
-	Allow the issuing entity (or one acting on behalf of a competent public body) to  to revoke a credential when it is no longer valid (e.g., due to expiry, change in entitlement or fraud).
-	Are machine-readable, versioned, and aligned with the semantics defined in the implementing acts.
-	Reflect changes in holder status or institutional authorisation that affect credential validity.
### 6.3	SUPPORTED METHODS
In the social security domain, the status of a PuB-EAA document on a revocation list is limited to binary values - either valid or revoked. Although the revocation model is functionally binary, it is implemented using the W3C-compliant StatusListCredential structure. This approach ensures complicance with the ARF and eIDAS implementing acts, while offering a scalable and privacy-preserving solution suitable for both offline and proximity-based use cases. 
The credential must include a credentialStatus claim (or property) that references a revocation list, typically implemented as a W3C-compliant StatusListCredential.

    "credentialStatus": {
        "id": "https://issuer.example.org/status/ehic-slc-01#list=1052",
        "type": "StatusList2021Entry",
        "statusPurpose": "revocation",
        "statusListIndex": "1052",
        "statusListCredential": "https://issuer.example.org/status/ehic-slc-01"
    }

The credentialStatus is a mandatory metadata field in Verifiable Credentials (when revocation is supported). The use of credentialStatus must also conform to Annex II of the eIDAS 2.0 Regulation, and relevant ARF guidelines on privacy-preserving revocation, including support for proximity/offline flows. It references an external resource (a status list), not the actual status value and it conforms to W3C Verifiable Credentials Data Model (VCDM) and ARF guidance.
Verifiers must receive only a privacy-preserving proof of validity, and all status checking should be performed internally by the holder’s wallet. Where feasible, issuers may rotate status list indexes or update list structures to further reduce correlation risks. These safeguards are essential to prevent cross-context tracking and uphold GDPR-compliant handling of social security entitlements.
In proximity flows (e.g., offline), wallets or relying party (verifier) instances may use pre-fetched revocation lists or signed status snapshots, ensuring validation without connectivity.



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








 
