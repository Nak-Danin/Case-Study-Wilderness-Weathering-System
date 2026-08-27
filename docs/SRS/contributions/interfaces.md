A# 4. Internal Interfaces

These are the interfaces *between components of the station software*. The
component structure follows the object-oriented design of the weather station in
Sommerville, 9th ed., Ch. 7, §7.1 (pp. 188–198), and exists so that a single
component can be replaced remotely (UR-15, NSR-11).

## 4.1 Component overview

| Component | Responsibility | Requirements served |
|---|---|---|
| `WeatherStation` | Top-level controller; starts and stops collection, reporting, testing and configuration | UR-01, UR-14 |
| `WeatherData` | Holds and summarises collected readings | UR-02 |
| `Instrument` (and its subtypes) | Reads one physical sensor, reports its own condition | UR-01, UR-08 |
| `InstrumentStatus` | Tracks operational / degraded / failed state; drives failover | UR-08, UR-16 |
| `PowerManager` | Battery and generator monitoring, load shedding, generator shutdown | UR-09, UR-12, UR-13 |
| `CommsController` | Satellite link, transmission queue, retry, link-fault detection | UR-03, UR-10 |
| `FaultReporter` | Assembles and queues diagnostic reports | UR-11 |
| `ConfigurationManager` | Applies parameter changes and installs replacement components | UR-14, UR-15 |

## 4.2 Interface definitions

| Provider → Consumer | Operations | Notes |
|---|---|---|
| `Instrument` → `WeatherStation` | `read()`, `selfTest()`, `getStatus()` | Uniform across all instrument subtypes so a backup can substitute for a primary |
| `WeatherStation` → `WeatherData` | `store(reading)`, `summarise(period)`, `clear()` | Summary is what is transmitted, not raw readings |
| `WeatherData` → `CommsController` | `getReportPayload()` | Payload released only after summarisation completes |
| `CommsController` → `WeatherStation` | `send(payload)`, `acknowledged()`, `linkFailed()` | Failure to acknowledge keeps data stored (SR-08) |
| `InstrumentStatus` → `WeatherStation` | `notifyFailure(instrumentId)` | Triggers failover to backup (SR-28) |
| `PowerManager` → `WeatherStation` | `lowPower()`, `powerRestored()` | Drives suspension and resumption of non-essential functions |
| `PowerManager` → generator hardware | `stopGenerator()`, `startGenerator()` | Invoked on the safe-wind threshold (SR-22) |
| Any component → `FaultReporter` | `raise(subsystem, condition, time)` | Single reporting channel for all subsystems |
| `ConfigurationManager` → any component | `deactivate()`, `install(version)`, `activate()`, `rollback()` | The contract that makes dynamic reconfiguration possible |

## 4.3 Constraint

A component may only be replaced at runtime if it is reached exclusively through
the operations listed above. Any direct dependency between component internals
breaks UR-15 and is prohibited.
