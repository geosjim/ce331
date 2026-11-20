# In-Class - Flow Frequency

These examples use the same equations and workflow as the homework on the Spanish Fork River; only the numbers and the size of the record change.

Excel starter file: [Flow Frequency Example Template.xlsx](Flow%20Frequency%20Example%20Template.xlsx)

# Example A - Weibull Plotting Position

A small ungaged tributary has only n = 10 years of annual peak flows (cfs):

1200, 800, 950, 1300, 600, 1100, 700, 2200, 900, 1500

Use the Weibull plotting-position method to estimate the empirical annual exceedance probability (AEP) and return period (T) for each observation, and then estimate the 2-yr and 5-yr flows.

$$P = \frac{m}{n+1}, \qquad T = \frac{1}{P}$$

where m is the rank from largest (m = 1) to smallest, and n is the number of observations.

**Find:** rank m, AEP P, and T for each Q; $Q_2$ and $Q_5$ (the 2-yr and 5-yr empirical flows).

Hint: sort largest to smallest first. Interpolate to read off a specific T.

# Example B - Gumbel Method of Moments

Use the same 10-year sample as Example A. Fit a Gumbel (Extreme Value Type I) distribution by the method of moments and estimate the design flows for T = 2, 25, and 100 yr.

$$y_T = -\ln\left[-\ln\left(1 - \frac{1}{T}\right)\right]$$

$$x_T = \bar{x} - 0.45\,s + 0.7797\,s\,y_T$$

where $\bar{x}$ and $s$ are the sample mean and standard deviation of the annual peaks.

**Find:** the sample mean $\bar{x}$ and standard deviation $s$; $y_T$ for each T; $x_T$ = Q for T = 2, 25, and 100 yr.

Hint: use AVERAGE() and STDEV() in Excel. Keep at least 4 significant figures in $y_T$.

# Example C - Flow-Duration Curve

A small stream's monthly mean flows (cfs) for one water year are:

500, 600, 700, 800, 1500, 1200, 400, 300, 250, 350, 450, 480

Build the empirical flow-duration curve: rank the flows, assign exceedance probabilities, and read off $Q_{50}$ (median flow) and $Q_{90}$ (a common low-flow design index).

$$EP = \frac{m}{n+1}$$

EP is the fraction of time the discharge is equaled or exceeded (m = rank from largest).

**Find:** a ranked table of Q vs. EP, $Q_{50}$, and $Q_{90}$.

Hint: interpolate between adjacent EP rows. Q here is NOT a return-period flow.
