# Part 4 - Climate Variables and Climate Change Projections

## Introduction

The purpose of this lab is to obtain historical climate variable measurements from NOAA and climate projections from CMIP6.

## Instructions

1. Determine the annual average total precipitation amount in Utah.
    1. Get precipitation gauge measurements from NOAA NCEI: [https://www.ncei.noaa.gov](https://www.ncei.noaa.gov){target='blank'}
        1. Go to "Access Data" and search for "Global Historical Climatology Network - Daily (GHCN-Daily), Version 3".
        2. Use the map to browse available stations. Find the Provo/Orem area which should have about 22 stations. Download these stations:
            - PROVO AIRPORT, UT US (USC00427061.csv)
            - PROVO BYU, UT US (USC00427064.csv)
            - OREM TREATMENT PLANT, UT US (USC00426538.csv)
            - CASCADE MOUNTAIN, UT US (USS0011J70S.csv)
    2. Get the annual cumulative rainfall in each year you have data.
    3. Make a bar chart of each year's cumulative value. Add a horizontal dashed line at the average of the most recent 30 years. Label this line with the average precipitation depth.
    4. Fit a linear regression trend line to the graphs. Also use the Data Analysis add-in for Excel to do a regression analysis. Find the p-value and the 95% confidence interval. Label the regression line with the equation and the p-value from the regression analysis.
2. Repeat #1 for air temperature.
3. Get climate change projections at the state/county level.
    1. [https://www.usgs.gov/tools/national-climate-change-viewer-nccv](https://www.usgs.gov/tools/national-climate-change-viewer-nccv){target='blank'}
    2. Open CMIP6 – States.
    3. Select the state, Utah, and the County, Utah.
    4. Alternate through the variables for precipitation, runoff, and snow.
    5. The controls for scenario and climatology period only affect the map layer and do not need to be modified.

## Deliverables

1. Bar chart of historical annual total precipitation in Provo/Orem according to NOAA gauges.
2. Bar chart of historical annual average air temperature in Provo/Orem according to NOAA gauges.
3. Figures from USGS NCCV
    1. Annual series for Precipitation, Runoff, and Snow. On the graphs, include the lines for normal (1981-2020) and SSP370. 3 total figures.
4. Provide 2 paragraphs explaining the figures you generated in response to these prompts:
    1. What is the normal amount of precipitation in a year in Utah? Based on the data from your gauges, is there evidence that it is changing over time? Comment on the statistical and practical significance as appropriate.
    2. What changes in patterns of precipitation should Utah County expect? Will there be more or less rain and snow? Will the proportion of rain and snow change? Do we expect a change in the timing of the precipitation? Comment on how the changes could affect other hydrological variables; namely, peak flow, and the loss variables infiltration and evaporation.
