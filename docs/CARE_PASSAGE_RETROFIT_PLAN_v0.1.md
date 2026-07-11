# CARE Passage Retrofit Plan v0.1

## Purpose

Older CARE projects may have been processed before passage provenance became stable.

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

## Retrofit order

First five:

1. CCRU Writings 1997–2003
2. Beyond Good and Evil
3. Difference and Repetition
4. Spinoza Ethics
5. The System of Objects

Second ring:

6. Kant Pure Reason
7. Marx Capital Vol. One
8. Revelation
9. The Accursed Share Volume One
10. Symbolic Exchange and Death

## Retrofit steps per book

For each book:

1. locate the cleaned RAW source;
2. create or verify the RAW passage set;
3. assign stable passage IDs;
4. verify CH units;
5. attach CH units to relevant passage IDs where possible;
6. verify CL units inherit CH ancestry;
7. verify MC units inherit CL / CH ancestry;
8. verify WB unit inherits lower-level ancestry;
9. update CARE_CORPUS_STATUS_v0.1.md;
10. create at least one demonstrable source chain.

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
