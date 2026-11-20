# In-Class - Snow

These examples are the same type of problem as Homework Problems 1-4: same equations, similar setup, different numbers.

Excel starter file: [Snow Example Template.xlsx](Snow%20Example%20Template.xlsx)

# Example A - SWE and Snowmelt Runoff Volume

An 8 mi² mountain basin holds an average snow depth of 90 cm with a measured bulk snow density of 250 kg/m³. Compute the snow water equivalent (SWE) in mm and inches, then estimate the total runoff volume in acre-feet that would result if the entire snowpack melted (ignore losses to evaporation, sublimation, or infiltration).

**Given**

- Basin area A = 8 mi²
- Snow depth $d_s$ = 90 cm
- Snow density $\rho_s$ = 250 kg/m³
- All snow becomes runoff (no losses)
- $SWE = 0.01 \cdot d_s \cdot \rho_s$

**Find**

a. SWE (mm and in)<br>
b. Total melt runoff volume (acre-ft)

# Example B - Degree-Day Melt by Elevation Band

A snowmelt basin has two elevation bands:

- 70% of the area at 2,200 m (mean daily air temperature = +2 °C)
- 30% of the area at 2,800 m

Use a temperature lapse rate of 1 °C/100 m, base melt temperature $T_b$ = 0 °C, and snow density $\rho_s$ = 300 kg/m³.

**Given**

- $M = D_f (T_i - T_b)$
- $D_f = 0.011 \cdot \rho_s$ (mm/day·°C)

**Find**

a. Daily melt in each band (mm/day)<br>
b. Basin-average daily melt (mm/day)<br>
c. 5-day total (mm)

# Example C - Albedo Effect on Melt (Energy Shortcut)

Incoming shortwave radiation at the snow surface is 600 ly/day. Other energy fluxes (net longwave + sensible + latent + ground + rain heat) sum to +40 ly/day. The pack is ripe (ready to melt). Compute the daily melt depth for (1) fresh snow with albedo α = 0.85 and (2) aged, dirty snow with α = 0.40, using the energy shortcut

$$Q_n = (1 - \alpha) \cdot SW + \text{Other} \qquad M = \Delta H / 80 \text{ (cm/day)}$$

**Find**

a. Daily melt for each albedo (cm/day and in/day)<br>
b. Ratio of melt between the two cases

# Example D - Snow Line, Areal Coverage and Basin Melt

A basin's area-elevation distribution is:

- 30% below 1,900 m
- 40% between 1,900 and 2,300 m
- 30% above 2,300 m

During a recent storm the freezing level was at 2,100 m, so precipitation fell as snow above 2,100 m and rain below. The next day, the index station at 2,100 m has a mean daily air temperature of +5 °C. Use $D_f$ = 2.5 mm/day·°C and $T_b$ = 0 °C.

**Find**

a. Fraction of the basin that is snow-covered (%)<br>
b. Basin-average daily melt (mm/day)
