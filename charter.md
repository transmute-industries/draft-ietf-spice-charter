# Secure Patterns for Internet CrEdentials (SPICE) at IETF - Proposed Charter

## Introduction

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, and transparency, such as digital licenses or certificates of origin.

A digital credential expresses claims or attributes about a subject, such as their name or age, and their cryptographic keys.  Some sets of claim names have already been defined by the IETF and other standards development groups (e.g., OpenID Foundation).  Digital credentials typically involve at least three entities:

- An "issuer", an entity (person, device, organization, or software agent) that constructs and secures digital credentials.
- A "holder", an entity (person, device, organization, or software agent) that controls the disclosure of credentials.
- A "verifier", an entity (person, device, organization, or software agent) that verifies and validates secured digital credentials.

In some contexts, holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values. When disclosed by an entity , a proof of the digital credential needs to be provided and verified, so that only the legitimate holder of the digital credential can take advantage of its possession.

Some holders may wish to carry more than one digital credential. These credentials, together with associated key material, can be stored in an identity digital wallet.

The W3C has published the 'Verifiable Credentials Data Model v2.0' specification (VCDM) with data serialization in JSON-LD.  In this charter, the VCDM defined concept of “verifiable credential” and “verifiable presentation” is captured using the wording "digital credential" and "digital presentation" respectively.

## Goal

The SPICE working group will develop a framework and recommendations for deploying digital credentials based on JOSE and COSE.

The following topics will be considered in the milestones:

- Unlinkability (preventing tracking while proving attributes / capabilities)
- Selective Disclosure (supporting user agency, data minimization, redaction)
- Authenticity (ensuring information is trustworthy and can be authenticated)
- Confidentiality (ensuring information is protected from unauthorized access)
- Hardware Assurance (awareness of the security capabilities of issuers, holders and verifiers, and consideration of TEEs (Trusted Execution Environments))
- Availability (efficiently information processing, minimizing data in flight, reducing carbon cost for storage and transmission, and supporting offline / paper credential use cases)
- Semantic interchangeability (ensuring terms are understood and used consistently, in a global or local context)
- Accountability (what format and protocol considerations can help mitigate abusive or excessive requests for credential presentation?  What mitigates abuse by issuers?)
- Integrity (ensuring tampering with information is always evident)
- Usability and Feasibility (the core operations must be easy to understand and use, and possible to integrate with existing platforms)

The WG will coordinate with RATS, OAuth, JOSE, COSE and SCITT working in related areas in the identity and credential space.  The WG will also build on cryptographic primitives defined in the CFRG (e.g., BBS Signatures) and will not define novel cryptographic schemes.

## Program of Work

The WG will focus on the following program of work.

### Architecture

An architecture document that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations), and the essential communication patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier. 


### Metadata Discovery

A meta-data discovery document enabling the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credentials and proofs.
With high probability this will build on HTTP, but with some consideration for constrained devices, and with a good deal of inspiration from recent HTTP work in OAuth, for example the "vc-jwt-issuer" metadata work in [draft-ietf-oauth-sd-jwt-vc](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/), but without being limited to JSON.


### Selective Disclosure of Claims

A document specifying the selective disclosure of claims in a secure and privacy-friendly manner.
This document will cover the details of making presentations of credentials, the traceability considerations for different cryptographic approaches, and concrete serialization guidance enabling support for CBOR based versions of SD-JWT or similar approaches, building on BBS.
We expect this document to address features relevant to digital credentials that have been exclusively implemented in JSON or CBOR, and provide an integrated concrete approach for JSON and CBOR based credentials.


## Milestones

- 10 2024 - Submit an informational Architecture document to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Selective Disclosure of Claims to the IESG for publication
