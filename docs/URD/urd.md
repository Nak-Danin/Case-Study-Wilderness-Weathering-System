# User Requirements Document (URD)
## Wilderness Weather Station

**Case study source:** Ian Sommerville, *Software Engineering*, 9th edition —
Ch. 1 §1.3.2 (pp. 19–21), Ch. 4 §4.1 (pp. 84–89), Ch. 7 §7.1 (pp. 188–198).

---

## Table of contents

| § | Section | File |
|---|---|---|
| 1 | Introduction | [`contributions/introduction.md`](contributions/introduction.md) |
| 2 | Background | [`contributions/background.md`](contributions/background.md) |
| 3 | Problem statement | [`contributions/problem_statement.md`](contributions/problem_statement.md) |
| 4 | Objectives | [`contributions/objectives.md`](contributions/objectives.md) |
| 5 | Stakeholders | [`contributions/stake_holders.md`](contributions/stake_holders.md) |
| 6 | Functional requirements | [`contributions/functional_requirements.md`](contributions/functional_requirements.md) |
| 7 | Non-functional requirements | [`contributions/non_functional_requirements.md`](contributions/non_functional_requirements.md) |

---

## Requirements index

| UR ID | Classification | Subsystem | One-line statement |
|---|---|---|---|
| UR-01 | Functional | Station | Collect periodic sensor measurements |
| UR-02 | Functional | Station | Validate, filter and summarise raw readings |
| UR-03 | Functional | Station | Transmit data to the central archive |
| UR-04 | Functional | Central server | Collect and organise data from all stations |
| UR-05 | Functional | Central server | Process and analyse weather data |
| UR-06 | Functional | Central server | Archive historical data for long-term use |
| UR-07 | Functional | Maintenance | Monitor station health over satellite |
| UR-08 | Functional | Station | Test instruments and flag anomalies |
| UR-09 | Functional | Station | Monitor battery charge and generator output |
| UR-10 | Functional | Station | Monitor satellite hardware, log link failures |
| UR-11 | Functional | Station + Maintenance | Issue diagnostic fault reports |
| UR-12 | Functional | Station | Manage consumption and recharge batteries |
| UR-13 | Functional | Station | Shut down the generator in hazardous winds |
| UR-14 | Functional | Maintenance | Remote administration of station parameters |
| UR-15 | Functional | Station + Maintenance | Dynamic remote component update |
| UR-16 | Functional | Station | Automatic failover to a backup instrument |
| UR-17 | Non-functional | Whole system | High availability, tolerate partial failure |
| UR-18 | Non-functional | Station | Fully autonomous operation in remote areas |

**Totals:** 16 functional, 2 non-functional, 18 user requirements.

---

## Process note

The requirements above are delivered through a hybrid process — a plan-driven
branch for the embedded station and an agile branch for the server and
maintenance applications, with dynamic reconfiguration used for remote updates.
See [`../software_process/process_model.md`](../software_process/process_model.md).

## Next document

Each UR is expanded into verifiable system requirements in
[`../SRS/srs.md`](../SRS/srs.md)
