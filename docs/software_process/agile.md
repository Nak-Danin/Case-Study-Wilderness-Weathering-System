# Agile Development

## Where it is used

1. **The data management and archiving system** — the central server that
   receives, processes and stores data from every station.
2. **The station maintenance system** — the operator-facing application used to
   monitor station health and change station parameters.

## Book reference

Sommerville, *Software Engineering*, 9th ed., **Ch. 1, p. 20, ll. 24–30**.

Paraphrased: the data management and archiving system gathers data from all of
the wilderness weather stations, performs processing and analysis on it, and
archives it. The station maintenance system talks to the stations over satellite
to monitor their health and to adjust station parameters.

## Reasoning

1. **The requirements move.** Analysis, reporting and forecasting needs change as
   meteorologists work with the archive. Locking these down in a waterfall
   specification would freeze the wrong thing.
2. **Deployment is cheap.** These applications run on standard servers under the
   organisation's control, so an iterative release every few weeks carries none
   of the risk that a field update to a station carries.
3. **The customer is available.** Meteorologists and maintenance engineers are
   in-house, which makes short feedback loops and incremental delivery practical.
4. **Value can be delivered early.** A first increment that only ingests and
   stores data is already useful; analysis and reporting can follow.

## Requirements developed under this branch

UR-04, UR-05, UR-06, UR-07, UR-11, UR-14, UR-15.

## Suggested increment plan

| Increment | Delivered capability | Requirements |
|---|---|---|
| 1 | Ingest and store station transmissions | UR-04, UR-06 |
| 2 | Processing and analysis of stored data | UR-05 |
| 3 | Station health dashboard and fault reports | UR-07, UR-11 |
| 4 | Remote administration and parameter control | UR-14 |
| 5 | Remote component update over satellite | UR-15 |
