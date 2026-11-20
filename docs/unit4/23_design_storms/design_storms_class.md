# In-Class - Design Storms

These examples mirror Parts 1 and 2 of the Provo Urban Hydrology homework.

Excel starter file: [Design Storms Example Template.xlsx](Design%20Storms%20Example%20Template.xlsx)

# Example A - Time of Concentration (TR-55)

A 35-acre residential watershed near University Parkway in Orem drains to a storm-drain inlet at point D. The flow path consists of three TR-55 segments: sheet flow over lawn, shallow concentrated flow in a backyard swale, and storm-drain pipe flow.

- Sheet flow: $T_t = \dfrac{0.007\,(nL)^{0.8}}{P_2^{0.5}\,s^{0.4}}$
- Shallow concentrated flow: V from TR-55 Fig. 3-1, then $T_t = L/(3600\,V)$
- Pipe flow: $V = \dfrac{1.49}{n} R^{2/3} s^{1/2}$, then $T_t = L/(3600\,V)$

**Given:**

| Segment | Type | L (ft) | s | n |
|---|---|---|---|---|
| A-B | Sheet flow, dense grass | 120 | 0.018 | 0.24 |
| B-C | Shallow concentrated, unpaved | 550 | 0.011 | |
| C-D | 24-in storm drain, half-full | 750 | 0.008 | 0.013 |

- A = 35 ac
- P₂ (2-yr, 24-hr, NOAA Atlas 14, Orem) = 2.0 in

**Find:**

- T<sub>t</sub> for each segment (min)
- Total T<sub>c</sub> (min)
- Which segment controls?

# Example B - IDF Curve and Rational Method

With T<sub>c</sub> ≈ 29 min from Example A, look up the design rainfall intensity from NOAA Atlas 14 (Orem) for a duration equal to T<sub>c</sub> and use the Rational Method, Qp = C·i·A, to compute the peak design flow for the 10- and 100-yr return periods. Use a composite runoff coefficient C = 0.55 (mixed residential with lawn, roof, and street). Note that 1 in/hr × 1 ac = 1.008 cfs ≈ 1 cfs.

**Given:**

- T<sub>c</sub> = 29 min (from Example A)
- A = 35 ac, C = 0.55
- From NOAA Atlas 14 at a duration of about 30 min: i₁₀ ≈ 1.85 in/hr, i₁₀₀ ≈ 3.00 in/hr

**Find:**

- Design duration
- Q<sub>p,10</sub> and Q<sub>p,100</sub> (cfs)

# Example C - Alternating-Block Design Hyetograph

Build a 10-yr design storm for the Orem basin as a 60-minute hyetograph at 10-minute increments using the alternating-block method. The NOAA Atlas 14 average intensities for the 10-yr return period are:

| d (min) | 10 | 20 | 30 | 40 | 50 | 60 |
|---|---|---|---|---|---|---|
| i (in/hr) | 3.00 | 2.50 | 2.10 | 1.85 | 1.65 | 1.50 |

Convert these to cumulative depths, then to incremental depths per 10-min block. Rank the increments from largest to smallest and arrange them in the time series with the peak placed in the middle, alternating the remaining blocks on each side. (This is the same method used by HEC-HMS's "Frequency Storm" option.)

**Find:**

- ΔP for each block (in)
- Alternating-block order
- Hyetograph (in/hr)
