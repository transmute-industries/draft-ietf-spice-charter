# Secure Patterns for Internet CrEdentials (SPICE) at IETF - Proposed Charter

## Introduction

Digital credentials based on IETF standards have use cases ranging from personal credentials, such as drivers licenses and vaccination proofs, to business-to-business or business-to-government applications.
One example is fraud and counter-fitting prevention in cross-border trade documents by protecting digital representations of mill test reports, bills of materials, bills of lading, or commercial invoices.

These scenarios were addressed with registered claim names in JOSE and COSE, but resulting solution have lead to fragmented approaches, where each working group rediscovers the essential architecture and conventions necessary for issuers to make claims about subjects.

In order to meet privacy, security, and sustainability objectives, digital credentials need to be designed with awareness of computation and storage constraints associated with their use cases.
The SPICE WG focuses on a few explicit higher level objectives: unreliability enabling trustworthy exposition of minimal required information to prevent correlation and other attacks, selective disclosure enabling controlled exposition and a authorized subset of likability, a well-curated, concise claim vocabulary enabling cross-domain interchangeability via registration authorizes (i.e., IANA).
These objectives can be achieved by leveraging industry adopted standards and managing trade-offs between cutting-edge and well-established cryptography.

As a guiding principle for the SPICE WG, claims that work well in JSON must work well in CBOR, without loss of semantics. Compact expressions of claims consume less resources and expose less attack surface, these properties are in support sustainable design.

The SPICE WG will support digital credential formats leveraging existing IETF standards and IANA registries, and create a framework for consistently extending them to support stakeholders that are building compliance and automation systems based on industry adopted cryptography and protocols.

Digital credentials are identity documents with attributes (public or private claims in IANA registries) about the identity. The identifiers referenced could be about any subject, but common examples include people, devices, assets, organizations and processes.

Examples of producing and consuming digital credentials with the "Three Role Model" include credential endorsement by third parties, credential trustworthiness via remote attestation evidence appraisal for issuers, or credential transparency via notarization.

## Goals

Coordination with RATS, OAUTH, JOSE, COSE, and SCITT are important to ensure that the latest work at IETF is leveraged. Feedback from experts in other IETF working groups is gathered in the SPICE WG without creating fragments of credential work spread across several existing places in the IETF. Additionally, the SPICE WG will coordinate with other SDOs, such as ISO or W3C, on data model elements needed to support existing credential use cases.

### In-Scope

The work of the SPICE WG aligns JWT and CWT registered claim names for use with the 'Three Role Model' as introduced by W3C's 'Verifiable Credentials Data Model v2.0' specification (https://w3c.github.io/vc-data-model/#roles).

The SPICE WG will develop a framework in support of the 'Three Role Model', selective disclosure, and unlinkability.
The framework will provide an architecture that enables consistent application of JOSE and COSE, similar to the work done in https://datatracker.ietf.org/doc/html/draft-ietf-rats-eat-21#name-eat-as-a-framework and https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof.
The intent is also to apply lessons learned from the development of W3C's 'Securing Verifiable Credentials using JOSE and COSE' specification (https://www.w3.org/TR/vc-jose-cose), and extend them to non JSON-LD based payloads, specifically CWT Claim Sets, or other CBOR data structures.

A short list of lessons learned:
1. Expressive data models, such as RDF, are not necessarily suitable for
   all use-cases outside W3C
2. Reusing existing semantics that fit the domain well, such as provided by
   the JWT/CWT Claims registry, provide can improve interoperability,
   significantly
3. Focussing on crisp technical specifications and producing separate
   informative guidance documents helps to keep technical interested parties
   involved
4. Compact encoding matters and aligning JSON and CBOR provides
   the basis for simpler interoperability and smaller specification

### Out-of-Scope

