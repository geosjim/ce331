# Homework - Distributions

You will use the Spanish Fork streamflow and precipitation data files for these three problems. Instructions for how to use Excel to do these exercises are given below.

Data files:

- [Spanish_Fork_daily-data-mean.xlsx](Spanish_Fork_daily-data-mean.xlsx) - daily mean discharge, Spanish Fork at Castilla (USGS 10150500)
- [Spanish_Fork_monthly-precipitation.xlsx](Spanish_Fork_monthly-precipitation.xlsx) - monthly precipitation, Spanish Fork Power House (GHCN USC00428119)

Excel template: [Distributions HW Template.xlsx](Distributions%20HW%20Template.xlsx)

## Problem 1 - Annual maximum series: histograms, moments, and fitted distributions

a. From the daily record, extract the maximum daily mean discharge for each calendar year.

b. Build a relative frequency histogram and a cumulative frequency histogram of the annual maximum series using a class interval of 250 cfs, with class limits running 250, 500, 750, … up to 3750 cfs.

c. Report the mean, median, standard deviation, and coefficient of skew of the annual maximum series. Compare the mean and the median: what does the sign and size of the skew tell you about the shape?

d. Repeat the four statistics on the base-10 logarithms of the annual maxima. Is Q or log Q closer to a normal distribution and by what evidence? Keep the mean, standard deviation, and skew of log Q: they are exactly what USGS Bulletin 17C requires to fit a Log-Pearson Type III distribution, and you will enter them in PeakFQ in the next assignment.

e. Overlay two fitted curves on your relative frequency histogram, both by the method of moments: a normal PDF from the mean and standard deviation of Q, and a lognormal PDF from the mean and standard deviation of log Q. Comment on how each fit succeeds and what the normal distribution model implies about the probability of a discharge below 250 cfs, given that the smallest annual peak in 91 years is 437 cfs.

### How to build the annual maximum series in Excel

- See the instructions from the previous assignment on using a PivotTable.
- Copy the 91 annual maxima into the homework template.
- Statistics: `=AVERAGE()`, `=MEDIAN()`, `=STDEV.S()` (or `=STDEV()`), `=SKEW()`. Excel's `SKEW()` uses the same n/((n-1)(n-2)) form as Eq. 3.40 in the text.
- For part (d), add a column of `=LOG10(Q)` and run the same four functions on it.

### How to build the histograms

1. In a new column, list your bin upper limits: 250, 500, 750, 1000, … up to 3750. These are the class limits, not the data.
2. Next to the bins, enter the counts with a single array formula: select the whole column of count cells, type `=FREQUENCY(data_range, bin_range)` and press Ctrl+Shift+Enter (in Microsoft 365 just press Enter).
3. Relative frequency: divide each count by the total number of annual maximum flows (should be 91) in the next column.
4. Cumulative frequency: in the next column, running sum of the relative frequencies, which should end at 1.00.
5. Select the bin column and the relative frequency column > Insert > Charts > Clustered Column. Then right-click a bar > Format Data Series > Gap Width = 0. A histogram has no gaps between bars; a bar chart does.
6. Label the x-axis "Annual maximum discharge (cfs)" and the y-axis "Relative frequency." Repeat with the cumulative column for the second chart.

### How to overlay the normal distribution

1. Add a column of bin midpoints beside your bins: for the 0-250 bin the midpoint is 125, for 250-500 it is 375, for 500-750 it is 625, and so on.
2. In the next column, compute the normal PDF at each midpoint: `=NORM.DIST(midpoint, $mean$, $stdev$, FALSE)`. The FALSE argument returns the density, not the cumulative probability. (`=NORMDIST()` is the equivalent older name and works in every version of Excel.)
3. Scale the density so it is comparable to your relative frequencies: multiply each PDF value by the class interval (250 cfs). This converts a density per cfs into the probability of falling in that 250-cfs class.
4. Select your chart > right-click > Select Data > Add, and add this scaled column as a new series.
5. Right-click the new series > Change Series Chart Type > Line with Smooth Markers, so it plots as a curve across the bars rather than as more bars.
6. Read the comparison bin by bin: where the curve sits above the bars the normal model over-predicts how often that range occurs, and where it sits below, it under-predicts.

