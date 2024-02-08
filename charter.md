## Introduction

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, and transparency, such as digital licenses or certificates of origin.

A digital credential expresses claims or attributes about a subject, such as their name or age, and their cryptographic keys.
Some sets of claim names have already been defined by the IETF and other standards development groups (e.g., OpenID Foundation).
Digital credentials typically involve at least three entities:

- An "issuer", an entity (person, device, organization, or software agent) that constructs and secures digital credentials.
- A "holder", an entity (person, device, organization, or software agent) that controls the disclosure of credentials.
- A "verifier", an entity (person, device, organization, or software agent) that verifies and validates secured digital credentials.

In some contexts, holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values. When disclosed by an entity, a proof of the digital credential needs to be provided and verified, so that only the legitimate holder of the digital credential can take advantage of its possession.

Some holders may wish to carry more than one digital credential.
These credentials, together with associated key material, can be stored in an identity digital wallet.

The W3C has published the 'Verifiable Credentials Data Model v2.0' specification (VCDM) with data serialization in JSON-LD.
In this charter, the VCDM defined concept of “verifiable credential” and “verifiable presentation” is captured using the wording "digital credential" and "digital presentation" respectively.

The SPICE WG, coordinates with RATS, OAuth, JOSE, COSE and SCITT working groups that develop documetns related to the identity and credential space.  
The SPICE WG builds on cryptographic primitives defined in the CFRG (e.g., BBS Signatures) and does not define novel cryptographic schemes.

## Goal

The JOSE WG is already standardizing the token format for unlinkability & selective disclosure in the form of JWP/CWP.  The SPICE WG profiles this token format to define/standardize digital credentials formats. See [draft-ietf-jose-json-web-proof](https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof/).

The OAUTH WG is already standardizing the token format for unlinkability & selective disclosure in the form of SD-JWT/SD-JWT-VC.  The SPICE WG profiles this token format to define/standardize digital credentials formats, and support similar functionality for SD-CWT/SD-CWT-VC. See [draft-ietf-oauth-selective-disclosure-jwt](https://datatracker.ietf.org/doc/draft-ietf-oauth-selective-disclosure-jwt/) and [draft-ietf-oauth-sd-jwt-vc](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/).

The ACE WG is already standardizing CWT. This group will build upon that format to deliver a profile of that token format for use as digital credentials and digital presentations. See [RFC8392](https://datatracker.ietf.org/doc/html/rfc8392).

## Program of Work

* An informational architecture that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations) and the essential communication patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier. 

* A proposed standard for digital credential profiles covering JWT, SD-JWT, JWP, CWT, SD-CWT, that enable digital credentials with unlinkability and selective disclosure. Including registering claims that are in JWT in the CWT registry to enable digital credentials to transition from one security format to another. This document will deliver "token formats" (profiles of CWT/CWP, JWT/JWP), which are concrete instantiations of the security formats the SPICE WG is profiling. For CWP/JWP see [draft-ietf-jose-json-web-proof](https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof/). The credential profile document will address features relevant to digital credentials that have been exclusively implemented in JSON or CBOR and provide an integrated concrete approach for JSON and CBOR based credentials.

* A proposed standard for meta-data discovery protocol using HTTPS/CoAP, enabling the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credentials and proofs. Compatibility with the "vc-jwt-issuer" metadata work in [draft-ietf-oauth-sd-jwt-vc](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/), will be maintained, while the SPICE WG expands the approach to support CBOR and COSE based metadata formats.

## Milestones

- 12 2024 - Submit an informational Architecture document to the IESG for publication
- 03 2025 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication
- 03 2025 - Submit a document as a proposed standard covering Digitial Credential Profiles to the IESG for publication



