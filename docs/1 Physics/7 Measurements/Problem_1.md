## 🧪 Measurements

### 📌 Problem 1: Measuring Earth's Gravitational Acceleration with a Pendulum

---

### 🔍 Motivation:
The acceleration due to gravity **g** is a fundamental constant that influences a wide range of physical phenomena. Measuring **g** accurately is crucial for understanding gravitational interaction, designing structures, and conducting experiments in various fields. One classic method for determining **g** is through the oscillations of a simple pendulum, where the period of motion depends on the local gravitational field.

---

### 🎯 Task:
Measure the acceleration due to gravity using a pendulum and in detail analyze the uncertainties in the measurements.

This exercise emphasizes rigorous measurement practices, uncertainty analysis, and their role in experimental physics.

---

### 🧪 Procedure:

#### 1. Materials:
- A string (1 or 1.5 meters long).
- A small weight (e.g., bag of coins, bag of sugar, key chain) mounted on the string.
- Stopwatch (or smartphone timer).
- Meter stick or measuring tape.

#### 2. Setup:
- Attach the weight to the string and fix the other end to a sturdy support.
- Measure the length of the pendulum, $L$, from the suspension point to the center of the weight using a ruler or measuring tape. Record the **resolution** of the measuring tool and calculate the uncertainty as half the resolution:  
  $$
  \Delta L = \frac{\text{Ruler Resolution}}{2}
  $$

#### 3. Data Collection:
- Displace the pendulum slightly (~15°) and release it.
- Measure the time for 10 full oscillations ($T_{10}$) and repeat this process 10 times. Record all 10 measurements.
- Calculate the mean time for 10 oscillations ($\overline{T_{10}}$) and the standard deviation ($s_{T_{10}}$).
- Determine the uncertainty in the mean time as:  
  $$
  \Delta \overline{T_{10}} = \frac{s_{T_{10}}}{\sqrt{n}}
  $$  
  where $n = 10$

---

### 🧮 Calculations:

#### 1. Calculate the period:
$$
T = \frac{\overline{T_{10}}}{10}, \quad \Delta T = \frac{\Delta \overline{T_{10}}}{10}
$$

#### 2. Determine $g$:
$$
g = \frac{4\pi^2 L}{T^2}
$$

#### 3. Propagate uncertainties:
$$
\Delta g = g \sqrt{ \left( \frac{\Delta L}{L} \right)^2 + \left( \frac{2\Delta T}{T} \right)^2 }
$$

---

### 📊 Analysis:

#### 1. Compare your measured $g$ with the standard value (9.81 m/s²).

#### 2. Discuss:
- The effect of measurement resolution on $\Delta L$.
- Variability in timing and its impact on $\Delta T$.
- Any assumptions or experimental limitations.

---

### 📦 Deliverables:
- Tabulated data in markdown:
  - $L$, $T_{10}$ measurements, $\overline{T_{10}}, s_{T_{10}}, \Delta T$
  - Calculated $g$ and $\Delta g$

- Discussion on sources of uncertainty and their impact on the results.
