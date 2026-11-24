# Homework - SCS Curve Number

## SCS Curve Number (CN) Method – Runoff Estimation and Comparison

### Objective

Apply the SCS Curve Number (CN) method to estimate direct runoff depth for design rainfall events under different land use and soil conditions, and evaluate how CN assumptions compare to other infiltration models.

### Background

The SCS CN method estimates direct runoff (Q) from total storm rainfall (P) using the relationship:

$$Q = \frac{(P - 0.2S)^2}{P + 0.8S}$$

where

- Q = direct runoff (inches)
- P = total storm rainfall (inches)
- S = potential maximum retention after runoff begins (inches), related to CN by

$$S = \frac{1000}{CN} - 10$$

When $P \le 0.2S$, $Q = 0$.

### Problem 1 – Urban vs. Agricultural Catchments

A small 25-acre watershed in Utah County receives a 3.5-inch storm.

The watershed includes:

- 60% urban residential area (¼-acre lots, fair condition, Soil Group C)
- 40% agricultural pasture (good condition, Soil Group B)

1. Determine the weighted CN for the watershed.
2. Compute the potential retention (S).
3. Calculate the direct runoff depth (Q) in inches using the SCS equation.
4. Estimate what fraction of rainfall became runoff (Q/P).

### Problem 2 – Sensitivity to Soil Group and Rainfall Depth

A 1 mi² watershed (640 acres) receives two different storms:

- Case A: P = 2.0 inches
- Case B: P = 6.0 inches

The watershed consists of open grassland (good condition) over Soil Group D.

1. Using the appropriate CN from the text, compute S and Q for each rainfall event.
2. Compare the runoff depths and comment on how storm size and infiltration capacity influence runoff generation.
3. If 25% of the watershed were converted to residential (1/8-acre lots, Soil Group D), recalculate a weighted CN and runoff for the 6-inch storm.

Hint: Clearly state all CN values you used and show calculations for S and Q for each case.

### Problem 3 – Conceptual Discussion (Short Answer)

Answer briefly (2–3 sentences each):

a) How does the SCS CN method differ conceptually from the Horton and Green–Ampt infiltration models?<br>
b) List two advantages and two limitations of the CN method for modern hydrologic design.<br>
c) Under what watershed or data conditions might you prefer to use the Green–Ampt method instead of SCS CN?

Excel template: [SCS Curve Number HW Template.xlsx](SCS%20Curve%20Number%20HW%20Template.xlsx)

## Submission

Upload your work to the matching assignment in Canvas.

!!! note "Do not put your name or NetID in the file"
    Canvas records who submitted each file, so your name is not needed
    inside the file itself. This applies to scans and photos too — please
    don't write your name on the page.

## Grading Rubric

**Total: 9 points**

Each problem is scored 0-3: 0 nothing submitted, 1 an intelligent attempt, 2 complete with some errors, 3 correct within a reasonable tolerance.

| Criteria | Points |
|---|:---:|
| Problem 1: Weighted CN, S, Ia, runoff depth and ratio | 3 |
| Problem 2: Runoff at two storm depths, non-linearity, added land use | 3 |
| Problem 3: CN vs Horton vs Green-Ampt; advantages and limitations | 3 |
