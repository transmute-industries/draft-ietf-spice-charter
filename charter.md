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

## Goal

The SPICE working group will:

- Register claims that are in JWT in the CWT registry to enable digital credentials to transistion from one security format to another.
- Develop a framework and recommendations for deploying digital credentials based on JOSE and COSE.
- Develop profiles of CWT/CWP, JWT/JWP (Digitial Credential Profiles) that enable the semantic interchangeability required by use cases, for example, the SPICE working group 
- define common conventions for key discovery (Metadata Discovery) that support verification and other issue, holder and verifier related capabilities.
- Coordinate with RATS, OAuth, JOSE, COSE and SCITT working in related areas in the identity and credential space.  The WG will also build on cryptographic primitives defined in the CFRG (e.g., BBS Signatures) and will not define novel cryptographic schemes.

## Program of Work

The SPICE working group will focus on the following program of work:

* An informational architecture document that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations) and the essential communication patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier. 
* A proposed standard HTTPS/CoAP based meta-data discovery document enabling the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credentials and proofs. With high probability this will build on HTTP, but with some consideration for constrained devices and with a good deal of inspiration from recent HTTP work in OAuth, for example, the "vc-jwt-issuer" metadata work in [draft-ietf-oauth-sd-jwt-vc](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/), but enabling CBOR and COSE based metadata formats.
* Proposed standards for digital credential profiles of security formats:
  * The JOSE WG is already standardizing the JWP/CWP token formats. This group
    will build upon those formats to deliver a profile of those token formats for
    use as digital credentials and digital presentations. See
    [draft-ietf-jose-json-web-proof](https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof/).
  * The OAuth WG is already standardizing JWT and SD-JWT. This group will build
    upon those formats to deliver a profile of those token formats for use as
    digital credentials and digital presentations.
  * The COSE WG is already standardizing CWT. This group will build upon that
    format to deliver a profile of that token format for use as digital
    credentials and digital presentations.
* A proposed standard for a token format based on CWT and SD-JWT that enables
  digital credentials with unlinkability and selective disclosure in CBOR.

## Milestones

- 12 2024 - Submit an informational Architecture document to the IESG for publication
- 03 2025 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication
- 03 2025 - Submit a document as a proposed standard covering Digitial Credential Profiles to the IESG for publication



