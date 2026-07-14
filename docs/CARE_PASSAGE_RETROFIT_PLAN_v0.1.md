# CARE Passage Retrofit Plan v0.1

Author: William Proudler

Version: v0.1.0

Initial public date: 11 July 2026

Release date: 15 July 2026

## Purpose

Any CARE project created without verified passage provenance requires review before it can be represented as passage-grounded.

This document defines the retrofit plan.

## New rule

From CARE v0.1 onward, RAW passages are generated at the point of RAW ingestion.

This means:

```text
SOURCE TEXT
→ CLEAN RAW TEXT
→ RAW UNIT
→ RAW PASSAGE SET
→ CH
→ CL
→ MC
→ WB
```

CARE units should not be free-floating summaries. They should be structured conceptual objects with source ancestry.

## Retrofit status

Any older project without verified passage provenance should be marked:

```text
RETROFIT NEEDED
```

until the passage chain is restored or verified.

## Retrofit prioritisation

Project identities and work-level processing records belong in private operational tracking unless they pass a separate public-release review.

Private prioritisation may consider:

1. provenance gaps;
2. public-demonstration value;
3. source-rights status;
4. technical complexity; and
5. review capacity.

## Retrofit steps per approved project

For each project selected through private operational tracking:

1. locate the cleaned RAW source;
2. create or verify the RAW passage set;
3. assign stable passage IDs;
4. verify CH units;
5. attach CH units to relevant passage IDs where possible;
6. verify CL units inherit CH ancestry;
7. verify MC units inherit CL / CH ancestry;
8. verify WB unit inherits lower-level ancestry;
9. create at least one demonstrable source chain.

## Minimum acceptable provenance chain

For v0.1, the minimum demonstration chain is:

```text
WB claim
→ source MC or CL unit
→ source CH unit
→ RAW passage
→ original source text
```

## Ideal provenance chain

The ideal chain is:

```text
WB claim
→ MC unit
→ CL unit
→ CH unit
→ RAW passage
→ original source text
```

## Principle

Passage provenance is not decorative.

It is what makes CARE different from ordinary AI summary.

Without provenance, CARE is only an interpretive compression system.

With provenance, CARE becomes a source-grounded recursive library.
