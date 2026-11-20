# In-Class - Regression

Simple linear regression by hand, then USGS regional regression. These examples use the same equations as the homework, with different numbers.

Excel starter file: [Regression Example Template.xlsx](Regression%20Example%20Template.xlsx)

# Example A - Simple Linear Regression

A regional team has six gaged basins in a homogeneous physiographic region and wants a simple equation to estimate mean annual discharge Q (cfs) from drainage area A (mi²) at any ungaged basin in the same region.

| Basin | A (mi²) | Q (cfs) |
|---|---|---|
| 1 | 1 | 12 |
| 2 | 2 | 18 |
| 3 | 3 | 26 |
| 4 | 5 | 38 |
| 5 | 6 | 45 |
| 6 | 9 | 60 |

Fit $Q = a + bA$ by ordinary least squares using the normal-equation formulas, report $R^2$, and use the equation to predict Q for a new basin with A = 4 mi².

$$b = \frac{n\sum AQ - \sum A \sum Q}{n\sum A^2 - \left(\sum A\right)^2}, \qquad a = \bar{Q} - b\bar{A}, \qquad R^2 = 1 - \frac{SS_{res}}{SS_{tot}}$$

**Find:**

- Slope b and intercept a of $Q = a + bA$
- Coefficient of determination $R^2$
- Predicted Q at A = 4 mi²
- A one-sentence interpretation of the slope

# Example B - Regional Regression at an Ungaged Urban Basin

A small, partly urbanized basin in the Tallahassee region needs 10-, 25-, and 100-yr peak discharge estimates for a culvert design. There is no streamgage on the basin.

Apply the USGS regional power equation (textbook Eq. 3-82)

$$Q_T = C_p\, A^{a}\, IA^{b}$$

with these coefficients:

| T (yr) | $C_p$ | a | b |
|---|---|---|---|
| 10 | 39.1 | 0.776 | 0.867 |
| 25 | 63.2 | 0.787 | 0.791 |
| 100 | 118.0 | 0.808 | 0.687 |

**Given:** A = 2.5 mi²; IA = 20% impervious; region: Tallahassee (Eq. 3-82 valid).

**Find:** $Q_{10}$, $Q_{25}$, and $Q_{100}$ (cfs).
