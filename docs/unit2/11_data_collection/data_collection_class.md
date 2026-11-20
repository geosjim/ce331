# In-Class - Data Collection

Handout: [CSVImportandPivotTables.pdf](CSVImportandPivotTables.pdf)

# Example 1 - Importing Downloaded Data and Building a PivotTable

Downloaded datasets often do not come in a format that is ready for a PivotTable. The handout walks through cleaning a daily discharge file with Text-to-Columns and then using a PivotTable to extract the annual peaks.

**Cleaning a downloaded file**

1. Open the exported csv file in a new Excel worksheet.
2. Delete extraneous metadata rows and columns so that you are left with just the date and discharge value.
3. Copy and paste the discharge values at least 5 columns from the date column (Column F).
4. Select the date column (Column A), then Data > Text-to-Columns.
5. Step 1 of 3: select "Delimited". Step 2 of 3: as a delimiter select "Space" and put "/" in the "Other" box; check the Data Preview. Step 3 of 3: Next.
6. Change the formatting of Column A to "Number".
7. Copy the discharge values to the column next to the year (Column D).
8. Insert a row at the top and add headings for Month, Day, Year, Q (Discharge).
9. Save the file. It is now ready for a PivotTable.

**Annual peaks with a PivotTable**

1. Select all rows and columns.
2. Insert > PivotTable, in a new worksheet.
3. Put Year in the Rows box and Q in the Values box.
4. Change the Values calculation from Sum (the default) to Max.
5. Copy and paste the annual maximums to another sheet for further analysis.

# Example 2 - Finding and Downloading a Precipitation Record

This is how the Spanish Fork monthly precipitation record used later in the course was obtained, and how to repeat it for any other station or period.

| Item | Value |
|---|---|
| Station name | Spanish Fork Power House, Utah |
| GHCN station ID | USC00428119 |
| Network | GHCN-Daily / Global Summary of the Month |
| Element code | PRCP (precipitation total) |

**Route 1 - Climate Data Online (point and click).** Use this route when you do not yet know which station you want.

1. Go to NOAA NCEI Climate Data Online: [https://www.ncei.noaa.gov/cdo-web/](https://www.ncei.noaa.gov/cdo-web/)
2. Choose "Search Tool." Set Select a Dataset to "Monthly Summaries," set the date range, and set Search For to "Stations."
3. Enter a place name (Spanish Fork, UT) or a county, then Search.
4. Click a station name on the results map to see its period of record and elements. Confirm that the record covers your date range and that PRCP is listed.
5. Add to Cart, choose Custom GHCN-Daily CSV (or Custom Monthly Summaries CSV), set the date range, and check Precipitation.
6. Enter your email and submit. NCEI emails a download link, usually within a few minutes.

**Route 2 - Direct data service URL.** Once you know the station ID, paste a URL like this into a browser:

```
https://www.ncei.noaa.gov/access/services/data/v1?dataset=global-summary-of-the-month&stations=USC00428119&startDate=2016-01-01&endDate=2025-12-31&dataTypes=PRCP&format=csv&units=standard
```

- `stations` - the GHCN ID; several can be comma separated.
- `startDate` / `endDate` - ISO format, YYYY-MM-DD.
- `dataTypes` - PRCP for precipitation, TMAX and TMIN for temperature.
- `dataset` - global-summary-of-the-month for monthly totals; daily-summaries for daily values.
- `units` - standard gives inches and degrees F; metric gives millimeters and degrees C.
- `format` - csv downloads a file; json displays in the browser.

**Check the record before you use it.** Monthly summaries are published even when the daily record is incomplete, and a missing month shows up as a missing row, not as a blank or a flag.

- Count the rows. Ten years of monthly data means 120 rows; fewer means a month is missing, not zero.
- Sort by date and scan for skipped months.
- Distinguish a missing month from a genuinely dry one: a reported 0.00 in. is a real measurement; a missing month has no row at all.
- Do not interpolate a missing monthly precipitation total. Shift the window or carry the reduced n through the analysis.

**Getting it into Excel.** Open the CSV, or use Data > From Text/CSV so you can set the date column type explicitly. Keep a second sheet recording the station name, station ID, element, period, source, and the date you retrieved it.

**Other sources worth knowing**

- USGS National Water Information System ([waterdata.usgs.gov](https://waterdata.usgs.gov/)) - streamflow, including the instantaneous annual peak series.
- NRCS SNOTEL ([nwcc-apps.sc.egov.usda.gov](https://nwcc-apps.sc.egov.usda.gov/)) - snow water equivalent and precipitation at high elevation.
- Utah Climate Center ([climate.usu.edu](https://climate.usu.edu/)) - a state-level interface to the same GHCN stations.
- PRISM ([prism.oregonstate.edu](https://prism.oregonstate.edu/)) - gridded precipitation for basin averages.
