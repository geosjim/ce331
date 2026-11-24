# 1.3 Reservoirs and Lakes

## Introduction

There are 3 major reservoirs in Utah County: Jordanelle Reservoir, Deer Creek Reservoir, and Utah Lake. The US Bureau of Reclamation is the federal level agency ultimately responsible for these 3 water sources. You can obtain measurements about them from a USBR website such as:

- [https://www.usbr.gov/rsvrWater/HistoricalApp.html](https://www.usbr.gov/rsvrWater/HistoricalApp.html){target='blank'}
- [https://www.usbr.gov/uc/water/hydrodata/reservoir_data/site_map.html](https://www.usbr.gov/uc/water/hydrodata/reservoir_data/site_map.html){target='blank'}

## Instructions

1. Download daily data for Deer Creek Reservoir and Utah Lake for all the available measurements.
2. For each of the variables 1) inflow, 2) outflow, and 3) evaporation, do the following steps using Excel pivot tables or in code.
    1. Find the average value for each day of the year. That is, average all measurements that occur on January 1, regardless of year. Repeat for each day of the year.
    2. Hint for Excel: to make this work with pivot tables, you should make a helper column with labels for month-day combination using the function `=CONCAT(TEXT(MONTH(dateCell), "00"), "-", TEXT(DAY(dateCell), "00"))`.
3. Find the net captured volume vs day of the year. Use the simplified mass balance equation $Volume = Inflow - Evaporation - Outflow$.
4. For each reservoir, make a line plot with the average day of year inflow, outflow, evaporation, and net captured. Keep all units in cfs. You will need to convert acre-feet to equivalent daily average cfs.

## Deliverable

1. 2 plots, 1 per reservoir, showing the day of year average inflow, outflow, and evaporation loss lines.
