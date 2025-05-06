# Orbital Period and Orbital Radius

---

## **Motivation**

Kepler's Third Law states that the square of the orbital period is proportional to the cube of the orbital radius, and it is a foundational principle in celestial mechanics.

> "The square of the period of a planet is directly proportional to the cube of the semi-major axis of its orbit."

This elegant relationship:

- Helps calculate planetary distances and masses,
- Enables satellite and orbital dynamics modeling,
- Links Newtonian gravity with astronomical observations.

---

## **1. Theoretical Derivation**

Starting from Newton’s law of universal gravitation and centripetal force:

\[
F_{\text{gravity}} = F_{\text{centripetal}} \Rightarrow \frac{G M m}{r^2} = \frac{m v^2}{r}
\]

Simplifying and solving for orbital velocity \( v \):

\[
v = \sqrt{\frac{G M}{r}}
\]

Now, using \( v = \frac{2\pi r}{T} \):

\[
\frac{2\pi r}{T} = \sqrt{\frac{G M}{r}} \Rightarrow T^2 = \frac{4\pi^2}{G M} r^3
\]

Thus proving:

\[
T^2 \propto r^3
\]

---

## **2. Astronomical Implications**

- Allows determination of planetary masses if radius and period are known.
- Enables accurate modeling of satellite orbits (e.g., Moon around Earth).
- Used in planning satellite launches and interplanetary missions.

---

### 3. Simulation (Python Code)

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # gravitational constant (m^3/kg/s^2)
M = 5.972e24     # mass of Earth in kg

# Radii in meters (example: Low Earth Orbit to Geostationary)
radii = np.linspace(7e6, 4.2e7, 100)
periods = 2 * np.pi * np.sqrt(radii**3 / (G * M))

# Plotting
plt.figure(figsize=(8, 5))
plt.plot(radii / 1e6, periods / 3600, color='royalblue')
plt.xlabel('Orbital Radius (×10⁶ m)')
plt.ylabel('Orbital Period (hours)')
plt.title("Kepler’s Third Law: Orbital Period vs Radius")
plt.grid(True)
plt.tight_layout()
plt.show()
```
### 4. Sample Table of Orbital Parameters

| Orbital Radius (km) | Period (hours) |
|---------------------|----------------|
| 7,000               | 1.6            |
| 10,000              | 2.8            |
| 15,000              | 5.2            |
| 20,000              | 8.2            |
| 26,600 (GPS)        | 12.0           |
| 35,786 (GEO)        | 24.0           |

---

### 5. Extension to Elliptical Orbits

Although derived for circular orbits, Kepler's Third Law also applies to elliptical orbits  
if *r* is replaced with the semi-major axis *a*.

---

### Limitations and Further Exploration

- Assumes two-body problem and ignores perturbations.  
- Doesn’t consider relativistic corrections (important near massive bodies).  
- Future extensions: elliptical orbits, n-body systems, or relativistic gravity.

---

### References

- Newton’s *Principia Mathematica*  
- Kepler’s Laws of Planetary Motion  
- NASA Orbital Mechanics Tutorials  

