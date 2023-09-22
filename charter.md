# Secure Patterns for Internet CrEdentials (SPICE) at IETF - Proposed Charter

## Introduction

Digital credentials based on IETF standards have use cases ranging from personal credentials, such as drivers licenses and vaccination proofs, to business-to-business or business-to-government applications.
One example is fraud and counterfitting prevention in cross-border trade documents by protecting digital representations of mill test reports, bills of materials, bills of lading, or commercial invoices.

In order to meet privacy, security, and sustainability objectives, digital credentials need to be designed with awareness of computation and storage constraints associated with their use cases.
These objectives can be achieved by leveraging industry adopted standards and managing tradeoffs between cutting-edge and well-established cryptography.

The SPICE WG aims to support digitial credential formats based on existing IETF standards, and extend them to support stakeholders that are building compliance and automation systems based on industry adopted cryptography and protocols.

## Goals

Coordination with RATS, OAUTH, JOSE, COSE, SCITT and WIMSE are important to ensure that the latest work at IETF is leveraged. Feedback from experts in other IETF working groups is gathered in the SPICE WG without creating fragments of credential work spread accross several existing places in the IETF.

### In-Scope

The work of the SPICE WG aligns JWT and CWT registered claim names for use with the 'Three Role Model' as introduced by W3C's 'Verifiable Credentials Data Model v2.0' specification (https://w3c.github.io/vc-data-model/#roles).

The SPICE WG will develop a framework in support of the 'Three Role Model', selective disclosure, and unlinkability.
The framework will provide an architecture that enables consistent application of JOSE and COSE, similar to the work done in https://datatracker.ietf.org/doc/html/draft-ietf-rats-eat-21#name-eat-as-a-framework and https://datatracker.ietf.org/doc/draft-ietf-jose-json-web-proof.
The intent is also to apply lessons learned from the development of W3C's 'Securing Verifiable Credentials using JOSE and COSE' specification (https://www.w3.org/TR/vc-jose-cose), and extend them to non JSON-LD based payloads, specifically CWT Claim Sets, or other CBOR data structures.
<!--based on complementary work conducted in JOSE, COSE, and OAUTH, if possible. -->

Leveraging COSE enables reuse of valuable extensions, such as transparency service inclusion proofs, as defined in https://datatracker.ietf.org/doc/draft-ietf-cose-merkle-tree-proofs/ and counter signatures as defined in https://datatracker.ietf.org/doc/html/rfc9338.
Both definitions are helpful building blocks for scenarios involving multiple parties that consume and produce credentials using the "Three Role Model".
Examples include credential endorsement by third parties, credential trustworthiness via remote attestation evidence appraisal for issuers, or credential transparency via notarization.

### Out-of-Scope

The working group will NOT address transport protocols, such as those developed at OAUTH, OIDF, W3C or ISO in the scope of its initial charter.

The working group will NOT address specific credential use cases, such as "personal credentials" or "software supply chain".
Instead, the SPICE WG will reuse existing work or incorporate emerging work items produced by other IETF working groups, such as SCITT, OAUTH. Additionally, the SPICE WG will coordinate with other SDOs, such as ISO or W3C, on data model elements needed to support existing credential use cases. 

The working group will NOT be limited to JSON-LD data models, but to the extent that JSON-LD is compatible with JWT regsitered claims and private claims, the W3C Verifiable Data Model remains supported, as described in https://www.w3.org/TR/vc-jose-cose.

## Motivating Use Cases 

There are several expanding use cases and common patterns that motivate the working group and broader community, including:

- Compact selective disclosure in verifiable credentials via CBOR, in support of optical and radio transports.
- Expanding use of topic-specific microcredentials, particularly in education
- Digitization of physical supply chain credentials in multiple jurisdictions requiring CBOR creds at volume with system to system presentations
  - Impending public tests with US CBP, USDA, FDA, and other regulatory agencies
      - https://github.com/w3c-ccg/traceability-vocab
  - Digital Product Passports
      - https://hadea.ec.europa.eu/calls-proposals/digital-product-passport_en
- IoT, Control Systems, and Critical Infrastructure related Credentials
- Credentials related to authenticity and provenance, especially related to digital media
- Offline exchange (in person) of credentials that may have been internet issued
- Embedding of credentials in other data formats
- Digital Wallet Initiatives

Some of these use cases may be solved by the group directly, for others the group may enable a solution by providing supporting specifications.

## Motivating Factors for conducting this work at IETF

- Privacy and security expertise at IETF / IRTF specifically relevant to this work
- Anticipated successful conclusion of the VC 2.0 Working Group at W3C

## Work Items

Documents produced by the working group will include the following:

- Architecture document
- Use case document https://datatracker.ietf.org/doc/draft-prorock-spice-use-cases/ 
- Selective Disclosure with CWTs https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/
- TBD Identity Specification inspired by
    - https://datatracker.ietf.org/doc/rfc9278/
    - https://datatracker.ietf.org/doc/draft-ietf-cose-key-thumbprint/

Based on conversations on OAUTH and SPICE lists, the following work items have been proposed to be moved to SPICE, assuming authors / WGs agree, and SPICE forms to be able to receive them:

- JWT and CWT Status List https://datatracker.ietf.org/doc/draft-looker-oauth-jwt-cwt-status-list/
- SD-JWT-based Verifiable Credentials (SD-JWT VC) https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/

## Milestones

MM YYYY - Submit a Use Case and Terminology document to the IESG for publication
MM YYYY - Submit an Architecture document to the IESG for publication
MM YYYY - Submit a document covering selective disclosure with COSE to the IESG for publication

## Why IETF

Because of the security and integrity aspects directly involved in verifiable credentials that utilize a "Three Role Model", particularly their reliance on asymmetric cryptography with possible intermediaries during exchange, this topic must be worked with in cooperation with existing security expertise in the IETF and IRTF.  The broader community engaging in the verifiable credential space is converging within the IETF because of this security expertise. Multiple editors of existing work in W3C related to verifiable credentials are engaged and supportive of this work, and believe that IETF is the appropriate location for this work. By working in IETF we can ensure broader engagement with the work, security, and privacy review by the appropriate experts at IETF, and better coordinate with IETF groups that are leveraging or extending this work for use in various IETF standards.

## Relationship with W3C VCWG
The VCWG, which developed the 'Three Role Model' and defined the 'Verifiable Credentials Data Model v2.0' specification (https://www.w3.org/TR/vc-data-model-2.0/) has created a JSON-LD data model and is defining mechanisms to secure this JSON-LD data model. It is anticipated that JSON-LD credentials will continue to be developed in the VCWG and the W3C. SPICE will concern itself with JSON, CBOR and other formats of digital credentials that may be required by IETF use cases.