### How to overlay the lognormal distribution

1. You already have the base-10 logs and their mean and standard deviation from part (d), and the lognormal uses those same two numbers as its parameters. They are NOT the mean and standard deviation of Q.
2. At each bin midpoint x, the lognormal density is `=NORM.DIST(LOG10(x), mean_logQ, stdev_logQ, FALSE)/(x*LN(10))`. The division by x·ln(10) is the Jacobian of the log transform, and it converts a density measured in log units back into a density in cfs. If you leave it out the curve will not integrate to 1.
3. Scale it the same way as the normal: multiply by the class interval (250 cfs).
4. Add this column to the chart as a second line series.
5. Compare the two curves against the bars. The lognormal is bounded at zero and right-skewed, so it should sit higher near the mode and keep more probability in the right tail.

## Problem 2 - Monthly precipitation at Spanish Fork

Using the Spanish Fork monthly precipitation totals for January 2016 through December 2025 at the Spanish Fork Power House station (GHCN USC00428119, NOAA NCEI):

a. Begin by counting the reported months with `=COUNT()`. The record should span 120 months.

b. Create a relative frequency and a cumulative frequency graph of the monthly totals using a 0.5-in. class interval. Calculate the mean, median, standard deviation, and skew, and overlay a normal PDF. Are the data normally distributed? Comment on what the normal model implies about negative precipitation.

c. Compare your skew from part (b) with the skew of the annual peak discharges from Problem 1, and explain in two or three sentences why two hydrologic variables measured in the same basin behave so differently.

Use the same histogram and normal-overlay procedures given under Problem 1. Note that a lognormal fit is not available here: several months report exactly 0.00 in. and the logarithm of zero is undefined.

## Problem 3 - Averaging interval: daily, monthly, and annual mean flow

Using the daily mean record for calendar year 2023 from the Spanish Fork streamflow data:

a. Plot the daily mean discharge for the year with date on the x-axis and discharge on the y-axis. Report the peak daily mean and the month it occurred.

b. Compute the mean discharge for each of the twelve months and add them to the chart as a second series. Report the highest monthly mean and the month it occurred.

c. Compute the mean discharge for the whole year and add it as a third, flat series. Report that value.

d. Express the monthly peak and the annual mean as percentages of the daily peak. Explain in two or three sentences why the reported maximum falls as the averaging interval lengthens, and why the maximum of an averaged series can never exceed the maximum of the series it was averaged from.

e. The annual maximum series you built in Problem 1 came from daily mean values. Based on what you found here, is that series biased high, biased low, or unbiased as an estimate of the true annual peaks? What does that imply about the design discharges the Flow Frequency assignment will estimate from it?

### How to build the three series in Excel

1. Filter the daily record to 1 January 2023 through 31 December 2023 into 365 rows.
2. Use a PivotTable to get the monthly average flows. This is the same as before, but instead of having the value be maximum it will be average.
3. Paste the twelve monthly averages as values, then add them to the daily chart with right-click > Select Data > Add.
4. For the annual mean, `=AVERAGE()` over all 365 daily values. To draw it as a flat line, fill a column with that single value repeated, and add that column as a third series.
5. Peaks: `=MAX()` on each of the three series. Percentages are each peak divided by the daily peak.

## Submission

Upload your work to the matching assignment in Canvas.

!!! note "Do not put your name or NetID in the file"
    Canvas records who submitted each file, so your name is not needed
    inside the file itself. This applies to scans and photos too — please
    don't write your name on the page.

## Grading Rubric

**Total: 9 points**

Each problem is scored 0-3: 0 nothing submitted, 1 an intelligent attempt, 2 complete with some errors, 3 correct within a reasonable tolerance.

| Criteria | Points |
|---|:---:|
| Problem 1: Annual maximum series - histograms, moments of Q and log Q, normal and lognormal overlays | 3 |
| Problem 2: Monthly precipitation - moments, histogram, normal overlay | 3 |
| Problem 3: Averaging interval - daily vs monthly vs annual mean flow for 2023 | 3 |
