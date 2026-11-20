# In-Class - Weather

These examples are the same type of problem as Homework Problems 1.11, 1.15 and 1.16: same equations, similar setup, different numbers.

Excel starter file: [Weather InClass_Template.xlsx](Weather%20InClass_Template.xlsx)

Saturation vapor pressure curve setup (also used for Problem 1.11): [Problem1-11Setup.xlsx](Problem1-11Setup.xlsx)

# Example A - Saturation, Dew Point and Relative Humidity

Two air parcels are observed at the same temperature T = 25 °C, but with different actual vapor pressures e:

- Sample X: e = 20 mb
- Sample Y: e = 28 mb

Use the saturation vapor-pressure relation

$$e_s = 2.7489 \times 10^8 \cdot \exp\left(\frac{-4278.6}{T + 242.79}\right) \qquad [T \text{ in °C},\ e_s \text{ in mb}]$$

to find the saturation vapor pressure, the dew point, and the relative humidity for each sample. Then ask what happens to each parcel if it cools to 20 °C with no change in vapor content.

**Given**

- T = 25 °C for both samples
- Sample X: e = 20 mb
- Sample Y: e = 28 mb
- Cool both to 20 °C (no moisture change)

**Find**

a. $e_s$, $T_d$ and RH for each sample (use Goal Seek in Excel for the dew point)<br>
b. What happens to RH when both are cooled to 20 °C

# Example B - Vapor Pressure, RH and Specific Humidity

At a weather station the air pressure is P = 95 kPa, the air temperature is T = 28 °C, and the dew point temperature is $T_d$ = 20 °C. Find the actual vapor pressure e, the saturation vapor pressure $e_s$, the relative humidity RH, and the specific humidity q.

**Given**

- P = 95 kPa = 950 mb
- T = 28 °C
- $T_d$ = 20 °C
- $e_s(T) = 2.7489 \times 10^8 \cdot \exp\left(-4278.6/(T+242.79)\right)$
- $q = 0.622\,e / (P - 0.378\,e)$

**Find**

e, $e_s$, RH, q

# Example C - Atmospheric Stability from the Lapse Rate

An unsaturated air parcel cools at the dry adiabatic lapse rate (DALR) ≈ 9.8 °C/km as it rises. The environmental lapse rate (ALR) is whatever the surrounding atmosphere actually does. For each of the following measured atmospheres, decide whether a lifted unsaturated parcel finds itself warmer, cooler, or at the same temperature as its surroundings, and label the atmosphere as stable, unstable, or neutral:

a. ALR = 5 °C/km<br>
b. ALR = 12 °C/km<br>
c. ALR = 9.8 °C/km<br>
d. ALR = 0 °C/km (isothermal)

**Given**

- Surface $T_0$ = 30 °C
- DALR = 9.8 °C/km (parcel)
- Lift parcel by 1 km
- Compare to ambient $T(z) = T_0 - \text{ALR} \cdot z$

**Find**

a. Parcel vs. ambient temperature at 1 km<br>
b. Stable, unstable or neutral for each case
