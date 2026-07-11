# CARE Architecture Specification v0.1

## Author

William Proudler

## Contributors

- Ian Wenzel-Garay *(anticipated contributor to future versions)*

Version: v0.1.0-alpha

Date: 11 July 2026

## 1. Name

CARE stands for **Canonical Axiomatic Reduction Engine**.

CARE has two related meanings:

- **CARE Machine** — the local compiler/process that transforms texts into structured CARE units.
- **CARE Library** — the accumulated corpus of processed CARE units.

The CARE Machine produces the CARE Library.

## 2. Core purpose

CARE is a source-grounded recursive system for turning books and texts into layered conceptual structures.

It is not a summarisation system.

A summary reduces a text into a shorter statement. CARE attempts to preserve the architecture of a text across multiple scales: passages, chapters, clusters, metaclusters, whole books, and eventually corpora.

CARE treats a book as an argument-field rather than as content.

## 3. Basic pipeline

The canonical CARE v0.1 pipeline is:

```text
SOURCE TEXT
→ CLEAN RAW TEXT
→ RAW UNIT
→ RAW PASSAGE SET
→ CH UNITS
→ CL UNITS
→ MC UNITS
→ WB UNIT
→ CORPUS / CROSS-LINEAGE UNITS
```

## 4. Unit levels

### RAW

The raw cleaned source text or source unit.

### RAW PASSAGES

Source passages created at ingestion. These give CARE its source-grounding and provenance layer.

### CH

Chapter-level CARE units. These extract and organise the conceptual structure of individual chapters or comparable source divisions.

### CL

Cluster-level CARE units. These synthesise groups of CH units.

### MC

Metacluster CARE units. These synthesise groups of CL units when a work is too large to move directly from cluster to whole-book level.

### WB

WholeBook CARE units. These represent the recursive conceptual architecture of a complete work.

### CB

CorpusBook or corpus-level units. Future layer for synthesising multiple WB units.

### XS

Cross-lineage synthesis units. Future layer for comparing works, authors, traditions, and conceptual lineages.

### SC

Strange-child synthesis units. Future experimental layer for producing new conceptual offspring from incompatible or distant source lineages.

### OV

Overlay units. Future layer for optional interpretive overlays, including occult, diagrammatic, apophatic, NUMO, or other specialist modes.

## 5. Passage provenance

From CARE v0.1 onward, raw passage generation should happen at the point of RAW ingestion.

This means the system should follow:

```text
SOURCE TEXT
→ RAW
→ RAW PASSAGES
→ CH
→ CL
→ MC
→ WB
```

The purpose is to ensure that higher-level claims can eventually trace backward through their ancestry.

A complete provenance chain should look like:

```text
WB CLAIM
→ MC SOURCE
→ CL SOURCE
→ CH SOURCE
→ RAW PASSAGE
→ ORIGINAL TEXT
```

## 6. Why this matters

CARE is designed to avoid the main weakness of ordinary AI summarisation: fluent but ungrounded compression.

CARE aims to preserve:

- argument structure;
- contradiction;
- exclusion;
- conceptual pressure;
- source ancestry;
- lineage;
- unresolved tensions;
- future comparability.

## 7. Current status

CARE v0.1 is in active local development.

A first corpus has already been processed across philosophy, theology, political economy, post-structuralism, accelerationism, psychoanalysis, and critical theory.

Some older projects were processed before passage provenance became central and therefore require passage retrofit.

## 8. Future development

Future development should prioritise:

1. passage-grounded ingestion;
2. stable unit identifiers;
3. schema validation;
4. corpus status tracking;
5. flagship examples;
6. cross-lineage synthesis;
7. public documentation;
8. open commons protocol design.
