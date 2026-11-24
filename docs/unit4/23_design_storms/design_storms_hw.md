# Homework - Design Storms

This homework has two parts: the Provo Urban Hydrology assignment below, and two textbook problems.

## Provo Urban Hydrology

### Part 1 - Time of Concentration

A 28-acre residential watershed drains to a storm inlet near 900 E in Provo.

| Segment | Type | Length (ft) | Slope |
|---|---|---|---|
| A–B | Sheet flow (lawn) | 100 | 0.020 |
| B–C | Shallow concentrated | 500 | 0.012 |
| C–D | Street gutter | 800 | 0.009 |

1. Compute travel time for each segment using TR-55 equations.
2. Compute total time of concentration.
3. Briefly explain which segment controls Tc and why.

NOTE: For the street gutter segment C-D you can use the fact that the hydraulic radius in Manning's equation is approximately equal to one half the depth, or d/2. In a typical street gutter that depth is on the order of 0.2 in, so use r = 0.1 inches. In an actual problem the calculation of t<sub>c</sub> is iterative, because you must know the flow before you know r.

To find P₂ (the 2-year, 24-hour rainfall depth) from NOAA Atlas 14:

1. Go to <https://hdsc.nws.noaa.gov/pfds/pfds_map_cont.html?bkmrk=ut>
2. Put your cursor on Provo.
3. Look down at where the 24-hr and 2-year values match up and find the precipitation depth.

### Part 2 - Using the IDF Curves

Using your computed t<sub>c</sub>:

1. Identify the rainfall duration to use for peak-flow design.
2. Using NOAA Atlas 14, obtain the 10- and 100-year design rainfall intensities.
3. Using the Rational Method, determine the design Q<sub>p</sub>.

### Part 3 - Think About It

These won't be graded, but should be something you understand.

1. Why is using t<sub>c</sub> as the duration on an IDF curve the right choice for design intensity?
2. What error would you be making if a duration longer than t<sub>c</sub> were used?
3. Why does storm temporal distribution matter more in urban basins than rural basins?

## Textbook Problems

Solve the following problems from Bedient, Huber & Vieux, *Hydrology and Floodplain Analysis*, 6th ed.

- **6.4**
- **6.6**

In the template these are on the sheets named "Problem 4.4" and "Problem 4.6".

Excel template: [Design Storms HW Template.xlsx](Design%20Storms%20HW%20Template.xlsx)

## Submission

Upload your work to the matching assignment in Canvas.

!!! note "Do not put your name or NetID in the file"
    Canvas records who submitted each file, so your name is not needed
    inside the file itself. This applies to scans and photos too — please
    don't write your name on the page.

## Grading Rubric

**Total: 12 points**

Each problem is scored 0-3: 0 nothing submitted, 1 an intelligent attempt, 2 complete with some errors, 3 correct within a reasonable tolerance.

| Criteria                                                        | Points |
|-----------------------------------------------------------------|:------:|
| Part 1: Travel time by segment, total Tc, controlling segment    |   3    |
| Part 2: Design duration and Rational Method peaks at two return periods |   3    |
| Problem 6.4: Number of events for MIT = 0-5 hr; MIT for one event |   3    |
| Problem 6.6: 25-yr, 24-hr SCS Type II storm for Houston, hourly hyetograph |   3    |

Part 3 is not graded.
