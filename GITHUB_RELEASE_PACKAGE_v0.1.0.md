# Proposed CARE Library v0.1.0 GitHub Release Package

**Status:** Proposal only  
**Release authorized:** No  
**Tag created:** No  
**Release published:** No

## Release identity

- **Tag:** `v0.1.0`
- **Release title:** CARE Library v0.1.0 — Architecture and Defensive Publication
- **Release type:** Documentation and defensive publication
- **Software included:** No
- **Public corpus included:** No
- **Licence:** CC BY-SA 4.0 for approved CARE-authored documentation

## Proposed tag allowlist

The proposed tag may include only approved versions of:

### Root governance and metadata

- `.gitignore`
- `README.md`
- `CHANGELOG.md`
- `CITATION.md`
- `CITATION.cff`, once final metadata is known
- `CONTRIBUTING.md`
- `DCO`
- `LICENSE`
- `LICENSES.md`
- `PULL_REQUEST_TEMPLATE.md`
- `RELEASE_CHECKLIST_v0.1.0.md`
- `SECURITY.md`
- `THIRD_PARTY_NOTICES.md`
- `TRADEMARK.md`
- `CARE_IMPLEMENTATION_STATUS_v0.1.md`
- `CARE_PUBLIC_RELEASE_BOUNDARY_v0.1.md`
- `CARE_PUBLIC_RIGHTS_MANIFEST_SCHEMA_v0.1.md`

### Architecture documents

- `docs/CARE_ARCHITECTURE_SPEC_v0.1.md`
- `docs/CARE_SCHEMA_APPENDIX_v0.1.md`
- `docs/CARE_PASSAGE_RETROFIT_PLAN_v0.1.md`
- `docs/CARE_COMMONS_CHARTER_v0.1.md`

### Defensive-publication documents

- `prior-art/CARE_MACHINE_DEFENSIVE_PUBLICATION_v0.1.md`
- `prior-art/CARE_PRIOR_ART_CLAIMS_v0.1.md`

Every allowed file must still pass the final rights and content review. Presence on this list does not by itself approve publication.

## Excluded from the tag and release

The release must not include:

- the withdrawn working paper;
- the withdrawn work-level corpus-status document;
- the withdrawn source-linked flagship example;
- source books or private source documents;
- RAW texts, passages or private annotations;
- private corpus databases, inventories or generated outputs;
- unpublished prompts or post-v0.1 specifications;
- XR, XS, SC revision, XA, Operator or revision-revalidation specifications;
- trademark filing evidence, correspondence or receipts;
- credentials, private configuration, personal information or private paths;
- material with an unresolved rights basis.

## Proposed attached assets

- `CARE_Library_Defensive_Publication_v0.1.0.md`
- `CARE_Library_Defensive_Publication_v0.1.0.pdf`
- `CARE_Library_Public_Documentation_v0.1.0.zip`
- `PUBLIC_RIGHTS_MANIFEST_v0.1.0.json`
- `RELEASE_MANIFEST_v0.1.0.json`
- `SHA256SUMS`
- `LICENSE.txt`

`PUBLIC_RIGHTS_MANIFEST_v0.1.0.json`, `RELEASE_MANIFEST_v0.1.0.json` and `SHA256SUMS` are generated from the frozen release commit and attached to the release. They are not tracked inside the `v0.1.0` tag.

`SHA256SUMS` records the SHA-256 checksum of every attached release asset except itself. The rights and release manifests do not contain their own checksums; those checksums are recorded in `SHA256SUMS`.

GitHub-generated source archives must be inspected separately because GitHub generates their bytes from the tag.

Attachments must be generated from the approved frozen commit and must match the recorded checksums.

## Draft release description

CARE Library v0.1.0 is a documentation-only publication describing the initial CARE architecture, provenance model, schema, commons principles and defensive-publication claims.

This release does not contain executable CARE software, a public CARE corpus, source texts, RAW materials, a public database or post-v0.1 specifications.

The documentation is licensed under CC BY-SA 4.0. Third-party source texts and trademarks are not included in that licence grant.

## Pre-publication verification

Before creating the tag:

- complete the public rights manifest;
- calculate the final checksums;
- confirm every internal link against the frozen tree;
- inspect GitHub’s complete automatic tag archive;
- confirm the version and release date;
- insert the reserved DOI into final citation metadata;
- confirm the v0.2 patent checkpoint remains intact;
- obtain explicit publication authorization.

No tag or release should be created from an unreviewed moving branch.
