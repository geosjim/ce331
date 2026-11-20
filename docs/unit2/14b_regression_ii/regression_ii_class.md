# In-Class - Regression II

# Example 1 - Multivariable Regression for Provo Canyon

The worked example spreadsheet pairs monthly gauged discharge for the Provo River in Provo Canyon with GLDAS land-surface model output for the same months (120 months). The GLDAS fields are:

- Average surface temperature (K)
- Air temperature at 2 m (K)
- Root zone soil moisture (kg m⁻²)
- Wind speed (m s⁻¹)
- Evapotranspiration (kg m⁻² s⁻¹)
- Plant canopy surface water (kg m⁻²)
- Snow depth (m)
- Snow depth water equivalent (kg m⁻²)
- Specific humidity (kg kg⁻¹)
- Total precipitation rate (kg m⁻² s⁻¹)

Fit a multivariable ordinary least-squares model

$$Q = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_k x_k$$

of average discharge on the GLDAS variables using Excel's `LINEST` (or the Data Analysis Regression tool), compute the predicted discharge for each month, and plot gauged and predicted discharge against time. A correlation matrix of the predictors helps decide which terms are redundant.

Worked example: [ProvoWorkedExample.xlsx](ProvoWorkedExample.xlsx)

Refresher: [How to do multiple regression analysis in Excel](https://www.exceldemy.com/how-to-do-multiple-regression-analysis-in-excel/)

The homework repeats this for Spanish Fork Canyon.
