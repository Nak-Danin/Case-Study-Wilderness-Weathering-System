# 1. Introduction

## 1.1 Purpose

This User Requirements Document (URD) states, in the language of the user, what
the Wilderness Weather Station system must do. It is the input to the System
Requirements Specification (`../../SRS/srs.md`), where each user requirement is
expanded into verifiable system requirements.

## 1.2 Scope

The system covered by this document has three parts:

- the **weather station** deployed in a remote area, with its instruments, power
  system and satellite link;
- the **data management and archiving system**, a central server that collects,
  processes and stores data from every station;
- the **station maintenance system**, used to monitor station health and control
  station parameters remotely.

## 1.3 Definitions

| Term | Meaning |
|---|---|
| Station | One self-contained wilderness weather station unit |
| UR | User Requirement, numbered UR-01 … UR-18 |
| Instrument | A sensor measuring temperature, pressure, sunshine, rainfall, wind speed or wind direction |
| Failover | Automatic switch from a failed primary instrument to a backup |
| Dynamic reconfiguration | Replacing a software component while the system keeps running |

## 1.4 Source

All requirements in this document are traced to Ian Sommerville,
*Software Engineering*, 9th edition — Chapter 1 (§1.3.2, pp. 19–21),
Chapter 4 (§4.1, pp. 84–89) and Chapter 7 (§7.1, pp. 188–198).
Full citation list: `../../references/references.md`.
