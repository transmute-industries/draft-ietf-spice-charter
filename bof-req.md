# BoF Request: Secure Patterns for Internet CrEdentials (SPICE)


## Description

There is a need document verifiable credentials more clearly: credentials that utilize the issuer, holder, and verifier (three role) model across various work IETF, ISO, W3C, and other SDOs.  This need particularly arises in use cases about verifiable credentials for personal credential *and* business credential.  In support of compactness, those use cases benefit from CBOR encoding.  In support of interoperabilty, those use cases benefit from the cryptographic agility properties of COSE.  Based on these use cases, there is a need to clearly define message formats and supporting mechanisms. The proposed SPICE WG is intended to coordinate closely with other working group's items developing JSON-based credentials to keep that work and the SPICE WG's work architecturally aligned.

Digital credentials based on IETF standards have use cases ranging from personal credentials, such as drivers licenses and vaccination proofs, to business-to-business or business-to-government applications.  One example is fraud and counterfitting prevention in cross-border trade documents by protecting digital representations of mill test reports, bills of materials, bills of lading, or commercial invoices.  In order to meet privacy, security, and sustainability objectives, digital credentials need to be designed with awareness of computation and storage constraints associated with their use cases.  These objectives can be achieved by leveraging industry adopted standards and managing tradeoffs between cutting-edge and well-established cryptography.

The SPICE WG aims to support digitial credential formats based on existing IETF standards, and extend them to support stakeholders that are building compliance and automation systems based on industry adopted cryptography and protocols.

## Required Details

- Status: WG Forming
- Responsible AD: Roman Danyliw
- BOF proponents: Mike Prorock <mprorock@mesur.io>, Heather Flanagan <hlf@sphericalcowconsulting.com>, Leif Johansson <leifj@sunet.se>, Brent Zundel <brent.zundel@gendigital.com>, Henk Birkholz <henk.birkholz@sit.fraunhofer.de>
- BOF chairs: TBD
- Number of people expected to attend: 60
- Length of session (1 or 2 hours): 2 hours
- Conflicts (whole Areas and/or WGs)
  - Chair Conflicts: TBD
  - Technology Overlap: OAUTH, SCITT, RATS, COSE, CBOR, JOSE, WIMSE, MLS, MIMI
  - Key Participant Conflict: COSE, JOSE, CFRG, OAUTH, RATS, OPSAWG, IOTOPS, SCITT

## Information for IAB/IESG

To allow evaluation of your proposal, please include the following items:

- Any protocols or practices that already exist in this space:
  - https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html
  - https://openid.net/specs/openid-4-verifiable-presentations-1_0.html
  - https://openid.net/specs/openid-connect-self-issued-v2-1_0.html
  - https://developer.apple.com/documentation/passkit/wallet/verifying_wallet_identity_requests?language=objc
  - https://chapi.io/ 
  - https://identity.foundation/presentation-exchange/ 
  - https://w3id.org/traceability/interoperability
  - https://datatracker.ietf.org/doc/draft-barnes-mls-userinfo-vc/  
  - Verifiable Credentials Data Model v1.1 (w3.org)
  - Decentralized Identifiers v1.0 (w3.org)

- Which (if any) modifications to existing protocols or practices are required:
  - The group will try to avoid modification to existing protocols and practices
- Which (if any) entirely new protocols or practices are required:
  - TBD based on scope of group - there is some chance that there is a practice shift towards enforced data-minimization through selective disclosure as a preferred mode of operations when working with credentials
- Open source projects (if any) implementing this work:
  - TBD based on scope of group

## Agenda

### Problem Statement (30 min)

- Problem Area and introduction to verifiable credentials
- Known Use Cases
- How is SPICE related to other IETF Work

### Scope and Proposed Work Items (45 min)

- SPICE Use Cases Documentation
- Selective Disclosure with CWTs
- Architecture
- Other Items that might be considered for inclusion in this group

### Discussion (45 min)

- Is the IETF the right place to do this work?
- Which organizations and SDOs need to be involved/collaborated with?
- What are the expected technical challenges?
- Is there interest in implementing such specifications?
- Is the technology likely to get deployed?
- Is there enough interest in helping with the work (spec editing, reviewing, implementing, deploying)?

## Links to the mailing list, draft charter if any, relevant Internet-Drafts, etc.

- Mailing List: TBD (requested: https://www.ietf.org/mailman/listinfo/spice)
- Draft charter: https://github.com/transmute-industries/ietf-spice-charter/blob/main/charter.md
- BoF Request: https://datatracker.ietf.org/doc/bofreq-prorock-secure-patterns-for-internet-credentials-spice/
- Relevant Internet-Drafts:
  - Use Cases:
    - https://datatracker.ietf.org/doc/draft-prorock-spice-use-cases/
  - Solutions:
    - https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/
