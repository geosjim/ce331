# Part 3 - Reservoirs and Lakes

## Introduction

There are 3 major reservoirs in Utah County: Jordanelle Reservoir, Deer Creek Reservoir, and Utah Lake. The US Bureau of Reclamation is the federal level agency ultimately responsible for these 3 water sources. You can obtain measurements about them from a USBR website such as:

- [https://www.usbr.gov/rsvrWater/HistoricalApp.html](https://www.usbr.gov/rsvrWater/HistoricalApp.html){target='blank'}
- [https://www.usbr.gov/uc/water/hydrodata/reservoir_data/site_map.html](https://www.usbr.gov/uc/water/hydrodata/reservoir_data/site_map.html){target='blank'}

## Data Files

| File | Description |
|:-----|:------------|
| [DEERCREEKRESERVOIR12-18-2025T16.05.36.csv](DEERCREEKRESERVOIR12-18-2025T16.05.36.csv) | USBR daily measurements for Deer Creek Reservoir (all available records) |

## Instructions

1. Download daily data for Deer Creek Reservoir for all the available measurements.
2. For each of the variables 1) inflow, 2) outflow, and 3) evaporation, do the following steps using Excel pivot tables or in code.
    1. Find the average value for each day of the year. That is, average all measurements that occur on January 1, regardless of year. Repeat for each day of the year.
    2. Hint for Excel: to make this work with pivot tables, you should make a helper column with labels for month-day combination using the function `=CONCAT(TEXT(MONTH(dateCell), "00"), "-", TEXT(DAY(dateCell), "00"))`.
3. Find the net captured volume vs day of the year. Use the simplified mass balance equation: Volume = Inflow - Evaporation - Outflow.
4. Make a line plot with the average day of year inflow, outflow, evaporation, and net captured. Keep all units in cfs. You will need to convert acre-feet to equivalent daily average cfs.
5. Identify the year with the maximum, minimum, and median cumulative value for evaporation, inflow, and outflow. Use a pivot table to find a cumulative value based on the year. You probably want to add a helper column which is the year of the measurement using `=YEAR()`. Report these values in a table. Include row and column labels. The table should be 4x4 in shape.
6. Evaluate Hobble Creek Canyon as a location for a new reservoir.
    1. Use StreamStats to estimate the annual average discharge from the canyon. Assume this is the inflow volume to the hypothetical reservoir.
    2. Assume you discharge half of the inflow.
    3. Approximately how much water is captured each year?
    4. Use the Deer Creek Reservoir data to estimate the percent of cumulative annual inflow lost to evaporation. Assume this is the same on your reservoir.
    5. After subtracting losses, how much net water is saved for use in a year?
    6. Assume this water is used exclusively by residents of Springville. What is the equivalent gallons per capita per day of this volume?

## Deliverables

1. 1 plot of inflow, outflow, evaporation, and net captured flow on each day of the year.
2. Table with the min, max, and median cumulative values for inflow, outflow, evaporation.
3. 1 page of hand calculations with rough estimates evaluating Hobble Creek as a reservoir location.
