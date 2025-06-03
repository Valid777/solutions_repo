# Problem 1: Measuring Earth's Gravitational Acceleration with a Pendulum

## Motivation
The acceleration due to gravity, denoted \( g \), is a fundamental constant influencing many physical phenomena. Accurate measurement of \( g \) is crucial for understanding gravitational interactions, structural design, and experiments in various scientific fields.

One classical approach to determine \( g \) is through the oscillations of a simple pendulum, where the period depends on the local gravitational field strength.

## Task
Measure the acceleration due to gravity \( g \) using a pendulum and perform a detailed uncertainty analysis of your measurements.

This exercise highlights rigorous measurement techniques, uncertainty quantification, and their significance in experimental physics.

## Procedure

### 1. Materials
- A string (approximately 1 or 1.5 meters long)
- A small weight (e.g., bag of coins, sugar bag, keychain) attached to the string
- Stopwatch or smartphone timer
- Ruler or measuring tape

### 2. Setup
- Attach the weight to one end of the string and fix the other end to a stable support.
- Measure the pendulum length \( L \) from the suspension point to the center of the weight using the ruler or measuring tape.
- Record the resolution of the measuring tool. Calculate the length measurement uncertainty as half of the resolution:
  
  $$
  \Delta L = \frac{\text{resolution}}{2}
  $$

### 3. Data Collection
- Displace the pendulum by a small angle (< 15°) and release it.
- Measure the time for 10 full oscillations \( T_{10} \) and repeat this 10 times, recording all measurements.
- Calculate the mean time for 10 oscillations \( \overline{T}_{10} \) and the standard deviation \( s_{T_{10}} \).
- Determine the uncertainty in the mean time as:
  
  $$
  \Delta \overline{T}_{10} = \frac{s_{T_{10}}}{\sqrt{10}}
  $$

## Calculations

### 1. Calculate the period \( T \) of one oscillation:
  
  $$
  T = \frac{\overline{T}_{10}}{10}
  $$
  
  $$
  \Delta T = \frac{\Delta \overline{T}_{10}}{10}
  $$

### 2. Determine gravitational acceleration \( g \):
  
  $$
  g = \frac{4 \pi^2 L}{T^2}
  $$

### 3. Propagate uncertainties for \( g \):
  
  $$
  \frac{\Delta g}{g} = \sqrt{\left(\frac{\Delta L}{L}\right)^2 + \left(2 \frac{\Delta T}{T}\right)^2}
  $$
  
  $$
  \Delta g = g \times \frac{\Delta g}{g}
  $$

## Analysis

1. Compare your measured value of \( g \) with the standard value \( 9.81\, \text{m/s}^2 \).

2. Discuss:
   - The impact of measurement resolution on \( L \).
   - Variability in timing measurements and its effect on \( g \).
   - Assumptions made during the experiment and potential limitations.

## Deliverables

1. **Tabulated data (Markdown table):**

| Trial | \( T_{10} \) (s) | Notes/Comments |
|-------|------------------|----------------|
| 1     |                  |                |
| ...   |                  |                |
| 10    |                  |                |

- Calculated values for \( \overline{T}_{10} \), \( s_{T_{10}} \), \( \Delta \overline{T}_{10} \), \( T \), \( \Delta T \), \( g \), and \( \Delta g \).

2. **Discussion** on uncertainty sources and their impact on results.
