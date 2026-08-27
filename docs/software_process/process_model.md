# 1. What software process does the Wilderness Weather Station use?

### Answer: Hybrid Process (Plan-driven + Agile/Incremental Development)

### References: Sommerville, I. (2015). Software Engineering (10th ed.). Pearson. Chapter 3, Section 3.4.2, “Agile and plan-driven methods,” pp. 83–84.

### Explaination:

```text
    The Wilderness Weather Station can be considered a hybrid process because the system contains
    areas that require plan-driven development, such as hardware, power management, generator
    protection, and reliability, while other software functions can be developed incrementally.
    This interpretation is based on Sommerville's discussion that software projects can combine
    practices from plan-driven and Agile approaches.
```

---

## 1.1 Which part is Plan-Driven Development?

### References: Software Engineering (9th Edition), Chapter 1, Page 20, Lines 5–18

```text
    The important characteristic of the weather station is that it has to be entirely
    self-contained... This means that the system has to have its own power generation capability...
    communicates via satellite and must be able to reconfigure itself... The software is embedded in
    that it is part of a wider hardware/software system...
```

### Answer: Hardware + Embedded System Requirements:

```text
    Sensors
    Power System
    Generator
    Communication
    Backup Instruments
```

**Reasoning:** System hardware must be specified and built up front; embedded failure safety
requires rigorous,plan-driven upfront modeling.

---

## 1.2 Which part is Agile/Incremental Development?

### Reference: Software Engineering (9th Edition), Chapter 1, Page 20, Lines 5–18

```text
    The data management and archiving system... collects the data from all of the wilderness weather
    stations, carries out data processing and analysis and archives the data.
```

### Answer: Software and Data Management

```text
    Data Processing
    Monitoring UI
    Analysis
```

**Reasoning:** Central software applications running on standard servers have changing business/user
requirements and benefit from continuous iterative releases.

## Other Methods: Dynamic Component-Based Software Reconfiguration

**Where used:** Dynamic updates on the remote station software **(UR-15)**

### References: Software Engineering (9th Edition), Chapter 7, Page 197, Lines 8–15

```text
    Dynamic software reconfiguration... allows components of the weather station software to be
    updated remotely by downloading new versions of these components over the satellite link without
    shutting down the system.
```
