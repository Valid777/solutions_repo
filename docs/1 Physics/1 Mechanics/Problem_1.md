# Problem 1
import numpy as np
import matplotlib.pyplot as plt

# Constants
g_earth = 9.8  # m/s^2
g_moon = 1.62  # m/s^2
v0 = 20.0      # initial velocity (m/s)

# Range function
def range_projectile(v0, theta_deg, g):
    theta = np.radians(theta_deg)  # Convert to radians
    return (v0**2 * np.sin(2 * theta)) / g

# Angles from 0 to 90 degrees
theta_deg = np.linspace(0, 90, 91)

# Calculate range for Earth and Moon
R_earth = range_projectile(v0, theta_deg, g_earth)
R_moon = range_projectile(v0, theta_deg, g_moon)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(theta_deg, R_earth, label=f'Earth (g = {g_earth} m/s²)', color='blue')
plt.plot(theta_deg, R_moon, label=f'Moon (g = {g_moon} m/s²)', color='red')
plt.xlabel('Angle of Projection (degrees)')
plt.ylabel('Range (meters)')
plt.title(f'Range vs Angle of Projection (v₀ = {v0} m/s)')
plt.grid(True)
plt.legend()
plt.show()

# Find max range and corresponding angle
max_R_earth = np.max(R_earth)
max_theta_earth = theta_deg[np.argmax(R_earth)]
print(f"Max range on Earth: {max_R_earth:.2f} m at {max_theta_earth}°")
