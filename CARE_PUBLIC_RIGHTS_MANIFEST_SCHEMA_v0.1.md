# CARE Public Rights Manifest Schema v0.1

**Status:** Public release-control specification  
**Scope:** Public CARE Library release assets

## Purpose

Every substantive file included in a CARE public release must have a recorded provenance, rights basis, release decision and final checksum. Integrity for the release-control files themselves is handled separately as described below, avoiding circular hashes.

The public manifest records release-safe facts. It must not contain source text, private paths, permission correspondence, personal contact details, payment information, or other sensitive evidence.

## Two-ledger model

### Private rights ledger

The private ledger may contain:

- permission evidence and correspondence;
- contracts and licence records;
- private source locations;
- confidential legal review;
- reviewer identity;
- personal or transaction information;
- unresolved rights analysis.

The private ledger must never be copied into the public repository or release package.

### Public rights manifest

The public manifest contains only the minimum non-sensitive information needed to establish why each released asset may be published.

## Manifest-level fields

A public manifest must contain:

- `manifest_version`
- `release_id`
- `release_date`
- `release_commit`
- `generated_at`
- `scope`
- `assets`
- `control_files`

The release commit and checksums must be populated only after the release contents are frozen.

## Asset-level fields

Each asset record must contain:

- `asset_id`
- `release_path`
- `asset_type`
- `sha256`
- `title`
- `creator_display`
- `public_source_identifier`
- `source_date`
- `derived_from_asset_ids`
- `contains_third_party_material`
- `rights_basis`
- `license_expression`
- `license_url`
- `rights_holder_display`
- `quotation_extent`
- `provenance_summary`
- `personal_data_status`
- `sensitive_data_status`
- `review_status`
- `reviewed_on`
- `reviewer_role`
- `release_decision`
- `notes`

## Controlled values

### `rights_basis`

Permitted values:

- `original`
- `public-domain`
- `open-licensed`
- `permission`
- `facts-only`
- `exception-reviewed`
- `restricted`
- `unknown`

### `release_decision`

Permitted values:

- `include`
- `include-redacted`
- `metadata-only`
- `exclude`

### `review_status`

Permitted values:

- `not-reviewed`
- `review-in-progress`
- `approved`
- `rejected`
- `needs-legal-review`

### Personal and sensitive data status

Permitted values:

- `none-detected`
- `redacted`
- `present-approved`
- `present-exclude`
- `not-reviewed`

## Publication rules

1. Only records with `review_status: approved` may receive an `include` decision.
2. Material with a `restricted` or `unknown` rights basis must not enter a public release.
3. `exception-reviewed` material requires a documented private legal assessment.
4. Final SHA-256 values must be calculated from the frozen release files.
5. Public records must use public URLs or opaque identifiers, never private filesystem paths.
6. Permission evidence remains in the private ledger.
7. The public manifest must describe quotation extent without reproducing the quotation.
8. Database rights and rights in individual database contents must be recorded separately.
9. Generated material must record its source ancestry without exposing private input text.
10. A manifest approval applies only to the identified asset version and checksum.

## Integrity-control files

To avoid circular or stale hashes:

1. `assets` must cover every tracked release file and every substantive attached release asset.
2. `PUBLIC_RIGHTS_MANIFEST_v0.1.0.json`, `RELEASE_MANIFEST_v0.1.0.json` and `SHA256SUMS` are generated from the frozen release commit and are not tracked inside the `v0.1.0` tag.
3. `SHA256SUMS` must record the SHA-256 checksum of every attached release asset except itself.
4. The rights and release manifests must not contain their own checksums; their final checksums are recorded in `SHA256SUMS`.
5. GitHub-generated source archives must be inspected separately because GitHub generates their bytes from the tag.

## Minimal manifest structure

```json
{
  "manifest_version": "0.1",
  "release_id": "v0.1.0",
  "release_date": "TO_BE_SET_AT_RELEASE",
  "release_commit": "TO_BE_SET_AT_RELEASE_FREEZE",
  "generated_at": "TO_BE_SET_AT_RELEASE_FREEZE",
  "scope": "CARE Library documentation-only public release",
  "control_files": {
    "rights_manifest": "PUBLIC_RIGHTS_MANIFEST_v0.1.0.json",
    "release_manifest": "RELEASE_MANIFEST_v0.1.0.json",
    "checksum_file": "SHA256SUMS",
    "checksum_rule": "SHA256SUMS covers every attached release asset except itself"
  },
  "assets": []
}
```

The empty structure above is a schema example, not an approved release manifest.

## Relationship to licensing

A manifest records whether an asset may be released and under what stated terms. It does not create rights that the project does not hold.
The repository-wide documentation licence applies only where license_expression and the rights basis support that conclusion.
