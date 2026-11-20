# In-Class - Evapotranspiration

These examples are the same type of problem as Homework Parts 1, 2 and 3: same equations, similar setup, different numbers.

Excel starter file: [Evapotranspiration Example Template.xlsx](Evapotranspiration%20Example%20Template.xlsx)

Handouts: [Seasonal Consumptive Use K values](Seasonal_Consumptive%20Use%20K%20values.pdf), [Blaney-Criddle P](BlaneyCriddle%20P.pdf)

# Example A - Blaney-Criddle for Alfalfa, May-July at 40°N

Compute monthly and seasonal Blaney-Criddle ET for irrigated alfalfa at 40 °N (Utah Valley) for May, June, and July using the equations:

$$ET_c = p\,(0.46\,T + 8) \quad \text{(mm/month, with } p \text{ as monthly \% daylight hours)}$$

$$ET = K_c \cdot ET_c$$

| Month | Mean T (°C) | $p_{daily}$ (40 °N) | Days | $K_c$ (alfalfa) |
|---|:---:|:---:|:---:|:---:|
| May | 15 | 0.32 | 31 | 0.85 |
| June | 20 | 0.34 | 30 | 0.90 |
| July | 25 | 0.33 | 31 | 0.90 |

**Find**

a. Monthly $ET_c$ and ET (mm and in)<br>
b. 3-month seasonal ET total

# Example B - Retrieving and Comparing OpenET Data

Using the Blaney-Criddle estimate for alfalfa in Utah Valley from Example A, retrieve a satellite-based ET estimate for the same field and time period from OpenET, and compare. Walk through the workflow at [explore.etdata.org](https://explore.etdata.org) and produce a side-by-side comparison table.

**Given**

- OpenET: explore.etdata.org
- Field: alfalfa polygon in Utah Valley
- Period: May-July 2024
- Variable: monthly ET (mm or in)

**Find**

a. Steps to retrieve OpenET data<br>
b. Side-by-side Blaney-Criddle vs. OpenET comparison table

# Example C - Why Might Blaney-Criddle and OpenET Differ?

Suppose the Blaney-Criddle estimate and the OpenET ensemble agree well in mid-summer but diverge in May (Blaney-Criddle higher than OpenET) and again in September (Blaney-Criddle lower than OpenET). Propose physical reasons for the seasonal pattern of disagreement and discuss when each method is the better choice for an engineer.

**Find**

a. Physical reason for the May gap<br>
b. Physical reason for the September gap<br>
c. When to prefer each method
