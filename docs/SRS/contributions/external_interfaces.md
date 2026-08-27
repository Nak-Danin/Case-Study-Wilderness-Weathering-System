# 5. External Interfaces

Interfaces between the system and anything outside it — hardware, other systems
and people.

## 5.1 Hardware interfaces

| Interface | Description | Requirements |
|---|---|---|
| Instrument bus | Electrical/logical connection to each sensor: temperature, pressure, sunshine, rainfall, anemometer, wind vane | UR-01, UR-08 |
| Battery subsystem | Charge level readout and charge control | UR-09, UR-12 |
| Wind generator | Output readout, plus stop/start control used in high winds | UR-09, UR-13 |
| Satellite transceiver | The station's only channel to the outside world; carries data out and commands in | UR-03, UR-07, UR-14, UR-15 |
| Non-volatile store | Retains summarised data and fault reports until acknowledged | UR-02, UR-17 |

## 5.2 Software / system interfaces

| Interface | Direction | Content | Requirements |
|---|---|---|---|
| Station → Data management and archiving system | Outbound, per reporting period | Station identifier, timestamped summary values | UR-03, UR-04 |
| Data management system → Station | Inbound | Transmission acknowledgement | UR-03 |
| Station → Station maintenance system | Outbound | Health status, fault reports, failover events | UR-07, UR-08, UR-10, UR-11 |
| Station maintenance system → Station | Inbound, authenticated | Parameter changes, restart commands, replacement components | UR-14, UR-15 |
| Data management system → analysis and archive clients | Outbound | Processed data sets, historical queries | UR-05, UR-06 |

## 5.3 Communication constraints

- The satellite link is intermittent and bandwidth-limited, so only summarised
  data is sent (SR-05, NSR-10).
- Every inbound command must be authenticated before it is acted on (NSR-14).
- An unacknowledged outbound message is retried, never discarded (SR-08, NSR-03).

## 5.4 User interfaces

| User | Interface | Requirements |
|---|---|---|
| Maintenance engineer | Station health dashboard with per-station fault list | UR-07, UR-11 |
| System administrator | Authenticated parameter control and update console | UR-14, UR-15 |
| Meteorologist / analyst | Query and reporting front end onto the archive | UR-05, UR-06 |

The station itself has **no local user interface**: it operates unattended in a
location with no staff (UR-18).
