# 3. Problem Statement

Weather observations are needed from areas that have **no local infrastructure** —
no mains power, no wired network, no staff (Sommerville, 9th ed., Ch. 1, p. 19,
l. 6). Conventional instrumentation cannot be used there, because it assumes
someone is present to power it, read it and repair it.

The problem the system must solve therefore has four strands:

1. **Autonomy.** The station has to run unattended for long periods and cannot
   depend on human intervention to keep working (Ch. 1, p. 19, l. 12).
2. **Self-sufficiency in power.** With no grid connection, the station must
   generate, store and ration its own power, and protect its generator in
   dangerous conditions (Ch. 1, p. 19, ll. 14–17).
3. **Communication without a network.** The only route to the outside world is a
   satellite link, which is intermittent and expensive, so data must be processed
   and summarised locally before it is sent (Ch. 1, p. 20, ll. 22–23).
4. **Maintenance at a distance.** Faults must be detected by the station itself,
   reported to a maintenance system, and where possible corrected remotely — by
   failing over to a backup instrument or by downloading a replacement software
   component — because a site visit may be months away (Ch. 7, pp. 195, 197).

Without a system that addresses all four, remote weather data stays unavailable
or arrives too late and too incomplete to be useful for forecasting.
