# Functional Requirements (UR-01 … UR-16)

**Definition applied** — Sommerville, 9th ed., Ch. 4, p. 85, ll. 3–6: functional
requirements state the services the system should provide, how it should react
to particular inputs, and how it should behave in particular situations.

| UR ID | Source (page & line) | Source content, paraphrased | User statement |
|---|---|---|---|
| UR-01 | Ch.1, p.20, l.10 | Stations gather readings from a set of instruments measuring temperature, pressure, sunshine, rainfall, wind speed and wind direction | "The system must collect temperature, humidity, wind speed/direction, rainfall and other sensor measurements periodically." |
| UR-02 | Ch.1, p.20, l.22 | The station software is responsible for collecting the weather data and performing initial processing on it | "The system must validate, filter and summarise raw sensor data before sending it out." |
| UR-03 | Ch.1, p.20, l.23 | …and for transmitting that data to the data management system | "The station must transmit collected weather data to the central Data Management and Archiving System." |
| UR-04 | Ch.1, p.20, l.25 | The central system gathers data from every wilderness weather station | "The central server system must collect and organise incoming data sent from multiple weather stations." |
| UR-05 | Ch.1, p.20, l.26 | It performs data processing and analysis | "The system must process and analyse weather data to support monitoring and forecasting." |
| UR-06 | Ch.1, p.20, l.27 | …and archives the data | "The system must archive historical weather data for long-term retrieval and analysis." |
| UR-07 | Ch.1, p.20, l.30 | The maintenance system uses satellite communication with all stations to monitor their health | "The system must remotely monitor overall station health status via satellite communications." |
| UR-08 | Ch.7, p.191, l.14 | The system monitors the condition of all instruments and reports problems to the maintenance system | "The station software must continuously test instruments and flag operational anomalies or failures." |
| UR-09 | Ch.1, p.19, l.15 | The station manages its own power, monitoring its batteries and generator | "The software must monitor battery charge, generator output and report power issues." |
| UR-10 | Ch.7, p.192, l.8 | The communication system monitors transmission hardware and reports link failures | "The system must monitor satellite communication hardware and log transmission failures." |
| UR-11 | Ch.1, p.20, l.31 | …and provides reports of problems | "The system must detect critical hardware/software faults and issue diagnostic fault reports to maintenance." |
| UR-12 | Ch.1, p.19, l.14 | Power has to be managed in situations where the available supply is restricted | "The system must manage power consumption and recharge batteries whenever conditions permit." |
| UR-13 | Ch.1, p.19, l.17 | The system may shut the wind generator down in high winds so the generator is not damaged | "The system must shut down the generator in hazardous conditions like extreme winds to protect hardware." |
| UR-14 | Ch.1, p.20, l.29 | The station maintenance system communicates by satellite in order to control station parameters | "The system must support remote administrative login to control station state and perform maintenance." |
| UR-15 | Ch.7, p.197, l.9 | Dynamic software reconfiguration lets components be updated remotely without shutting the system down | "The system software must support dynamic component replacement/updates remotely with minimal disruption." |
| UR-16 | Ch.7, p.195, l.18 | If an instrument fails, the system switches to a backup instrument where one is available | "The system must automatically failover to a backup sensor whenever a primary instrument fails." |

## Grouping

- **Data acquisition:** UR-01, UR-02, UR-03
- **Central data services:** UR-04, UR-05, UR-06
- **Monitoring and fault reporting:** UR-07, UR-08, UR-10, UR-11
- **Power management:** UR-09, UR-12, UR-13
- **Remote administration:** UR-14, UR-15
- **Fault tolerance:** UR-16
