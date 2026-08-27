# Convert URD to SRS

### UR-01: Weather Data Collection
* **SR-01:** The station shall read every attached instrument — temperature, pressure, sunshine, rainfall, wind speed, wind direction — once per collection cycle.
* **SR-02:** The collection cycle interval shall be a configurable station parameter.
* **SR-03:** The station shall timestamp every reading with the station clock at the moment of acquisition.

---

### UR-02: Initial Data Processing
* **SR-04:** The station shall reject readings that fall outside the valid range declared for the instrument and record the rejection.
* **SR-05:** The station shall compute summary values (maximum, minimum, mean, total) per reporting period from the accepted readings.
* **SR-06:** The station shall hold summarised data in non-volatile storage until transmission is acknowledged.

---

### UR-03: Weather Data Transmission
* **SR-06:** The station shall hold summarised data in non-volatile storage until transmission is acknowledged.
* **SR-07:** The station shall transmit the summarised data set to the data management system once per reporting period over the satellite link.
* **SR-08:** The station shall retry an unacknowledged transmission on the next reporting period without discarding the stored data.

---

### UR-04: Data Management
* **SR-09:** The data management system shall accept transmissions from every registered station and identify each record by station identifier and timestamp.
* **SR-10:** The data management system shall reject records from an unregistered station identifier and log the attempt.

---

### UR-05: Data Processing and Analysis
* **SR-11:** The data management system shall provide processing and analysis functions over the collected data in support of monitoring and forecasting.

---

### UR-06: Data Archiving
* **SR-12:** The data management system shall archive all accepted records permanently and make them retrievable by station, instrument and time range.

---

### UR-07: Station Health Monitoring
* **SR-18:** The station shall transmit outstanding fault reports to the maintenance system at the next available transmission opportunity.
* **SR-19:** The maintenance system shall display the current health status of every station and its outstanding faults.

---

### UR-08: Instrument Monitoring
* **SR-13:** The station shall test the condition of every instrument once per monitoring cycle.
* **SR-14:** The station shall classify each instrument as operational, degraded or failed.

---

### UR-09: Power System Monitoring
* **SR-15:** The station shall monitor battery charge level and wind-generator output once per monitoring cycle.

---

### UR-10: Communication Hardware Monitoring
* **SR-16:** The station shall monitor the satellite transceiver and record every failed link attempt.

---

### UR-11: Fault Detection and Reporting
* **SR-17:** The station shall raise a fault report identifying the faulty subsystem, the detected condition and the time of detection.
* **SR-18:** The station shall transmit outstanding fault reports to the maintenance system at the next available transmission opportunity.
* **SR-19:** The maintenance system shall display the current health status of every station and its outstanding faults.
* **SR-29:** The station shall record each failover event and include it in the next fault report.

---

### UR-12: Power Management
* **SR-20:** The station shall recharge its batteries whenever generated power exceeds current consumption.
* **SR-21:** When battery charge falls below the low-power threshold, the station shall reduce consumption by suspending non-essential functions.
* **SR-23:** Low-power and safe-wind thresholds shall be configurable station parameters.

---

### UR-13: Generator Protection
* **SR-22:** The station shall shut the wind generator down when measured wind speed exceeds the safe-operation threshold, and restart it when wind speed returns below that threshold.
* **SR-23:** Low-power and safe-wind thresholds shall be configurable station parameters.

---

### UR-14: Remote Maintenance
* **SR-02:** The collection cycle interval shall be a configurable station parameter.
* **SR-23:** Low-power and safe-wind thresholds shall be configurable station parameters.
* **SR-24:** The maintenance system shall authenticate an administrator before any station parameter may be changed.
* **SR-25:** The maintenance system shall allow an authenticated administrator to read and modify station parameters and to command a restart.

---

### UR-15: Dynamic Software Reconfiguration
* **SR-26:** The station shall accept a replacement software component delivered over the satellite link and install it without a full system shutdown.
* **SR-27:** The station shall verify the integrity of a downloaded component before activating it, and shall revert to the previous version if activation fails.

---

### UR-16: Backup Instrument Switching
* **SR-14:** The station shall classify each instrument as operational, degraded or failed.
* **SR-28:** On classifying a primary instrument as failed, the station shall switch acquisition to its backup instrument where one is configured.
* **SR-29:** The station shall record each failover event and include it in the next fault report.
* **SR-30:** Where no backup exists, the station shall continue collecting from all remaining instruments.

---

### UR-17: System Reliability
* **SR-08:** The station shall retry an unacknowledged transmission on the next reporting period without discarding the stored data.
* **SR-21:** When battery charge falls below the low-power threshold, the station shall reduce consumption by suspending non-essential functions.
* **SR-27:** The station shall verify the integrity of a downloaded component before activating it, and shall revert to the previous version if activation fails.
* **SR-30:** Where no backup exists, the station shall continue collecting from all remaining instruments.
* **NSR-01:** The station shall continue to operate without human intervention for the whole of a deployment period.
* **NSR-02:** No single instrument failure shall stop collection from the remaining instruments.
* **NSR-03:** No stored observation shall be lost as a result of a failed transmission attempt.
* **NSR-04:** The data management system shall remain available to receive station transmissions during scheduled maintenance of its analysis functions.

---

### UR-18: Remote Operation
* **NSR-05:** The station shall operate with no mains power and no wired network connection.
* **NSR-06:** The station shall operate across the full environmental range of its deployment site without manual adjustment.
* **NSR-07:** All corrective maintenance that does not require physical replacement of hardware shall be performable remotely.