# Part 2 - Rivers and Watersheds

## Introduction

The purpose of this assignment is to collect and analyze information about rivers in Utah County using StreamStats and USGS gauge data.

## Data Files

If you have trouble downloading from StreamStats or NWIS, you can use these copies.

| File | Description |
|:-----|:------------|
| [provocanyon.geojson](provocanyon.geojson) | StreamStats basin boundary, Provo Canyon |
| [hobblecreekcanyon.geojson](hobblecreekcanyon.geojson) | StreamStats basin boundary, Hobble Creek Canyon |
| [spanishforkcanyon.geojson](spanishforkcanyon.geojson) | StreamStats basin boundary, Spanish Fork Canyon |
| [paysoncanyon.geojson](paysoncanyon.geojson) | StreamStats basin boundary, Payson Canyon |
| [santaquincanyon.geojson](santaquincanyon.geojson) | StreamStats basin boundary, Santaquin Canyon |
| [spanishfork.usgs.10150500.txt](spanishfork.usgs.10150500.txt) | USGS NWIS daily mean discharge (cfs) at gauge 10150500, 1980 to present (tab-delimited) |

## Instructions

1. Delineate the watersheds of the canyons in Utah County; namely Provo, Hobble Creek, Spanish Fork, Payson, and Santaquin canyons. Choose a spot to delineate near the mouth of the canyons. The specific locations are not critical. Download the basin boundaries as GeoJSON.
2. Prepare one map of all the basin boundaries in ArcGIS/QGIS. Adjust colors and styles so the basins are distinguishable from each other.
3. Delineate other spots in Utah County at the inlets and outlet of Utah Lake to explore basin boundaries and the locations and flow directions of the rivers.
4. Redelineate Spanish Fork Canyon. This time, generate a report. Check all the boxes under "Regression Based Scenarios" and all the boxes under "Basin Characteristics." Read the report. Find the basin characteristics about developed and impervious area and other land use descriptions.
5. Get gauge discharge from the USGS gauge 10150500 near the outlet of the Spanish Fork Canyon. Data is available since 1919! To keep your analysis simpler and make plots readable, you may use daily average discharge since 1980-01-01. [https://waterdata.usgs.gov/nwis](https://waterdata.usgs.gov/nwis){target='blank'}
    1. Plot the hydrograph of Spanish Fork Canyon.
    2. Calculate the annual average discharge.
    3. Calculate the average discharge for each month.
    4. Compare these numbers to the StreamStats numbers. It is normal and expected for these to be different.

## Deliverables

1. A map of the canyon basin boundaries.
2. The hydrograph of Spanish Fork Canyon at the USGS gauge.
3. A table of the annual and monthly average flows.
4. The StreamStats report for Spanish Fork Canyon.
