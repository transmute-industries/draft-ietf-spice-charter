## Introduction

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, and transparency, such as digital licenses or certificates of origin.

A digital credential expresses claims or attributes about a subject, such as their name or age, and their cryptographic keys.
Some sets of claim names have already been defined by the IETF and other standards development groups (e.g., OpenID Foundation).
Digital credentials typically involve at least three entities:

* An "issuer", an entity (person, device, organization, or software agent) that constructs and secures digital credentials.
* A "holder", an entity (person, device, organization, or software agent) that controls the disclosure of credentials.
* A "verifier", an entity (person, device, organization, or software agent) that verifies and validates secured digital credentials.

In some contexts, holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values. 

When disclosed by an entity, a proof of the digital credential needs to be provided and verified, so that only the legitimate holder of the digital credential can take advantage of its possession.

Some holders may wish to carry more than one digital credential.
These credentials, together with associated key material, can be stored in an identity digital wallet.

The W3C has published the 'Verifiable Credentials Data Model v2.0' specification (VCDM) with data serialization in JSON-LD.  In this charter, the VCDM defined concept of “verifiable credential” and “verifiable presentation” is captured using the wording "digital credential" and "digital presentation" respectively.


## Goal

The SPICE WG will profile existing IETF technologies and address residual gaps that would enable their use in digital credentials and presentations.

- The JOSE WG is already standardizing the token format for unlinkability & selective disclosure in the form of JWP/CWP (draft-ietf-jose-json-web-proof). The SPICE WG will profile theses token formats for use with digital credentials. 


- The OAUTH WG is already standardizing the token format for unlinkability & selective disclosure in the form of SD-JWT/SD-JWT-VC (draft-ietf-oauth-selective-disclosure-jwt and draft-ietf-oauth-sd-jwt-vc). The SPICE WG will define SD-CWT/SD-CWT-VC, analogs for these JWT-based tokens but based on CWT. 


The SPICE WG, coordinates with RATS, OAuth, JOSE, COSE and SCITT working groups that develop documents related to the identity and credential space. The SPICE WG builds on cryptographic primitives defined in the CFRG (e.g., BBS Signatures) and does not define novel cryptographic schemes.

The SPICE WG will not develop digital credentials for any particular use case.  The general purpose profiles the WG will define will enable credential issuers to more easily build on existing IETF technologies.

## Program of Work

* An informational Architecture that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations) and the essential communication patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier. 

* Proposed standard documents for digital credential profiles covering JWP and CWP (from JOSE) that enable digital credentials with unlinkability and selective disclosure. This work will include registering claims that are in the JWT and CWT registries to enable digital credentials to transition from one security format to another (i.e., JSON/CBOR). 
* Proposed standard document defining SD-CWT, a profile of CWT inspired by SD-JWT (from OAuth) that enables digital credentials with unlinkability and selective disclosure.



* A proposed standard Metadata Discovery protocol using HTTPS/CoAP for CBOR-based digital credentials to enable the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credential types and proofs.  The design will be inspired by the OAuth "vc-jwt-issuer" metadata work (draft-ietf-oauth-sd-jwt-vc) which supports ecosystems using JSON serialization.

## Milestones

* 04 2025 - Submit an informational Architecture document to the IESG for publication
* 10 2025 - Submit a proposed standard document covering a JWP/CWP profile for digital credentials  to the IESG for publication
* 10 2025 - Submit a proposed standard document defining SD-CWT to the IESG for publication
* 03 2026 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication

