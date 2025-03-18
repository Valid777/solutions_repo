# Investigating the Range as a Function of the Angle of Projection

## 1. Theoretical Foundation

Projectile motion describes the motion of an object thrown into the air, subject to only the acceleration of gravity.

**Assumptions:**
- No air resistance
- Flat ground (launch and landing at the same height)
- Constant gravitational acceleration `g`

The equations of motion are:
- Horizontal motion: `x(t) = v0 * cos(θ) * t`
- Vertical motion: `y(t) = v0 * sin(θ) * t - (1/2) * g * t^2`

At the time of landing, `y(t) = 0`. Solving for time of flight `T`:

The **horizontal range** `R` is:

### Key Takeaways:
- `R` depends on the sine of twice the projection angle `2θ`
- Maximum range occurs at `θ = 45°` (when sin(2θ) = 1)

---

## 2. Analysis of the Range

We will simulate the relationship between the angle `θ` and range `R` for different initial velocities `v0` and gravitational accelerations `g`.

## 3. Implementation

### Importing Libraries
```python
import numpy as np
import matplotlib.pyplot as plt
def projectile_range(v0, theta_deg, g=9.81):
    theta_rad = np.radians(theta_deg)
    R = (v0**2) * np.sin(2 * theta_rad) / g
    return R
angles = np.linspace(0, 90, 100)  # angles from 0 to 90 degrees

# Different initial velocities
velocities = [10, 20, 30]  # m/s
g_values = [9.81, 1.62, 24.79]  # Earth, Moon, Jupiter gravity
plt.figure(figsize=(12, 6))

for v0 in velocities:
    ranges = projectile_range(v0, angles)
    plt.plot(angles, ranges, label=f'v₀ = {v0} m/s')

plt.title('Range vs Angle of Projection (Earth gravity)')
plt.xlabel('Angle of Projection (degrees)')
plt.ylabel('Range (m)')
plt.legend()
plt.grid(True)
plt.show()
plt.figure(figsize=(12, 6))

for g in g_values:
    ranges = projectile_range(20, angles, g=g)
    plt.plot(angles, ranges, label=f'g = {g} m/s²')

plt.title('Range vs Angle of Projection (Different Gravities)')
plt.xlabel('Angle of Projection (degrees)')
plt.ylabel('Range (m)')
plt.legend()
plt.grid(True)
plt.show()
