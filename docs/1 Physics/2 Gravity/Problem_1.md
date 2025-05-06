# 🌍 Orbital Period and Orbital Radius

---

## 🚀 **Motivation**

Kepler's Third Law — the square of the orbital period is proportional to the cube of the orbital radius — is a foundational principle in celestial mechanics:

> "The square of the period of a planet is directly proportional to the cube of the semi-major axis of its orbit."

This elegant relationship:
- Helps calculate planetary distances and masses,
- Enables satellite and orbital dynamics modeling,
- Links Newtonian gravity with astronomical observations.

---

## 🧮 **1. Theoretical Derivation**

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

## 🔍 **2. Astronomical Implications**

- Allows determination of planetary masses if radius and period are known.
- Enables accurate modeling of satellite orbits (e.g., Moon around Earth).
- Used in planning satellite launches and interplanetary missions.

---

## 💻 **3. Simulation (Python Code)**

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # m^3/kg/s^2
M = 5.972e24     # mass of Earth in kg

# Radii in meters (example: Low Earth Orbit to Geostationary)
radii = np.linspace(7e6, 4.2e7, 100)
periods = 2 * np.pi * np.sqrt(radii**3 / (G * M))

# Plotting
plt.figure(figsize=(8, 5))
plt.plot(radii / 1e6, periods / 3600, color='royalblue')
plt.xlabel('Orbital Radius (x10⁶ m)')
plt.ylabel('Orbital Period (hours)')
plt.title('Kepler’s Third Law: $T^2 \\propto r^3$')
plt.grid(True)
plt.tight_layout()
plt.show()
