# Homework 12 - Flow Frequency

**Data:** USGS gauge 10150500, Spanish Fork River. Work in the Flow Frequency HW Template. The 91 annual peak discharges (1935-2025) are provided on the Problem 1 and Problem 2 sheets; the Problem 5 sheet holds the full daily mean record for the same gauge and period. This is the same data you used for the Distributions assignment. You do not need any other data files, but I hope you understand where they come from.

Excel template: [Flow Frequency HW Template.xlsx](Flow%20Frequency%20HW%20Template.xlsx)

PeakFQ input file (Part 3): [SpanishFork_AnnualPeaks_PeakFQ.csv](SpanishFork_AnnualPeaks_PeakFQ.csv)

Parts 1 through 3 estimate design return-period discharges three different ways. Part 4 collects them in one table and one plot for comparison. Part 5 looks at the complete flow record rather than just the peaks to create a flow duration curve. Parts 6 through 8 ask what a design discharge actually means for a structure that has to survive a project lifetime, using the risk and reliability material in Section 3.5 of the text.

## Part 1 - Annual peak series and Weibull plotting positions

The 91 annual peak discharges show the maximum daily mean flow in each calendar year from 1935 through 2025 on the Problem 1 sheet.

Sort the peaks largest to smallest, assign ranks m = 1 to 91, and compute the empirical exceedance probability and return period with the Weibull plotting formula. Estimate the return-period Q at T = 2, 5, 10, 25, 50, and 100 yr by interpolating between the ranks that bracket each target.

$$P = \frac{m}{n+1}, \qquad T = \frac{1}{P}, \qquad \text{so the rank corresponding to } T \text{ is } m = \frac{n+1}{T}$$

With n = 91 the largest observed peak plots at T = n + 1 = 92 yr, so T = 100 falls just past the end of the record. Extend the curve through your top two plotting positions and report a best estimate rather than leaving it blank, and then say in one sentence what you assumed to extend it. Add your results for Weibull to the Problem 4 comparison table.

## Part 2 - Gumbel distribution, method of moments

The same 91 annual peaks are repeated on the Problem 2 sheet. Compute the mean and the standard deviation of the peaks there, then apply the Gumbel method-of-moments quantile to estimate Q for the same six return periods. Copy the results to the table for Problem 4.

$$x_T = \bar{x} - 0.45\,s + 0.7797\,s\left(-\ln\left[-\ln\left(1 - \frac{1}{T}\right)\right]\right)$$

## Part 3 - Log-Pearson Type III per USGS Bulletin 17C

