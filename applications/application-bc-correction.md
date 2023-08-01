---
layout: default
title: Okanagan Corrections Centre Governance Framework - Draft
parent: Applications
---

## Okanagan Corrections Centre Governance Framework - Draft

# 1. Primary Document

## 1.1. Introduction 
Digital credentials will allow Corrections Reception Team Members to be more confident that the individual they are providing access to is a lawyer in good standing.
Currently, Corrections Reception Team Members verify that the individual is a lawyer in good standing by looking at the individual’s Law Society of BC (LSBC) card, and then looking them up on the LSBC web site directory.
This document details the Governance Framework (GF) for [BC Corrections](https://www2.gov.bc.ca/gov/content/justice/criminal-justice/corrections) as an actor involved in the verification of verifiable credentials (VC) with the mobile verifier in BC Wallet.

## 1.2. Terminology and Notation 

Please reference [Glossary - General Trust Over IP Terms](https://trustoverip.github.io/toip/glossary)

Please reference the [Terminology - Verifiable Credential Data Model](https://www.w3.org/TR/vc-data-model/#terminology)

Terms | Description 
--- | --- |
Requirements | Include any combination of Machine-Testable Requirements and Human-Auditable Requirements.
Machine-Testable Requirements | Requirements in which compliance can be verified using an automated test suite and appropriate scripting or testing software.
Human-Auditable Requirements | Requirements in which compliance can only be verified by an audit of people, processes, and procedures.
Policies | Human-Auditable Requirements written using standard conformance terminology. The Policies used in the Governance Framework will use the standard terminology detailed in RFC 2119 keywords. Note that all RFC 2119 keywords have weight from an auditing perspective. An implementer MUST explain why a SHOULD or RECOMMENDED requirement was not implemented and SHOULD explain why a MAY requirement was implemented.
Specifications | A document containing any combination of Machine-Testable Requirements and Human-Auditable Requirements needed to produce technical interoperability.

## 1.2. Governing Authority
BC Corrections is the Governing Authority responsible for this Governance Framework. The contact information for BC Corrections during the pilot phase of development is:
Name: Tiffany Wise, Assistant Deputy Warden OCC

## 1.5 Administoring Authority
*The party tasked with operating the management of a particular governance framework. The administering authority may or may not be the governing authority. For example, a government may be the governing authority for a governance framework administered by an NGO as the administering authority.*

## 1.6 Purpose
The purpose of this GF is to describe the rules, requirements, policies, and procedures for the verification of an accredited lawyer by the Law Society of British Columbia using digital credentials.

##1.7 Scope
BC Corrections is a participant in an open ecosystem and the focus of this framework is to describe the process BC Corrections uses for digital exchanges on Indy networks.

## 1.10 Objectives
The objective of this GF is to be transparent in describing the rules, requirements, policies and procedures for the verification of an accredited lawyer by the Law Society of British Columbia using digital credentials. Individuals listed under Roles can review this document and acquire their respective information. 

## Principles
*This section states the principles by which all members of the trust community agree to abide. It:*

1.	*SHOULD serve as a guide to the development of policies, rules, and other requirements in the GF ("principles guide policies").*
2.	*SHOULD, if applicable, refer to previously existing principles (whether defined by ToIP or other sources).*
3.	*SHOULD be referenced (along with any other relevant parts of the GF) in any Legal Agreement so as to help clarify intent.*
4.	*MUST NOT include requirements (e.g., using capitalized RFC 2119 keywords) for which either human or machine conformance can be directly tested — those MUST be stated as policies or rules elsewhere in the GF.*


## General Requirements
A Corrections Reception Team Member must be able to verify with confidence a person’s identity and a lawyer member’s status using the BC Wallet mobile verifier. The person’s identity must be from the Person credential that’s issued by Service BC and their lawyer member status from their Member Card issued by the Law Society of BC. Their names and photo ID presented on those two digital credentials must match the individual. 

# 2. Controlled Documents
## 2.1 Risk Assessment
TBD 

Number | Risk | Description | Probability | Severity | Actions to mitigate
--- | --- | --- | --- | --- | --- 
2.1.1 | Security guard uses BC Wallet on their personal device | Security guard retires and leaves with work data | Low | High | BC Wallet will not retain any proof request data after the interaction is complete. Policy states that that verification must be used with a government issued device.
2.1.2 | Security guard makes a connection and reuses that connection to send proof requests with reoccurring lawyers | Security guard bypasses the data retention mitigation and proof request data is retained | Low | High | 
2.1.3 | Device with BC Wallet installed runs out of battery | Mobile verifier is inaccessible | High | Medium | Default back to traditional method of verification. Have a back-up mobile device
2.1.4 | Device with BC Wallet installed malfunctions | Mobile verifier is inaccessible | Low | Medium | Default back to traditional method of verification. Have back-up phone
2.1.5 | WiFi of facility is offline | Mobile verifier is inaccessible | Medium | Medium | Default back to traditional method of verification


## 2.2 Governance Requirements
TBD

Number | Requirements | Notes
--- | --- | ---
2.2.1 | Mobile verification will be done on a shared government issued mobile device. | To avoid the use of a personal device.
2.2.2 | Mobile verification will be done using BC Wallet | To avoid the use of a personal device.
2.2.3 | Support regarding the use of BC Wallet will be addressed by DITP | 
2.2.4 | Support regarding the verification processes will be addressed by OCC
2.2.5 | A Corrections Reception team member will not add a lawyer as a Contact on the shared mobile device in BC Wallet | Adding a contact will circumvent the data retention mitigation and data of interactions between the connection will be retained.
2.2.6 | A lawyer will not add the shared device used by a Correction Reception team member as a Contact | Adding a contact will circumvent the data retention mitigation and data of interactions between the connection will be retained.

## 2.3 Business Requirements
TBD

### 2.3.1 Roles
-	The verifier must be a Corrections Reception team member
-	The holder must be an accredited lawyer from the Law Society of BC

### 2.3.2 Tools
-	The verifier must use a shared government issued mobile device to install [BC Wallet](https://www2.gov.bc.ca/gov/content/governments/government-id/bc-wallet/help).
-	The verifier must use BC Wallet and the mobile verifier feature to verify digital credentials of the holder.

### 2.3.3 Data retention
-	BC Corrections must not retain any data shared by the holder.

### 2.3.4 Verification
-	When a holder identifies their scheduled appointment to access the corrections facility, the verifier must communicate the option to use digital credentials for verification. 
-	When verifying digital credentials, the verifier must use the tools to present a proof request to the holder.
-	The holder will scan the proof request with their BC Wallet to present their digital credentials.

Once the requested information has been sent to the verifier, the verifier must confirm:
-	The Member Status is Practising
-	The Member Status Code is PRAC
-	The photo ID matches the holder.
-	The Given Names and Family Name from the Person credential matches the Given Name and Surname of the Member card.

## 2.4 Technical Requirements
TBD

Number | Requirements | Notes
--- | --- | ---
2.4.1 | The BC Wallet mobile verifier on the shared mobile device used by OCC will not retain data of any proof requests | 
2.4.2 | The presentation request will not accept revoked credentials
2.4.3 | The presentation request will not accept non-production credentials
2.4.4 | The presentation request will be connectionless

## 2.5 Presentation request definition
 ID: TBD
 Name: TBD
 Version TBD

### Requested attributes
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
Member Status | Practising
Member Status Code | PRAC

PPID is not requested from the Member Card as it is not the actual Member Card number but a proxy specific to the digital credential. The Person credential is only requesting the person’s full name and picture for the purpose of name and picture matching. Other attributes in the Person credential would be irrelevant to this use case. 

___
