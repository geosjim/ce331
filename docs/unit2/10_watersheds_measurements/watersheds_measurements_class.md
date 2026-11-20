# In-Class - Watersheds and Measurements

These examples mirror Homework Problems 1.25, 1.28, and the annual hydrograph problem: the same type of problem, with different numbers.

Excel starter file: [Watersheds and Measurements Example Template.xlsx](Watersheds%20and%20Measurements%20Example%20Template.xlsx)

# Example A - Stream Discharge by the Velocity-Area Method

A small creek is gauged using the velocity-area method. The crew sets up seven stations across the channel at 5 ft spacing and measures depth and average velocity at each station. The endpoints A and G are at the banks (D = v = 0).

| Station | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| Distance (ft) | 0 | 5 | 10 | 15 | 20 | 25 | 30 |
| Depth D (ft) | 0 | 0.8 | 1.6 | 2.0 | 1.8 | 1.0 | 0 |
| Velocity v (ft/s) | 0 | 0.5 | 1.2 | 1.5 | 1.3 | 0.6 | 0 |

Find $\Delta W$ for each station (half-distances) and the total discharge through the cross-section, $Q = \sum v_i D_i \Delta W_i$ (cfs).

# Example B - Hyetograph from a Cumulative Rainfall Record

A rain gauge records cumulative rainfall every 30 minutes during a 3-hour storm:

| Time (hr) | 0 | 0.5 | 1.0 | 1.5 | 2.0 | 2.5 | 3.0 |
|---|---|---|---|---|---|---|---|
| Cumulative P (in) | 0.0 | 0.1 | 0.4 | 1.0 | 1.6 | 1.9 | 2.0 |

Compute the gross rainfall per 30-minute interval, convert each to an intensity in in/hr to build the hyetograph, and report the maximum and average rainfall intensity over the storm.

# Example C - Building an Annual Hydrograph from USGS Data

Download an annual streamflow record from a real USGS gauge and produce a hydrograph. We will use the Provo River near Provo, UT (USGS gauge 10163000) for one water year (the slides use water year 2023; the starter file's steps use October 1, 2023 - September 30, 2024). A water year runs October 1 - September 30 to keep the spring snowmelt season inside one year.

**Given:** USGS NWIS ([https://apps.usgs.gov/nwismapper/](https://apps.usgs.gov/nwismapper/)), site 10163000, daily mean discharge in cfs.

**Find:** the steps to retrieve the data, an annual hydrograph plot, and the snowmelt peak, baseflow, and recession on that plot.

# Example D - Reservoir Hydrographs

Daily reservoir data (Deer Creek, starting May 1991) give the inflow (cfs) and the daily change in storage (acre-ft/day). Convert the storage change to cfs (1 acre-ft/day = 0.50417 cfs) and compute the outflow from continuity,

$$Q_{out} = Q_{in} - \frac{\Delta S}{\Delta t}$$

then plot the inflow and outflow hydrographs on one chart. The homework asks you to repeat this for a different reservoir.

Data file: [Hydrograph_reservoir.xlsx](Hydrograph_reservoir.xlsx)
