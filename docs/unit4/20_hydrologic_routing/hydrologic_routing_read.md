# Pre-Class - Hydrologic Routing

Routing describes how a flood wave changes shape as it moves down a river reach. This lesson contrasts hydrologic routing (continuity plus a storage relation) with hydraulic routing (continuity plus momentum), explains why reach storage depends on both inflow and outflow, and introduces the Muskingum method: the storage equation with parameters K and x, the routing coefficients C₀, C₁, and C₂, and the translation and attenuation of a routed hydrograph.

## Reading

Bedient, Huber & Vieux, *Hydrology and Floodplain Analysis*, 6th ed., Sections 4.1 (Hydrologic and Hydraulic Routing) and 4.2 (Hydrologic River Routing).

## Slides

[Presentation - Hydrologic River Routing](Presentation21%20-%20Hydrologic%20River%20Routing.pdf)

## Pre-Class Questions

### Question 1 - Hydrologic vs. Hydraulic Routing

In one or two sentences, distinguish between hydrologic routing and hydraulic routing. What physical principle does each method rely on, and which one is computationally simpler?

### Question 2 - Continuity, Storage, and the Loop Rating Curve

Why does the storage–outflow relationship for a river reach plot as a loop rather than a single line, and what physical concept does the loop reveal?

### Question 3 - Muskingum Storage Equation and Parameters K and x

Write the Muskingum storage equation and describe the physical meaning of the parameters K and x. What is the typical range of x for natural channels, and what do the limiting values x = 0 and x = 0.5 represent?

### Question 4 - The Muskingum Routing Equation

Starting from S = K[xI + (1−x)Q] and the finite-difference continuity equation, the textbook derives Q₂ = C₀ I₂ + C₁ I₁ + C₂ Q₁. Write the formulas for C₀, C₁, and C₂, and explain what numerical check confirms that the coefficients were computed correctly.

### Question 5 - Translation and Attenuation in a Routed Hydrograph

When a flood wave passes through a river reach modeled with the Muskingum method, two characteristic changes occur in the hydrograph between the upstream and downstream ends. Name these two effects and explain which parameter primarily controls each.

Answer these questions in Learning Suite (assignment "Pre Class: Hydrologic Routing") by 8:00 am on the day of class. Write your own answer first. If you then use AI to critique or expand your answer, disclose it, as described in the course AI policy.
