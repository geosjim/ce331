# In-Class - Wells

These examples are the same type of problem as Homework Problems 8.4, 8.5 (a and b) and 8.6: same equations, similar setup, different numbers.

Excel starter file: [Wells Example Template.xlsx](Wells%20Example%20Template.xlsx)

# Example A - Unconfined Well Discharge

A fully penetrating pumping well is completed in an unconfined sand aquifer. After steady state is reached, drawdowns are measured at two observation wells at different radial distances from the pumping well. You are asked to compute the well's steady-state discharge.

**Given**

- Well diameter = 12 in, so rw = 0.5 ft
- Saturated aquifer thickness b = 80 ft
- Observation well 1: r₁ = 75 ft, drawdown s₁ = 18 ft, so h₁ = 62 ft
- Observation well 2: r₂ = 250 ft, drawdown s₂ = 16 ft, so h₂ = 64 ft
- K = 1000 gpd/ft²

**Find**

Steady-state pumping rate Q (gpm), using the unconfined (Dupuit) well equation (Equation 8-42):

$$Q = \frac{\pi K (h_2^2 - h_1^2)}{\ln(r_2/r_1)}$$

Watch units: convert K from gpd/ft² to ft/day (divide by 7.48).

# Example B - Dupuit Parabola

Two piezometers penetrate a homogeneous unconfined aquifer that sits on a horizontal impermeable base. Under steady flow between two adjacent water bodies, the water table follows the Dupuit parabola.

**Given**

- Aquifer thickness (to base) = 350 ft
- Piezometer spacing L = 1200 ft
- Depth to water table: 30 ft (shallower piezometer), 60 ft (deeper piezometer)
- h₀ = 350 − 30 = 320 ft (upgradient)
- h_L = 350 − 60 = 290 ft (downgradient)
- K = 4 × 10⁻⁴ ft/s

**Find**

a. Height of the water table at the midpoint (x = 600 ft) using the Dupuit parabola:

$$h^2(x) = h_0^2 - \frac{x}{L}\left(h_0^2 - h_L^2\right)$$

b. Flow rate per unit width q using the Dupuit equation:

$$q = \frac{K \left(h_0^2 - h_L^2\right)}{2L}$$

# Example C - Drawdown at the Well

Rearrange Equation 8-42 to solve for h_w.

**Given**

- Q = 30 gpm ≈ 5,776 ft³/day
- Unconfined aquifer, thickness b = 120 ft
- K = 25 ft/day
- At r₁ = 150 ft: drawdown s₁ = 25 ft, so h₁ = 95 ft
- Well radius rw = 0.75 ft

**Find**

Drawdown at the well (r = rw), using

$$h_w^2 = h_1^2 - \frac{Q \ln(r_1/r_w)}{\pi K}, \qquad s_w = b - h_w$$
