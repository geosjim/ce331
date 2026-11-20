# In-Class - Hydrologic Modeling and Review

We will work five review examples together. Each example is followed by a practice problem that uses the same equations and setup with different numbers; try the practice problems on your own and we will review them. After the review we walk through a single-basin WMS / HEC-HMS demonstration.

# Example A - Reservoir Water Balance

A 1,500-acre upland watershed drains to a small reservoir of 200 surface acres, monitored for 30 days. Steady inflow from a small creek averages 12 cfs. A controlled outlet releases water at 14 cfs. Over the 30-day period rainfall of 4.0 in. fell uniformly over the entire watershed (including the reservoir). Runoff to the reservoir from the surrounding land surface was 22 percent of the precipitation falling on the land. Reservoir-surface losses were evaporation = 4.5 in. and seepage = 0.8 in. No WWTP discharge for this case. Find the change in reservoir storage in acre-feet over the 30-day period (positive = gain).

Find: each term in ac-ft, $\Delta S$ in ac-ft, and whether the reservoir gained or lost water.

## Practice A' - Reservoir Water Balance

A reservoir of 900 ac sits inside a 2,200-ac watershed and is monitored for 45 days. River inflow upstream = 18 cfs. WWTP discharge directly into the reservoir = 6 cfs. Controlled outflow = 22 cfs. Precipitation = 3.6 in. uniformly over the entire watershed (including the reservoir). Land-surface runoff to the reservoir = 18 percent of precipitation falling on the land. Reservoir-surface evaporation = 5.1 in.; seepage = 1.2 in. Find the change in storage in ac-ft and decide whether the reservoir gained or lost water.

# Example B - Hyetograph and Horton Infiltration

A 320-ac (0.5 mi²) watershed near Spanish Fork records a storm with cumulative rainfall:

| t (hr) | 0 | 1 | 2 | 3 | 4 |
|---|:---:|:---:|:---:|:---:|:---:|
| ΣP (in.) | 0.0 | 0.8 | 2.2 | 3.0 | 3.4 |

Use Horton's equation with $f_0$ = 0.9 in/hr, $f_c$ = 0.25 in/hr, $k$ = 0.40 hr$^{-1}$.

a. Build the incremental hyetograph (in/hr per hour).<br>
b. Compute the average infiltration rate during each hour.<br>
c. Sum to get total infiltration depth.<br>
d. Compute total runoff depth (in.) and runoff volume (ac-ft).

## Practice B' - Hyetograph and Horton Infiltration

A 640-ac (1 mi²) watershed records cumulative rainfall:

| t (hr) | 0 | 1 | 2 | 3 | 4 |
|---|:---:|:---:|:---:|:---:|:---:|
| ΣP (in.) | 0.0 | 1.0 | 2.5 | 3.3 | 3.7 |

Use Horton's equation with $f_0$ = 1.0 in/hr, $f_c$ = 0.3 in/hr, $k$ = 0.35 hr$^{-1}$.

a. Construct the hyetograph and compute incremental P.<br>
b. Compute the average infiltration rate each hour.<br>
c. Compute total infiltration depth in inches.<br>
d. Compute total runoff in ac-ft.

# Example C - SCS Curve Number Runoff

Same 320-ac Spanish Fork watershed. Land cover is open grassland in fair condition. Soils are entirely hydrologic group D. A design storm delivers P = 3.4 in.

a. Look up CN from Table 2-1 (open grassland, fair condition, group D).<br>
b. Compute $S = 1000/CN - 10$ and the initial abstraction $I_a = 0.2S$.<br>
c. Verify $P > I_a$, then compute Q from the SCS runoff equation.<br>
d. Convert Q (in.) to runoff volume (ac-ft).

## Practice C' - SCS Curve Number Runoff

Reuse the storm from Practice B' (P = 3.7 in. over the same 640-ac watershed). Land cover is open grassland in good condition. Soils are entirely hydrologic group D.

a. Look up CN from Table 2-1.<br>
b. Compute S, $I_a$, and check $P > I_a$.<br>
c. Compute Q (in.) from the SCS equation.<br>
d. Convert to runoff volume in ac-ft and compare to the Horton answer from B'.

# Example D - Unit Hydrograph Convolution

A 600-ac watershed has a 1-hr unit hydrograph with ordinates:

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| U (cfs) | 0 | 30 | 80 | 60 | 25 | 0 |

A storm delivers net rainfall excess of 0.6 in. in hour 1, 1.0 in. in hour 2, and 0.4 in. in hour 3. Compute the storm direct-runoff hydrograph by add-and-lag and identify the peak.

Find: the storm hydrograph Q(t), the peak Q (cfs), and the time to peak (hr).

## Practice D' - Unit Hydrograph Convolution

A 1-hr unit hydrograph for a watershed has ordinates:

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| U (cfs) | 0 | 40 | 90 | 70 | 30 | 0 |

A storm produces net rainfall excess of 0.5 in. in hour 1, 1.2 in. in hour 2, and 0.6 in. in hour 3.

a. Compute the storm hydrograph by add-and-lag.<br>
b. Identify the peak discharge (cfs) and time-to-peak (hr).<br>
c. Sum the ordinates as a quick volume check.

# Example E - Is It a Unit Hydrograph?

A consultant hands you a triangular direct-runoff hydrograph for a 600-ac watershed: $Q_{peak}$ = 200 cfs; rise time = 2 hr; fall time = 4 hr; baseflow = 0. They claim it is the 1-hr unit hydrograph for the basin. Verify by:

a. Computing the area under the triangle (DRO volume in cfs-hr).<br>
b. Converting cfs-hr to ac-in.<br>
c. Dividing by the watershed area to get a depth in inches.<br>
d. Comparing to 1.00 in.

## Practice E' - Is It a Unit Hydrograph?

A measured direct-runoff hydrograph from a 1,280-ac watershed is:

| t (hr) | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Q (cfs) | 0 | 120 | 260 | 340 | 280 | 180 | 80 | 0 |

a. Compute the runoff volume in cfs-hr (sum Q·Δt with Δt = 1 hr; trapezoidal).<br>
b. Convert to ac-ft.<br>
c. Convert to runoff depth in inches over the watershed.<br>
d. Decide whether this is a unit hydrograph (depth = 1.0 in.?).

# Model Demonstration - WMS / HEC-HMS

After the review we build a single-basin model in WMS / HEC-HMS: delineate the watershed, compute a curve number from land use and soils, choose a unit hydrograph method, apply a design hyetograph, run the model, and check the sensitivity of the results.
