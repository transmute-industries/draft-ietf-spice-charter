# BoF Request: Secure Patterns for Internet CrEdentials (SPICE)

## Description

Digital credentials are essential to identity, authorization, licenses, certificates and digitization use cases that are part of modernization efforts targeting efficiency, and transparency, such as digital licenses or certificates of origin.

At IETF 118, SPICE had a WG forming BOF, see the BoF Request:

- https://datatracker.ietf.org/doc/bofreq-prorock-secure-patterns-for-internet-credentials-spice/03/
- https://datatracker.ietf.org/meeting/118/materials/slides-118-spice-complete-slide-deck-pdf-00

There was energy in the room, but the details of the specific drafts and the charter were not clear enough.

Since IETF 118, the draft charter, and several individual drafts have been shared on the SPICE list:

- https://mailarchive.ietf.org/arch/browse/spice/
- https://datatracker.ietf.org/group/spice/documents/

Regular informal meetings have been held, open to everyone, with agenda's and minutes to the best of our ability.

We have developed a revised proposed charter that addresses the feedback we have gathered from IETF 118, and on the lists.

- https://mailarchive.ietf.org/arch/msg/spice/V88sssepcruM6FKIgOxddc3rR-4/

We believe the charter is nearing a state of universal support from active contributors, but we are still making refinements.

See the latest charter activity here: 

- https://github.com/transmute-industries/ietf-spice-charter


## Required Details

- Status: WG Forming
- Responsible AD: Roman Danyliw
- BOF proponents: Orie Steele <orie@transmute.industries>, Heather Flanagan <hlf@sphericalcowconsulting.com>, Leif Johansson <leifj@sunet.se>, Brent Zundel <brent.zundel@gendigital.com>, Henk Birkholz <henk.birkholz@sit.fraunhofer.de>
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
  - https://www.w3.org/TR/vc-jose-cose/
  - https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/
  - https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/
  - https://datatracker.ietf.org/doc/draft-ietf-oauth-status-list/
  - https://digital-strategy.ec.europa.eu/en/library/european-digital-identity-wallet-architecture-and-reference-framework
  - https://www.cbp.gov/newsroom/national-media-release/cbp-initiates-interoperability-standards-test-improve-supply-chain
  - and same list as last BoF - https://datatracker.ietf.org/doc/bofreq-prorock-secure-patterns-for-internet-credentials-spice/03/

- Which (if any) modifications to existing protocols or practices are required:
  - The group will try to avoid modification to existing protocols and practices
  - The group may recommend extensions to JOSE and COSE
- Which (if any) entirely new protocols or practices are required:
  - The group will recommend data minimization and selective disclosure approaches for digital credential
- Open source projects (if any) implementing this work:
  - https://github.com/transmute-industries/sd-cwt
  - https://github.com/transmute-industries/dune

## Agenda

### Problem Statement (30 min)

- Problem Area and Introduction to Digital Credentials
- Known Use Cases
- How is SPICE related to other IETF Work

### Scope and Proposed Work Items (45 min)

- Architecture
- Selective Disclosure
- Metadata Discovery

### Discussion (45 min)

- Is the IETF the right place to do this work?
- Which organizations and SDOs need to be involved/collaborated with?
- What are the expected technical challenges?
- Is there interest in implementing such specifications?
- Is the technology likely to get deployed?
- Is there enough interest in helping with the work (spec editing, reviewing, implementing, deploying)?

## Links to the mailing list, draft charter if any, relevant Internet-Drafts, etc.

- Mailing List: https://www.ietf.org/mailman/listinfo/spice
- Draft charter: https://github.com/transmute-industries/ietf-spice-charter/blob/main/charter.md
- BoF Request: https://datatracker.ietf.org/doc/bofreq-prorock-secure-patterns-for-internet-credentials-spice/
- Relevant Internet-Drafts:
  
  - Metadata Discovery:
    - https://datatracker.ietf.org/doc/draft-steele-spice-metadata-discovery/

  - Selective Disclosure with CBOR:
    - https://datatracker.ietf.org/doc/draft-prorock-cose-sd-cwt/

  - Transparency Tokens:
    - https://datatracker.ietf.org/doc/draft-steele-spice-transparency-tokens/

  - Animated QR Code Presentations:
    - https://datatracker.ietf.org/doc/draft-steele-spice-cryptovolense/

  - Privacy Preserving Dynamic Credential State
    - https://datatracker.ietf.org/doc/draft-steele-spice-oblivious-credential-state/

  - Integrating with Contact Management Systems:
    - https://datatracker.ietf.org/doc/draft-steele-spice-vcard-credentials/

  - Guidance for Regional Profiles
    - https://datatracker.ietf.org/doc/draft-steele-spice-profiles-bcp/

  - Full list
    - https://datatracker.ietf.org/group/spice/documents/
