# 1.5 Precipitation and Climate Change

## Instructions

Determine the annual average total precipitation amount in Utah County.

1. Get precipitation gauge measurements from NOAA NCEI: [https://www.ncei.noaa.gov](https://www.ncei.noaa.gov){target='blank'}
    1. Go to "Access Data" and search for "Global Historical Climatology Network - Daily (GHCN-Daily), Version 3".
    2. Use the map to browse available stations. Find the Provo/Orem area which should have about 22 stations. Download at least these 4 stations:
        1. PROVO AIRPORT, UT US (USC00427061.csv)
        2. PROVO BYU, UT US (USC00427064.csv)
        3. OREM TREATMENT PLANT, UT US (USC00426538.csv)
        4. CASCADE MOUNTAIN, UT US (USS0011J70S.csv)
2. Get the annual cumulative rainfall in each year you have data by averaging the numbers from each station. Note that this is a large simplification.
3. Calculate the average annual rainfall based on the most recent 30 years of total annual precipitation.
4. Make a bar chart of each year's cumulative value. Add a dashed horizontal line at the average annual precipitation.
5. Determine if the annual precipitation total is changing over time. Fit a linear regression trend line to the graphs. Also use the data analysis add-in for Excel to do a regression analysis. Find the p-value and the 95% confidence interval. Label the regression line with the equation and the p-value from the regression analysis.

### Get climate change projections at the state/county level

1. Use the USGS National Climate Change Viewer (NCCV): [https://www.usgs.gov/tools/national-climate-change-viewer-nccv](https://www.usgs.gov/tools/national-climate-change-viewer-nccv){target='blank'}
2. Open CMIP6 - States.
3. Select the state, Utah, and the County, Utah.
4. Alternate through the variables for precipitation, runoff, and snow.
5. The controls for scenario and climatology period only affect the map layer and do not need to be modified.
6. Save the annual series figures for precipitation, runoff, and snow. On the graphs, include the lines for normal (1981-2020) and SSP370.

## Deliverable

1. A chart with:
    1. Bars of total precipitation in Utah County vs time.
    2. A dashed horizontal line at the 30-year average annual precipitation.
    3. A trendline, with the equation labeled/annotated on the chart.
2. Charts from the NCCV showing the current and projected amount of precipitation.
