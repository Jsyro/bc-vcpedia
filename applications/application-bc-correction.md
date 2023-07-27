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

[Glossary - General Trust Over IP Terms](https://trustoverip.github.io/toip/glossary)

## 1.2. Governing Authority
BC Corrections is the Governing Authority responsible for this Governance Framework. The contact information for BC Corrections during the pilot phase of development is:
Name: Tiffany Wise, Assistant Deputy Warden OCC

## 1.5 Administoring Authority
TBD

## 1.6 Purpose
The purpose of this GF is to describe the rules, requirements, policies and procedures for the verification of an accredited lawyer by the Law Society of British Columbia using BC Wallet and the mobile verifier in BC Wallet.

##1.7 Scope
This document does not describe the GF for the verifications processes outside the use of BC Wallet.

## 1.10 Objectives
The objectives of this GF is to be transparent in describing the rules, requirements, policies and procedures for the verification of an accredited lawyer by the Law Society of British Columbia using BC Wallet and the mobile verifier in BC Wallet. Individuals listed under Key Roles can review this document and acquire their respective information. 

## Principles
TBD

## General Requirements
A Corrections Reception Team Member must be able to verify with confidence a person’s identity and a lawyer member’s status using the BC Wallet mobile verifier. The person’s identity must be from the Person credential that’s issued by Service BC and their lawyer member status from their Member Card issued by the Law Society of BC. Their names and photo ID presented on those two digital credentials must match the individual. 

# 2. Risk and requirements
## 2.1 Risk Assessment
TBD 

Number | Risk | Description | Probability | Severity | Actions to mitigate
--- | --- | --- | --- | --- | --- 

## 2.2 Governance Requirements
TBD

Number | Requirements | Notes
--- | --- | ---

## 2.3 Business Requirements
TBD

Number | Requirements | Notes
--- | --- | ---

## 2.4 Technical Requirements
TBD

Number | Requirements | Notes
--- | --- | ---

## 2.5 Presentation request definition
 ID: TBD
 Name: TBD
 Version TBD

### Requested attributes
Schema Name: Person
Issuer DID: RGjWbW1eycP7FrMf4QJvX8
Schema version 1.0
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
