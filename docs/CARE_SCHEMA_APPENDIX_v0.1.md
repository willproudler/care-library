# CARE Schema Appendix v0.1

## Purpose

This appendix records the conceptual schema of CARE v0.1.

It is not yet a final technical schema. It is a stabilising document for the unit hierarchy, naming conventions, and future validation rules.

## Core object: CARE Unit

A CARE unit is a structured interpretive object generated at a particular scale.

Possible unit levels include:

- RAW
- PASSAGE
- CH
- CL
- MC
- WB
- CB
- XS
- SC
- OV

## Suggested CARE unit fields

A CARE unit may include:

```text
unit_id
unit_type
project_id
work_id
source_unit_ids
derived_from_unit_ids
passage_ids
title
author
level
version
created_at
model_or_method
content
claims
axioms
exclusions
contradictions
source_trace
validation_status
notes
```

## Unit levels

### RAW

Represents cleaned source text or a source division.

### PASSAGE

Represents a source passage split from RAW text.

Possible fields:

```text
passage_id
raw_unit_id
project_id
passage_index
text
start_char
end_char
source_ref
checksum
```

### CH

Chapter-level CARE unit.

Possible fields:

```text
care_unit_id
unit_type: CH
raw_unit_id
source_passage_ids
argument_spine
axioms
exclusions
contradictions
conceptual_pressure
notes
```

### CL

Cluster-level unit synthesising multiple CH units.

Possible fields:

```text
care_unit_id
unit_type: CL
source_ch_ids
inherited_passage_ids
cluster_argument
cluster_axioms
cluster_exclusions
```

### MC

Metacluster unit synthesising multiple CL units.

Possible fields:

```text
care_unit_id
unit_type: MC
source_cl_ids
inherited_ch_ids
inherited_passage_ids
metacluster_argument
```

### WB

WholeBook unit synthesising a complete work.

Possible fields:

```text
care_unit_id
unit_type: WB
source_mc_ids
source_cl_ids
source_ch_ids
inherited_passage_ids
wholebook_argument
book_axioms
book_exclusions
book_contradictions
lineage_notes
```

## Future units

### CB

Corpus-level synthesis across multiple WB units.

### XS

Cross-lineage synthesis across different authors, traditions, or conceptual fields.

### SC

Strange-child synthesis generated from multiple parent units.

### OV

Overlay unit applying a specialist interpretive frame.

## Validation principles

A valid CARE unit should ideally include:

- stable unit ID;
- clear unit type;
- source ancestry;
- version information;
- content field;
- relation to lower-level units;
- passage provenance where available.

## Retrofitting note

Older CARE units may lack passage provenance.

These should be marked as:

```text
RETROFIT NEEDED
```

until their source passages and inherited ancestry are restored or verified.
