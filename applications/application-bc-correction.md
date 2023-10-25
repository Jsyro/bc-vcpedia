---
layout: default
title: Okanagan Corrections Centre Governance Framework - Draft
parent: Applications
---

## Okanagan Corrections Centre Governance Framework - Draft

# 1. Primary Document

## 1.1. Introduction 
This document details the Governance Framework (GF) for [BC Corrections](https://www2.gov.bc.ca/gov/content/justice/criminal-justice/corrections) as an actor involved in [verifiable credential](https://www.w3.org/TR/vc-data-model/#abstract) exchanges. 

Verifiable credentials will allow BC Corrections to be more confident and secure in delivering services to individuals. 

## 1.2. Terminology and Notation 

Please reference [Glossary - General Trust Over IP Terms](https://trustoverip.github.io/toip/glossary)

Please reference the [Terminology - Verifiable Credential Data Model](https://www.w3.org/TR/vc-data-model/#terminology)

Please reference the [Glossary of Criminal Justice Terms](https://www2.gov.bc.ca/gov/content/justice/criminal-justice/bcs-criminal-justice-system/justice-terms)

Terms | Description 
--- | --- |
Requirements | Include any combination of Machine-Testable Requirements and Human-Auditable Requirements.
Machine-Testable Requirements | Requirements in which compliance can be verified using an automated test suite and appropriate scripting or testing software.
Human-Auditable Requirements | Requirements in which compliance can only be verified by an audit of people, processes, and procedures.
Policies | Human-Auditable Requirements written using standard conformance terminology. The Policies used in the Governance Framework will use the standard terminology detailed in RFC 2119 keywords. Note that all RFC 2119 keywords have weight from an auditing perspective. An implementer MUST explain why a SHOULD or RECOMMENDED requirement was not implemented and SHOULD explain why a MAY requirement was implemented.
Specifications | A document containing any combination of Machine-Testable Requirements and Human-Auditable Requirements needed to produce technical interoperability.
BC Corrections Staff | A person employed by BC Corrections

## 1.2. Governing Authority
BC Corrections is the Governing Authority responsible for this Governance Framework. The contact information for BC Corrections during the pilot phase of development is:
Name: Tiffany Wise, Assistant Deputy Warden OCC

## 1.5 Administoring Authority
BC Corrections is the Adminstoring Authority responsible for this Governance Framework. The contact information for BC Corrections during the pilot phase of development is:
Name: Tiffany Wise, Assistant Deputy Warden OCC

## 1.6 Purpose
The purpose of this governance framework is to describe the rules/policies/procedures for verifiable credential exchanges involving BC Corrections with the open global community. The purpose of the rules is to enable all actors to understand agreed upon standards, terminology and processes that allow the community to interact with MMO in a trusted manner.

## 1.7 Scope
BC Corrections is a participant in an open ecosystem and the focus of this framework is to describe the process BC Corrections uses for digital exchanges on Indy networks.

## 1.10 Objectives
The objective of this GF is to be transparent in describing the rules/policies/procedures for verifiable credential exchanges involving BC Corrections with the open global community. Participating actors can review this document and acquire their respective information. 

## Principles
Please reference the [Basic principles of Canadian criminal law](https://www2.gov.bc.ca/gov/content/justice/criminal-justice/bcs-criminal-justice-system/understanding-criminal-justice/principles-and-sources-of-criminal-law/basic-principles)

Please reference the [Adult Custody Policy](https://www2.gov.bc.ca/gov/content/justice/criminal-justice/corrections/about-us/divisions/adult-custody)

Please reference the [Appropriate Use Policy](https://www2.gov.bc.ca/gov/content/governments/services-for-government/policies-procedures/appropriate-use-policy) 

## General Requirements
A BC Corrections Staff must be able to verify with confidence a person's qualitications through verifiable credential exchanges.

# 2. Controlled Documents
## 2.1 Risk Assessment
 
### 2.1.1 General Risks
Number | Risk | Description | Probability | Severity | Actions to mitigate
--- | --- | --- | --- | --- | --- 
2.1.1.1 | BC Corrections Staff uses BC Wallet on their personal device | BC Corrections Staff retires and leaves with work data | Low | High | The digital wallet will not retain any proof request data after the interaction is complete. Policy states that that verification must be used with a government issued device.
2.1.1.2 | BC Corrections Staff makes a connection and reuses that connection to send proof requests | BC Corrections Staff bypasses the data retention mitigation and proof request data is retained | Low | High | 
2.1.1.3 | Device with BC Wallet installed runs out of battery | Mobile verification is inaccessible | High | Medium | Default back to traditional method of verification. Have a back-up mobile device.
2.1.1.4 | Device with BC Wallet installed malfunctions | Mobile verifier is inaccessible | Low | Medium | Default back to traditional method of verification. Have back-up phone
2.1.1.5 | WiFi of Correction Centre is offline | Mobile verifier is inaccessible | Medium | Medium | Default back to traditional method of verification

### 2.1.2 Verification of Accredited Lawyer Risks
Number | Risk | Description | Probability | Severity | Actions to mitigate
--- | --- | --- | --- | --- | --- 
2.1.2.1 | Individual receives lawyer credential from an unverified Issuer | Credential could be fraudulent | Low | High | Presentation definition specifies Issuer DID
2.1.2.2 | Individual has their lawyer accreditation revoked | lawyer may be suspended or disbarred due to misconduct | Low | High | Presentation definition requires non-revoked digital credentials 

## 2.2 Governance Requirements

Number | Requirements | Notes
--- | --- | ---
2.2.1 | Mobile verification will be done on a shared government issued mobile device. | To avoid the use of a personal device.
2.2.2 | Mobile verification will be done using BC Wallet | To avoid the use of a personal device.
2.2.3 | Support regarding the use of BC Wallet will be addressed by DITP | 
2.2.4 | Support regarding the verification processes will be addressed by BC Corrections
2.2.5 | A BC Corrections Staff will not add an individual as a Contact on the shared mobile devices in BC Wallet | Adding a contact will circumvent the data retention mitigation and data of interactions between the connection will be retained.
2.2.6 | An individual will not add the shared mobile devices used by a Correction Reception team member as a Contact | Adding a contact will circumvent the data retention mitigation and data of interactions between the connection will be retained.
2.2.7 | Any individuals who add the shared mobile devices used by a BC Corrections Staff will be removed as a Contact from the shared mobile device | Removing contacts from BC Wallet deletes the connection
2.2.8 | BC Corrections Staff are not allowed their personal mobile device at their station | 

## 2.3 Business Requirements

### 2.3.2 Tools
-	The Verifier must use a shared government issued mobile device to install [BC Wallet](https://www2.gov.bc.ca/gov/content/governments/government-id/bc-wallet/help).
-	The Verifier must use BC Wallet and the mobile verifier feature to verify digital credentials of the holder.

### 2.3.4 Verification of an Accredited Lawyer from the Law Society of British Columbia
-	When an individual (Holder) identifies their scheduled appointment to access the Corrections Centre, the BC Corrections Staff (Verifier) must communicate the option to use digital credentials for verification. 
-	When verifying digital credentials, the Verifier must use the tools to present a proof request to the Holder.
-	The Holder must scan the proof request with their BC Wallet to present their digital credentials.

Once the requested information has been sent to the verifier, the verifier must confirm:
-	The Member Status is Practising
-	The Member Status Code is PRAC
-	The Picture matches the Holder.
-	The Given Names and Family Name from the Person credential matches the Given Name and Surname of the Member card.

### 2.3.5 Verification of a Holder with name mismatch
If the Given names and Surname/Family Names of credentials do not match: 
- The Holder will need to provide another form of ID with names matching.

## 2.4 Technical Requirements

Number | Requirements | Notes
--- | --- | ---
2.4.1 | The BC Wallet mobile verifier on the shared mobile device used by BC Corrections will not retain data of any proof requests | 
2.4.2 | The presentation request will not accept revoked credentials
2.4.3 | The presentation request will not accept non-production credentials
2.4.4 | The presentation request will use ephemeral connections (a temporary connection that is deleted after the verifiable credential exchange is complete)

## 2.5 Presentation Request Definition
 ID: BC:5:PracticingLawyerAndPhoto:0.0.1:indy
 
 Name: Lawyer Status and Photo

### Requested Attributes
Schema Name: Person

Issuer DID: RGjWbW1eycP7FrMf4QJvX8

Schema version: 1.0

Restrictions: non-revoked

Attribute | Value
--- | ---
given_names | 
family_name | 
Picture | 

Schema Name: Member Card

Issuer DID: 4xE68b6S5VRFrKMMG1U95M

Schema version: 1.5.1

Restrictions: non-revoked

Attribute | Value
--- | ---
Given Name | 
Surname | 
Member Status | 
Member Status Code | 

PPID is not requested from the Member Card as it is not the actual Member Card number but a proxy specific to the digital credential. The Person credential is only requesting the person’s full name and picture for the purpose of name and picture matching. Other attributes in the Person credential would be irrelevant to this use case. 

___
