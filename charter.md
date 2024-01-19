# Secure Patterns for Internet CrEdentials (SPICE) at IETF - Proposed Charter

## Introduction

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, and transparency, such as digital licenses or certificates of origin.

A digital credential expresses claims or attributes about a subject, such as their name or age, made my an authority known as an issuer, such as a government agency.

The term "holder" is used to describe an entity that controls disclosure of credentials.

In some contexts, holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values.

When received by an entity, a proof of the digital credential needs to be provided and verified, so that only the legitimate controller of the digital credential can take an advantage of its possession.

The use of Trusted Applications (TAs) supported by a Trusted Execution Environment (TEE) may be essential for some use cases in order to provide a proof of control of a digital credential.

Some holders may wish to carry more than one credential. These credentials, together with associated key material, can be stored in a identity digital wallet.


## In-Scope

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

## Background

W3C has introduced a 'Three Role Model' in the 'Verifiable Credentials Data Model v2.0' specification. VCDM 2.0 (https://w3c.github.io/vc-data-model)
with the following roles: a holder, an issuer and a verifier.

The wording "Verifiable Credential" (VC) is used in VCDM 2.0. It implies the use of data serialization using JSON-LD.
The wording "Verifiable Presentation" (VP) is used in VCDM 2.0. It implies the use of data serialization using JSON-LD.

In this charter, the VC concept is captured using the wording "digital credential", while the VP concept is captured using the wording "digital presentation".

Some sets of claim names are registered with IANA and originate from the IETF, OIDF and other standards organizations.

For example, [jwt](https://www.iana.org/assignments/jwt/jwt.xhtml) and [cwt](https://www.iana.org/assignments/cwt/cwt.xhtml) both contain expressions for "subject" and "issuer", while the JWT registry has claims such as "name" and "email address", the CWT registry has claims regarding devices, such as "Software Measurement Results", and "Certifications received as Digital Letters of Approval".

IETF working groups and IRTF research groups have developed foundational building blocks with [BBS Signatures](https://datatracker.ietf.org/doc/draft-irtf-cfrg-bbs-signatures/), [RSA Blind Signatures](https://datatracker.ietf.org/doc/rfc9474/), [Verifiable Random Functions](https://datatracker.ietf.org/doc/rfc9381/),
or other [Selective-Disclosure](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/) and collection limitation techniques.

The SPICE WG intends to consume cryptographic systems produced by CFRG, similar to how those schemes are consumed in JOSE and COSE.

The SPICE WG will not develop novel cryptographic schemes, but might provide comments on use cases for schemes under development in CFRG.

## Deliverables

Documents produced by the working group will include the following:

### Architecture

An architecture document that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations), and the essential communciation patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier. The architecture will also cover the extensibility points, such as discovering key material associated with the roles (to enable digital signatures, proofs and encryption), formats such as JSON and CBOR based claims, and protocols, such as the various ways to transport credentials and presentations. The architecture will not define new key formats, credential formats, or protocols, but it will express how their evolution can support digital credential improvements over time.

Related Drafts:

- https://datatracker.ietf.org/doc/draft-steele-spice-profiles-bcp/
- https://datatracker.ietf.org/doc/draft-steele-spice-transparency-tokens/

### Metadata Discovery

A meta-data discovery document enabling the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credentials and proofs.
With high probability this will build on HTTP, but with some consideration for constrained devices, and with a good deal of inspiration from recent HTTP work in OAuth, for example the "vc-jwt-issuer" metadata work in [draft-ietf-oauth-sd-jwt-vc](https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/), but without being limited to JSON.

Related Drafts:

- https://datatracker.ietf.org/doc/draft-steele-spice-metadata-discovery/
- https://datatracker.ietf.org/doc/draft-steele-spice-oblivious-credential-state/
- https://datatracker.ietf.org/doc/draft-steele-spice-vcard-credentials/

### Selective Disclosure of Claims

A document specifying the selective disclosure of claims in a secure and privacy-friendly manner.
This document will cover the details of making presentations of credentials, the traceability considerations for different cryptographic approaches, and concrete serialization guidance enabling support for CBOR based versions of SD-JWT or similar approaches, building on BBS.
We expect this document to address features relevant to digital credentials that have been exclusively implemented in JSON or CBOR, and provide an integrated concrete approach for JSON and CBOR based credentials.

Related Drafts:

- https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/
- https://datatracker.ietf.org/doc/draft-steele-spice-transparency-tokens/

## Milestones

- 10 2024 - Submit an informational Architecture document to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Selective Disclosure of Claims to the IESG for publication
  
## Coordination

Coordination with CFRG, RATS, OAuth, JOSE, COSE, and SCITT are important to ensure that the latest work at IETF is leveraged.
Feedback from experts in other IETF working groups is gathered in the SPICE WG without creating fragments of credential work spread across several existing places in the IETF. 
Additionally, the SPICE WG will coordinate with other organizations that have specific documents or working groups targeting the definition or application of digital credentials.

