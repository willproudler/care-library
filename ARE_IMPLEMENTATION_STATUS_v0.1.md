# CARE Library Implementation Status v0.1

**Status:** Public alpha documentation  
**Last reviewed:** 14 July 2026

## Purpose

This document distinguishes what is publicly documented, what is publicly implemented, and what remains proposed or private.

A specification or defensive-publication statement does not by itself establish that corresponding software, data, tests or operational infrastructure have been publicly released.

## Status terms

### Documented

The concept, architecture, schema or process is described in the public repository.

### Publicly implemented

A runnable implementation and sufficient public verification material are available in the public repository or an identified public release.

### Proposed

The material describes intended or future development rather than a released implementation.

### Not publicly released

Related work may exist outside the public repository, but no implementation, corpus or dataset is being represented here as a public release.

## Current public status

| Area | Public status |
|---|---|
| CARE v0.1 architecture | Documented |
| CARE v0.1 schema | Documented |
| Passage-grounded ingestion and retrofit approach | Documented |
| CARE commons principles | Documented |
| v0.1 defensive publication and prior-art statements | Publicly documented |
| Executable CARE reference implementation | Not publicly released |
| Public CARE API or hosted service | Not publicly released |
| Public CARE corpus or source-text collection | Not publicly released |
| Public RAW-text or passage dataset | Not publicly released |
| Public conformance or regression test suite | Not publicly released |
| Public database release | Not publicly released |
| XR, XS, SC revision, XA, Operator and revision-revalidation specifications | Excluded from v0.1 public scope |

## Release boundary

CARE Library v0.1 is currently a documentation-only public alpha.

The repository does not release:

- source books or source documents;
- RAW texts, passages or private annotations;
- a work-level corpus inventory;
- generated private corpus outputs;
- executable CARE software;
- a public CARE database;
- unpublished post-v0.1 specifications.

The controlling release boundary is `CARE_PUBLIC_RELEASE_BOUNDARY_v0.1.md`.

## Claims and compatibility

Claims that a project “implements CARE” or is “CARE-compatible” should identify:

- the public CARE specification version used;
- which documented components are implemented;
- which components are omitted or modified;
- the available validation or conformance evidence.

Until a public conformance suite exists, compatibility claims are descriptive and are not official certification.

## Updates

This status document must be updated whenever software, tests, databases, corpus assets or later specifications are approved for public release.

A future release must not silently change an item from “not publicly released” to “publicly implemented” without identifying the relevant public artifact and version.
