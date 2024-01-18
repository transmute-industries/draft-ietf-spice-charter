# Secure Patterns for Internet CrEdentials (SPICE) at IETF - Proposed Charter

## Introduction

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, transparency, such as digital licenses or certificates of origin.

In some contexts, holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values.
When received by an entity, a proof of the digital credential needs to be provided and verified, so that only the legitimate controller of the digital credential can take an advantage of its possession. The use of Trusted Applications (TAs) supported by a Trusted Execution Environment (TEE) may be essential for some use cases in order to provide a proof of control of a digital credential
Some holders may wish to carry more than one credential. These credentials, together with associated key material, can be stored in a identity digital wallet.

## Background

W3C has introduced a 'Three Role Model' in the 'Verifiable Credentials Data Model v2.0' specification. VCDM 2.0 (https://w3c.github.io/vc-data-model)
with the following roles: a holder, an issuer and a verifier.

The wording "Verifiable Credential" (VC) is used in VCDM 2.0. It implies the use of a schema defined using JSON-LD.
The wording "Verifiable Presentation" (VP) is used in VCDM 2.0. It implies the use of data serialization using JSON-LD.

In this charter, the VC concept is captured using the wording "digital credential", while the VP concept is captured using the wording "digital presentation".

Some sets of claim names have been defined by the IANA and originate both from the IETF and the OIDF.

IETF and IRTF working groups have developed foundational building blocks with BBS Signatures, RSA Blind Signatures, Verifiable Random Functions,
or other Selective-Disclosure and collection limitation techniques.

## Key Design Properties of Digital Credentials

- Unlinkability (preventing tracking while proving attributes / capabilities)
- Selective Disclosure (supporting user agency, data minimization, redaction)
- Authenticity (ensuring information is trustworthy and can be authenticated)
- Confidentiality (ensuring information is protected from unauthorized access)
- Hardware Assurance (awareness of the security capabilities of issuers, holders and verifiers)
- Availability (efficiently information processing, minimizing data in flight, reducing carbon cost for storage and transmission, and supporting offline / paper credential use cases)
- Semantic interchangeability (ensuring terms are understood and used consistently, in a global or local context)
- Usability and Feasibility (the core operations must be easy to understand and use, and possible to integrate with existing platforms)
- Accountability (what format and protocol considerations can help mitigate abusive or excessive requests for credential presentation?  What mitigates abuse by issuers?)
- Integrity (ensuring tampering with information is always evident)
- Semantic interchangeability (ensuring terms are understood and used consistently, in a global or local context)
- Usability (the core operations must be easy to understand and use)

## Goals

Coordination with CFRG, RATS, OAuth, JOSE, COSE, and SCITT are important to ensure that the latest work at IETF is leveraged.
Feedback from experts in other IETF working groups is gathered in the SPICE WG without creating fragments of credential work spread across several existing places in the IETF. Additionally, the SPICE WG will coordinate with other SDOs, such as ISO or W3C, on data model elements or protocols needed to support existing credential use cases.

## In-Scope

The SPICE WG will develop a framework in support of the 'Three Role Model', considering in particular selective disclosure of attributes and unlinkability between verifiers. It will consider the use of TEEs (Trusted Execution Environments) for managing key material and digital credentials.

The intent is to apply lessons learned from the development of W3C's 'Securing Verifiable Credentials using JOSE and COSE' specification
(https://www.w3.org/TR/vc-jose-cose), and extend them to non JSON-LD based payloads, specifically JOSE or other CBOR data structures.

A short list of lessons learned:

1. Expressive data models, such as RDF, are not necessarily suitable for all use-cases outside W3C
1. Reusing existing semantics that fit the domain well, such as provided by the IANA registry, provide can improve interoperability, significantly
1. Focussing on crisp technical specifications and producing separate informative guidance documents helps to keep technical interested parties involved
1. Compact encoding matters and aligning JSON and CBOR may provide the basis for simpler interoperability and smaller specification


## Deliverables

Documents produced by the working group will include the following:

- An architecture document that defines the terminology (e.g., Issuer, Holder, and Verifier), the communication patterns between these parties, and the security/privacy properties.
- A meta-data discovery document enabling the 3 roles (issuers, holders and verifiers) to discover supported protocols and formats for keys, claims, credentials and proofs.
- A document specifying the selective disclosure of claims in a secure and privacy-friendly manner.

## Milestones

- 10 2024 - Submit an informational Architecture document to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Metadata Discovery to the IESG for publication
- 02 2025 - Submit a document as a proposed standard covering Selective Disclosure of Claims to the IESG for publication