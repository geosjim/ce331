# Homework - Regression II

**Spanish Fork River at Castilla, Utah (USGS 10150500)** - GLDAS land-surface model output vs. gauged discharge. GLDAS-2.1 monthly fields, area-weighted over the five 0.25-degree cells covering 94% of the 631 mi² basin.

Excel template: [Spanish Fork MultiVariable Regression - Template.xlsx](Spanish%20Fork%20MultiVariable%20Regression%20-%20Template.xlsx)

## The Problem

Using as many of the other provided columns as you find helpful, create the best regression equation you can using the GLDAS modeled values and transformations (log, exponential, polynomial terms, etc.). Provide a plot with the gauge discharge and your equation's predicted discharge during the 10 years.

## What to Turn In

Report your results on the Problem Statement sheet of the template.

1. Your final regression equation, written out with its coefficients and the units of the response.
2. The list of terms you dropped and the conceptual or mathematical reasons why you did.
3. R-squared and adjusted R-squared for your final model, and the number of months you fit it on.
4. A plot with time on the x axis and two series: gauge discharge and your predicted discharge.
5. Two or three sentences on where your model does well and where it does not.

See the [In-Class](regression_ii_class.md) Provo Canyon worked example for the approach.

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
| Final regression equation with coefficients and units, and the dropped terms with reasons (items 1-2) | 3 |
| R-squared, adjusted R-squared, and number of months fit (item 3) | 3 |
| Time-series plot of gauge vs. predicted discharge, with comments on where the model does well and poorly (items 4-5) | 3 |