The working group will NOT address transport protocols, such as those developed at OAUTH, OIDF, W3C or ISO in the scope of its initial charter.
The working group will NOT address specific credential use cases, such as "personal credentials" or "software supply chain".
The SPICE WG's work items will not require nor forbid the use of JSON-LD. Retaining semantic interchangeability is not in-scope. Newly registered claims will have broader applicability, to both JWT and CWT use cases.

## Key Design Properties of Digital Credentials

- Unlinkability (preventing tracking while proving attributes / capabilities)
- Selective Disclosure (supporting user agency, data minimization, redaction)
- Authenticity (ensuring information is trustworthy and can be authenticated)
- Integrity (ensuring tampering with information is always evident)
- Confidentiality (ensuring information is protected from unauthorized access)
- Availability (efficiently information processing, minimizing data in flight, reducing carbon cost for storage and transmission, and supporting offline / paper credential use cases)
- Semantic interchangeability (ensuring terms are understood and used consistently, in a global or local context)
- Usability and Feasibility ( The core operations must be easy to understand and use, and possible to integrate with existing platforms)

## Motivating Factors for conducting this work at IETF

- Privacy and security expertise at IETF / IRTF specifically relevant to this work
- Anticipated successful conclusion of the VC 2.0 Working Group at W3C

## Work Items

Documents produced by the working group will include the following:

- Architecture document
    - addressing the desired properties of "digital credentials"
    - commenting on registries
    - commenting on proof type (signatures, detecting duplicity, non equivocation, unlinkability, redactability)
- Unlinkabilty of SD/VC with CWTs (TBD )
- Selective Disclosure with CWTs https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/

## Inspiring Input Documents

- Use case document https://datatracker.ietf.org/doc/draft-prorock-spice-use-cases/ 
- Unlinkable Selective Disclosure with JWPs https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof/
- Proofs of Inclusion / Consistency - https://datatracker.ietf.org/doc/draft-ietf-cose-merkle-tree-proofs/
- Countersignatures - https://datatracker.ietf.org/doc/html/rfc9338
- TBD Identity Specification inspired by
    - KEYTRANS
    - (JWK Thumbprint URI, jkt) https://datatracker.ietf.org/doc/rfc9278/ 
    - (COSE Key Thumbprint URI, ckt) https://datatracker.ietf.org/doc/draft-ietf-cose-key-thumbprint/

Based on conversations on OAUTH and SPICE lists, while the following items are currently adopted by OAUTH,
they might become potential candidates to be moved to a SPICE WG, pending WG forming:

- JWT and CWT Status List https://datatracker.ietf.org/doc/draft-looker-oauth-jwt-cwt-status-list/
- SD-JWT-based Verifiable Credentials (SD-JWT VC) https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/


## Milestones

MM YYYY - Submit a Use Case and Terminology document to the IESG for publication
MM YYYY - Submit an Architecture document to the IESG for publication
MM YYYY - Submit a document covering selective disclosure with COSE to the IESG for publication

## Why IETF

Because of the security and integrity aspects directly involved in verifiable credentials that utilize a "Three Role Model", particularly their reliance on asymmetric cryptography with possible intermediaries during exchange, this topic must be worked with in cooperation with existing security expertise in the IETF and IRTF.  The broader community engaging in the verifiable credential space is converging within the IETF because of this security expertise. Multiple editors of existing work in W3C related to verifiable credentials are engaged and supportive of this work, and believe that IETF is the appropriate location for this work. By working in IETF we can ensure broader engagement with the work, security, and privacy review by the appropriate experts at IETF, and better coordinate with IETF groups that are leveraging or extending this work for use in various IETF standards.

## Relationship with W3C VCWG
The VCWG, which developed the 'Three Role Model' and defined the 'Verifiable Credentials Data Model v2.0' specification (https://w3c.github.io/vc-data-model/#roles) has created a JSON-LD data model and is defining mechanisms to secure this JSON-LD data model. It is anticipated that JSON-LD credentials will continue to be developed in the VCWG and the W3C. SPICE will concern itself with JSON, CBOR and other formats of digital credentials that may be required by IETF use cases.

