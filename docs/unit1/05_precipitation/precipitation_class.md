# In-Class - Precipitation

These examples are the same type of problem as Homework Problems 1.18, 1.21, 1.22, 1.23 and 1.24: same equations, similar setup, different numbers.

Excel starter file: [Precipitation Example Template.xlsx](Precipitation%20Example%20Template.xlsx)

# Example A - Areal Rainfall: Arithmetic Mean vs. Thiessen

A small basin (10 km²) has four rain gauges, with these storm totals and Thiessen polygon areas:

| Gauge | P (in) | A (km²) |
|:---:|:---:|:---:|
| 1 | 1.5 | 2 |
| 2 | 2.0 | 4 |
| 3 | 2.5 | 3 |
| 4 | 1.0 | 1 |

Find the average areal rainfall using (a) the arithmetic mean and (b) the Thiessen polygon method, then (c) comment on the difference.

# Example B - Hyetograph from a Cumulative Rainfall Record

A USGS gauge records cumulative rainfall every 15 minutes during a 2-hour storm. Build the hyetograph (intensity in in/hr vs. time) and identify the time period with the highest rainfall intensity.

| t (hr) | 0 | 0.25 | 0.5 | 0.75 | 1.0 | 1.25 | 1.5 | 1.75 | 2.0 |
|---|---|---|---|---|---|---|---|---|---|
| Cum P (in) | 0 | 0.10 | 0.30 | 0.70 | 1.20 | 1.40 | 1.50 | 1.55 | 1.60 |

**Find**

a. Incremental rainfall in each 15-minute interval<br>
b. Intensity (in/hr) in each interval<br>
c. Time interval of maximum intensity

# Example C - Runoff Coefficient and Infiltration Loss

Use the same storm as Example B (1.60 in over 2 hr) on a 100-acre basin. The recorded streamflow hydrograph (already integrated for you) gives a total direct-runoff volume of about 6.67 ac-ft. Find the runoff coefficient C = R/P and the volume of water lost to infiltration during the storm (neglecting evaporation).

**Given**

- Storm depth P = 1.60 in
- Watershed area A = 100 acres
- Direct-runoff volume = 6.67 ac-ft
- Neglect ET

**Find**

a. Runoff depth R (in)<br>
b. Runoff coefficient C = R/P<br>
c. Infiltration volume (ac-ft)

# Example D - Reading an IDF Curve for Design Rainfall

You are designing a small storm drain whose contributing area has a time of concentration of about 30 minutes. The municipal standard requires a 10-year design return period. Use the IDF curve in Figure 1-15 (or a NOAA Atlas 14 lookup at the project location) to read the design rainfall intensity, and convert it to a design rainfall depth.

**Given**

- Time of concentration $t_c$ = 30 min
- Design return period T = 10 yr

**Find**

a. Design intensity i (in/hr)<br>
b. Design depth P (in) over $t_c$
