# 2. Background

## 2.1 The case study

The wilderness weather station is the running case study introduced in
Sommerville, *Software Engineering*, 9th ed., Ch. 1, §1.3.2 (pp. 19–21) and
carried into the object-oriented design chapter, Ch. 7, §7.1 (pp. 188–198).

Paraphrasing the source (Ch. 1, p. 19, ll. 6–17): stations of this kind gather
weather information in remote areas that have no local infrastructure. They must
be reliable and run for long periods without anyone attending them, they manage
their own power by monitoring batteries and a generator, and they may shut the
wind generator down in high winds so it is not damaged.

## 2.2 Why the system exists

Meteorological services need observations from places where no staffed station
can be maintained: mountain ranges, deserts, ice fields. A network of unattended
stations feeding a central archive gives that coverage, provided each station can
survive on its own between visits.

## 2.3 Existing situation

- Weather data from remote regions is sparse or absent.
- Where instruments do exist, readings must be collected manually on site visits.
- There is no single archive that consolidates data from every remote location.
- Instrument or power faults are only discovered on the next visit, so months of
  data can be lost.

## 2.4 Classification basis

Requirements are classified using Sommerville, Ch. 4, §4.1:

- **Functional requirements** (p. 85, ll. 3–6) describe the services the system
  provides, how it reacts to inputs, and how it behaves in particular situations.
- **Non-functional requirements** (p. 87, ll. 1–4) are constraints on those
  services — timing, process, standards and similar.
