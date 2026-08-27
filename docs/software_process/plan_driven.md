# Plan-Driven (Waterfall) Development

## Where it is used

The **wilderness weather station embedded software and hardware system** — the
unit deployed in the field, together with its instruments, power plant and
satellite transceiver.

## Book reference

Sommerville, *Software Engineering*, 9th ed., **Ch. 1, p. 20, ll. 5–18**.

Paraphrased: the defining characteristic of the weather station is that it is
entirely self-contained. It generates its own power, communicates over a
satellite link, and must be able to reconfigure itself when part of it fails.
The software is *embedded* — it is one element of a larger hardware/software
system rather than a stand-alone application.

## Reasoning

1. **The hardware is specified up front.** Instruments, battery capacity, wind
   generator and satellite modem are procured and mounted before the software
   ships. Requirements that depend on physical parts cannot be renegotiated
   sprint by sprint.
2. **Failure is expensive.** A station sits in an area with no local
   infrastructure (UR-18). A defect that bricks the unit costs a field trip, not
   a patch release, so rigorous up-front modelling and verification pay for
   themselves.
3. **Safety and protection behaviour must be proven before deployment.**
   Shutting the generator down in high winds (UR-13) and failing over to a backup
   instrument (UR-16) are behaviours that have to be specified, reviewed and
   tested against a fixed specification.
4. **Regulatory / contractual traceability.** A plan-driven process produces the
   documentation set (URD → SRS → design → test) that this repository mirrors.

## Requirements developed under this branch

UR-01, UR-02, UR-03, UR-08, UR-09, UR-10, UR-11, UR-12, UR-13, UR-16, UR-17, UR-18.

## Stage mapping

| Waterfall stage | Artefact in this repository |
|---|---|
| Requirements definition | `docs/URD/urd.md` |
| System & software specification | `docs/SRS/srs.md` |
| Architectural design | `docs/diagrams/` |
| Implementation & unit test | `source/` |
| Integration & system test | Field acceptance of the station unit |
| Operation & maintenance | Station maintenance system (agile branch) |
