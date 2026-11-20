# Pre-Class - Regression II

This lesson continues regression and watershed classification: building a simple linear model from real Spanish Fork data and judging whether it is useful, using USGS StreamStats to apply regional regression equations to a basin, and extending ordinary least squares to multivariable regression with several predictors and transformed terms.

## Reading

Review Bedient, Huber & Vieux, *Hydrology and Floodplain Analysis*, 6th ed., Sections 3.7 (Regional Analysis) and 3.8 (Related Topics).

## Slides

[Presentation - Multivariable Regression](statistical-hydrology-multivariable-regression.pdf)

## Other Resources

- [How to do multiple regression analysis in Excel](https://www.exceldemy.com/how-to-do-multiple-regression-analysis-in-excel/) (refresher tutorial)
- [USGS StreamStats](https://streamstats.usgs.gov/ss/)

## Pre-Class Assignment

This one is a working assignment rather than a set of reading questions, so plan on 45-60 minutes. Part 1 uses two data files (linked below); Part 2 uses USGS StreamStats in your browser. Enter your answers in the Learning Suite quiz before class. I am still grading evidence that you did the work and thought about it rather than perfect numbers, but both parts produce numbers, so report the ones you get. Bring your plot and your StreamStats report to class - we will use several of them as the starting point for the in-class examples.

### Part 1 - Build a Simple Linear Model for Spanish Fork

Data files:

- [Spanish_Fork_monthly-precipitation.xlsx](Spanish_Fork_monthly-precipitation.xlsx) - monthly precipitation totals, January 2016 through December 2025, from the Spanish Fork Power House GHCN station (USC00428119).
- [Spanish_Fork_daily-data-mean.xlsx](Spanish_Fork_daily-data-mean.xlsx) - daily mean discharge for Spanish Fork at Castilla (USGS 10150500), the same gage we used for flow frequency in Lesson 13.

What to do:

1. Reduce the daily discharge record to one mean discharge value for each month from January 2016 through December 2025. A PivotTable will help.
2. Pair each monthly precipitation total P (in) with the mean discharge Q (cfs) for that same month. You should end up with 120 pairs.
3. Fit Q = a + b*P by ordinary least squares and report a, b, R^2, and n. Use the same normal-equation formulas from the first regression class, or Excel's SLOPE, INTERCEPT, and RSQ.
4. Make a scatter plot of Q against P with the fitted line drawn on it.

### Question 1.1 - Your Fitted Equation

Report your fitted equation Q = a + b*P, your R^2, and the number of monthly pairs n you used.

### Question 1.2 - The Sign of the Slope

What is the sign of your slope, and does it match what you expected before you ran the numbers? In one or two sentences, explain what is physically going on in this basin.

### Question 1.3 - Would You Use It?

Would you use this equation to forecast next June's mean discharge? Why or why not? If not, what would you change about the way the predictor is defined?

### Part 2 - Regional Regression for a Basin Near Home

What to do:

1. Open USGS StreamStats at [https://streamstats.usgs.gov/ss/](https://streamstats.usgs.gov/ss/) and zoom to your hometown. If your hometown is outside the United States, or in an area StreamStats does not cover, pick a basin near campus or near somewhere you have lived.
2. Select the state, click a point on a stream, and delineate the basin upstream of that point.
3. Run the basin characteristics report, then run the Peak-Flow Statistics (flood frequency) report.
4. Save or screenshot the report. You will need both the flow values and the list of basin characteristics the equations used.

### Question 2.1 - Your Basin

Identify the basin you delineated: stream name, state, and roughly where the outlet is. Report the drainage area StreamStats computed and the regression region or study it assigned you to.

### Question 2.2 - AEP Flows

Report the peak discharge for the 1, 2, 4, 10, 20, and 50 percent annual exceedance probabilities, and state the return period that goes with each one.

### Question 2.3 - Which Basin Characteristics, and Why

List the basin characteristics that appear in the regression equations StreamStats used for your site. For each one, write a sentence on why you think it is in the equation.

### Question 2.4 - What Is Missing

Name at least two characteristics you expected to see in the equations and did not. Why do you think they were left out?

Bring your scatter plot from Part 1 and your StreamStats peak-flow report from Part 2 to class. We will put a few of them on the screen and work from them.

Answer in Learning Suite (assignment "Pre Class: Regression II") by 8:00 am on the day of class. Write your own answer first. If you then use AI to critique or expand your answer, add that after your own answer and disclose it, as described in the course AI policy.