Open the USGS PeakFQ web tool at [https://rconnect.usgs.gov/peakfq/](https://rconnect.usgs.gov/peakfq/) and upload SpanishFork_AnnualPeaks_PeakFQ.csv (linked above). It holds the same 91 annual peaks listed on the Problem 1 sheet, so every part of this assignment analyses one consistent record. PeakFQ could get the data from NWIS directly, but it won't match the record used in the first two problems.

Run the analysis with the default Bulletin 17C settings - Expected Moments Algorithm with station skew. Record the discharge AND the 5% / 95% confidence bounds for each of the six return periods in the Problem 3 sheet. Copy the results into the Part 4 comparison.

Download the frequency-curve plot PeakFQ produces (the one showing the gaged peak discharges, the fitted frequency curve, and the 5% and 95% confidence limits) and paste it into the sheet for Problem 3.

PeakFQ works in log space internally, so you do not transform the data yourself. Check what it reports: 91 years, 1935-2025, and a station skew near 1.82.

## Part 4 - Comparison table and frequency plot

The Problem 4 sheet collects all three sets of estimates in one table. Plot Weibull, Gumbel, and LP3 on a single chart, with discharge on the vertical axis and return period on a logarithmic horizontal axis.

Then answer, in three to five sentences:

a. At which return period do the three methods agree most closely, and why should that be expected?<br>
b. At which return period do they differ most? Which method gives the largest estimate there, and which the smallest?<br>
c. Your Weibull value at T = 100 is an extrapolation of one step past the record, while the Gumbel and LP3 values come from fitted distributions. Which do you trust more at that return period, and why?<br>
d. Which of the three estimates would you take into a design, and why?

## Part 5 - Annual flow duration curve

Using the complete daily record on the Problem 5 sheet, construct the annual (also called total) flow duration curve. Copy the discharge column, sort it largest to smallest, assign EP = rank / (count + 1), and plot Q against EP on both arithmetic and logarithmic y axes.

Report $Q_{50}$ and $Q_{95}$. In two or three sentences, describe what the shape of the curve says about the snowmelt-driven hydrology of the Spanish Fork, and explain why the 1% exceedance flow on this curve is NOT the same thing as the 100-year flood you estimated in Parts 1 through 3.

## Part 6 - Risk over a design life

A diversion structure on the Spanish Fork is designed to pass the 25-year peak discharge. Use your LP3 estimate from Part 3 as the design discharge (Bulletin 17C is the required method for this kind of design in the United States). The structure has a design life of 30 years.

a. What is the probability that the design discharge is exceeded at least once during the 30-year design life? This quantity is called the risk.<br>
b. What is the probability that it is never exceeded during the design life? This is the reliability.<br>
c. What is the probability that it is exceeded in the very first year of operation?<br>
d. What is the probability that it is exceeded exactly twice during the 30-year life? (Use the binomial distribution in Excel, `=BINOMDIST(2, 30, 1/25, FALSE)`.)<br>
e. The structure is left in service for an additional 20 years beyond its design life. What is the risk over the full 50 years?

$$\text{Risk} = 1 - \left(1 - \frac{1}{T}\right)^n \qquad \text{Reliability} = \left(1 - \frac{1}{T}\right)^n$$

State the assumption about successive years that both formulas require, and say in one sentence whether you believe it holds for this river.

## Part 7 - Designing to an accepted level of risk

A contractor must build a cofferdam to protect the Spanish Fork work site for the three years of construction. The owner will accept a 10% risk of the cofferdam being overtopped during that period. Use your LP3 results from Part 3 throughout this part.

a. Rearrange the risk equation to solve for the return period required. What T does a 10% risk over 3 years demand?<br>
b. Read the corresponding design discharge off your LP3 curve from Part 3, interpolating between the tabulated return periods. Report the cofferdam design discharge in cfs.<br>
c. Now suppose the owner wants that same 10% risk over a 50-year design life instead. What return period is required? Compare it with the length of the record (91 years), and state whether your LP3 analysis can support a design discharge at that return period.

$$T = \frac{1}{1 - (1 - \text{Risk})^{1/n}}$$

## Part 8 - What the numbers mean

a. A homeowner takes a 30-year mortgage on a house just outside the mapped 100-year floodplain. What is the probability of at least one 100-year flood during the life of that mortgage? Many people hear "100-year flood" and assume it is a once-in-a-lifetime event. Is that reading correct?<br>
b. Build a table of the return period required for risks of 5%, 10%, and 25% over design lives of 10, 25, and 50 years. Compare your table against Table 3-3 in the text.<br>
c. Look back at the LP3 confidence bounds you recorded in Part 3. At T = 475 you would be extrapolating roughly five times beyond the 91-year record. Given how the interval widens, how much confidence would you place in a design discharge at that return period, and what should a designer do about it? Two or three sentences.

## Submission

Upload your work to Learning Suite.

!!! note "Do not put your name or NetID in the file"
    Learning Suite records who submitted each file, so your name is not needed
    inside the file itself. This applies to scans and photos too — please
    don't write your name on the page.

## Grading Rubric

**Total: 24 points**

Each problem is scored 0-3: 0 nothing submitted, 1 an intelligent attempt, 2 complete with some errors, 3 correct within a reasonable tolerance.

| Criteria | Points |
|---|:---:|
| Part 1: Ranked peaks, Weibull plotting position, Q at six return periods | 3 |
| Part 2: Gumbel by method of moments | 3 |
| Part 3: Log-Pearson III via the USGS PeakFQ web tool, with confidence bounds and the pasted frequency curve | 3 |
| Part 4: Comparison table and semi-log plot of the three methods | 3 |
| Part 5: Annual flow duration curve, Q50 and Q95 | 3 |
| Part 6: Risk and reliability for a 25-yr design, 30-yr life | 3 |
| Part 7: Cofferdam - required T for an accepted risk | 3 |
| Part 8: Risk interpretation and the T-by-risk-and-life table | 3 |
