# In-Class - Distributions

Both examples use the same file. The example uses USGS gauge 10153100; the homework uses Spanish Fork.

Excel starter file: [Distributions InClass Example Template.xlsx](Distributions%20InClass%20Example%20Template.xlsx)

# Example A - Histogram and Two Fitted Distributions

Open sheet "Example A". It holds 17 annual maximum daily mean discharges for USGS gauge 10153100, 2009 through 2025 - small enough to see every value at once.

Build the relative-frequency histogram with a 100-cfs class interval, then overlay a normal and a lognormal PDF, both fit by the method of moments.

**Given:** n = 17 annual maxima (cfs); class interval = 100 cfs; Excel functions AVERAGE, MEDIAN, STDEV, SKEW, FREQUENCY (entered as an array), and NORMDIST(x, µ, σ, FALSE).

**Find:**

- The mean, median, standard deviation, and skew of Q and of log₁₀Q
- A relative-frequency histogram (and cumulative frequency)
- A normal PDF on the same axes, and a lognormal PDF alongside it
- The probability of Q < 0 under the normal model
- Which distribution fits, and why

# Demonstration - What Averaging Interval Does to a Flood Peak

Open sheet "Demonstration": USGS 10153100, calendar year 2023, the largest flood in that record.

1. Column D: `=MONTH(B20)`.
2. Column E: `=AVERAGEIF($D$20:$D$384,D20,$C$20:$C$384)` - each month's average repeated on every day of that month.
3. Column F: `=AVERAGE($C$20:$C$384)` filled down - the annual mean as a flat line.
4. Plot the daily, monthly, and annual series on one date axis.

**Find:** the peak of the daily mean series, the peak of the monthly mean series, the annual mean, and the monthly peak and annual mean as percentages of the daily peak.
