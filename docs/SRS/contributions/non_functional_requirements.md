# 3. Non-Functional System Requirements

Classification follows Sommerville, 9th ed., Ch. 4, p. 87, ll. 1–4 —
constraints on the services the system offers, rather than services themselves.

## 3.1 Reliability and availability (from UR-17)

| SR ID | Requirement |
|---|---|
| NSR-01 | The station shall continue to operate without human intervention for the whole of a deployment period. |
| NSR-02 | No single instrument failure shall stop collection from the remaining instruments. |
| NSR-03 | No stored observation shall be lost as a result of a failed transmission attempt. |
| NSR-04 | The data management system shall remain available to receive station transmissions during scheduled maintenance of its analysis functions. |

## 3.2 Autonomy and environment (from UR-18)

| SR ID | Requirement |
|---|---|
| NSR-05 | The station shall operate with no mains power and no wired network connection. |
| NSR-06 | The station shall operate across the full environmental range of its deployment site without manual adjustment. |
| NSR-07 | All corrective maintenance that does not require physical replacement of hardware shall be performable remotely. |

## 3.3 Performance

| SR ID | Requirement |
|---|---|
| NSR-08 | Instrument sampling shall complete within the collection cycle interval. |
| NSR-09 | Local summarisation shall complete before the next reporting period begins. |
| NSR-10 | Transmission payload shall be summarised rather than raw, to fit within the satellite bandwidth budget. |

## 3.4 Maintainability

| SR ID | Requirement |
|---|---|
| NSR-11 | Station software shall be structured as independently replaceable components with defined interfaces. |
| NSR-12 | Replacing one component shall not require recompilation or redeployment of the others. |
| NSR-13 | Every fault report shall carry enough diagnostic detail to identify the failing subsystem without a site visit. |

## 3.5 Security

| SR ID | Requirement |
|---|---|
| NSR-14 | Station parameter changes and component updates shall be accepted only from an authenticated maintenance system. |
| NSR-15 | Archived data shall be protected against modification after acceptance. |

## 3.6 Process constraints

| SR ID | Requirement |
|---|---|
| NSR-16 | Station embedded software shall be developed under a plan-driven process with the specification frozen before implementation. |
| NSR-17 | Server and maintenance applications shall be developed and released incrementally. |
