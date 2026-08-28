# 7. Non-Functional Requirements (UR-17, UR-18)

**Definition applied** — Sommerville, 9th ed., Ch. 4, p. 87, ll. 1–4:
non-functional requirements are constraints on the services or functions the
system offers — timing constraints, constraints on the development process,
standards, and so on.

| UR ID | Type | Source (page & line) | Source content, paraphrased | User statement |
|---|---|---|---|---|
| UR-17 | Reliability / availability | Ch. 1, p. 19, l. 12 | The system has to be reliable and operate without human intervention for long periods | "The overall system must maintain high availability, tolerate partial failures and minimise downtime." |
| UR-18 | Environmental / operational | Ch. 1, p. 19, l. 6 | These stations collect weather information in remote areas that have no local infrastructure | "The station must operate completely autonomously in remote locations where physical access is difficult." |

## Why these are non-functional

Neither requirement names a service the system performs. Each constrains *how
well* and *under what conditions* every service in §6 must be delivered:

- **UR-17** constrains all functional requirements with an availability and
  fault-tolerance target. It is the reason UR-16 (failover) and UR-11 (fault
  reporting) exist as functions.
- **UR-18** constrains the operating environment: no mains power, no wired
  network, no operator on site. It is the reason UR-09, UR-12 and UR-13 (power
  management) and UR-03 (satellite transmission) exist as functions.

## Measurable form for the SRS

| UR | Suggested verifiable criterion |
|---|---|
| UR-17 | Station availability across a deployment period; no single instrument failure causes total loss of service |
| UR-18 | Station runs for a full unattended deployment period on generated power alone, with no site visit |
