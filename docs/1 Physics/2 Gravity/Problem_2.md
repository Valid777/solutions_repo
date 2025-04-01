import numpy as np
import matplotlib.pyplot as plt
import os

# Create a directory to save figures if it doesn't exist
if not os.path.exists("figures"):
    os.makedirs("figures")

# 1. Theoretical Foundation: Calculate the projectile motion trajectory
def projectile_motion(theta, v0, g=9.81, h0=0):
    """
    Calculate the trajectory and range of a projectile.
    
    Parameters:
        theta (float): Launch angle in degrees
        v0 (float): Initial velocity in m/s
        g (float): Gravitational acceleration in m/s^2 (default: 9.81)
        h0 (float): Initial height in meters (default: 0)
    
    Returns:
        range_x (float): Horizontal range in meters
        x (array): x-coordinates of the trajectory for plotting
        y (array): y-coordinates of the trajectory for plotting
    """
    # Convert angle from degrees to radians
    theta_rad = np.radians(theta)
    
    # Calculate the x and y components of the initial velocity
    v0x = v0 * np.cos(theta_rad)
    v0y = v0 * np.sin(theta_rad)
    
    # Calculate the time of flight by solving the quadratic equation for y(t) = 0
    # y(t) = h0 + v0y*t - (1/2)*g*t^2 = 0
    a = -0.5 * g
    b = v0y
    c = h0
    discriminant = b**2 - 4*a*c
    t_flight = (-b + np.sqrt(discriminant)) / (2*a)  # Take the positive root
    
    # Calculate the horizontal range (range_x = v0x * t_flight)
    range_x = v0x * t_flight
    
    # Generate points for the trajectory (x, y coordinates)
    t = np.linspace(0, t_flight, 100)
    x = v0x * t
    y = h0 + v0y * t - 0.5 * g * t**2
    
    return range_x, x, y

# 2. Analysis: Plot the range as a function of the launch angle
def analyze_range_vs_angle(v0, g=9.81, h0=0):
    """
    Analyze and plot the horizontal range as a function of the launch angle.
    
    Parameters:
        v0 (float): Initial velocity in m/s
        g (float): Gravitational acceleration in m/s^2
        h0 (float): Initial height in meters
    """
    # Create an array of angles from 0 to 90 degrees
    angles = np.linspace(0, 90, 91)
    ranges = []
    
    # Calculate the range for each angle
    for theta in angles:
        range_x, _, _ = projectile_motion(theta, v0, g, h0)
        ranges.append(range_x)
    
    # Plot the range vs. angle
    plt.figure(figsize=(10, 6))
    plt.plot(angles, ranges, label=f"Initial velocity = {v0} m/s, g = {g} m/s², h0 = {h0} m")
    plt.xlabel("Launch Angle (degrees)")
    plt.ylabel("Horizontal Range (m)")
    plt.title("Horizontal Range vs. Launch Angle")
    plt.grid(True)
    plt.legend()
    plt.savefig("figures/range_vs_angle.png")
    plt.show()

# 3. Visualization: Plot trajectories for different angles
def plot_trajectories(v0, angles, g=9.81, h0=0):
    """
    Plot the trajectories of the projectile for different launch angles.
    
    Parameters:
        v0 (float): Initial velocity in m/s
        angles (list): List of launch angles in degrees
        g (float): Gravitational acceleration in m/s^2
        h0 (float): Initial height in meters
    """
    plt.figure(figsize=(10, 6))
    for theta in angles:
        range_x, x, y = projectile_motion(theta, v0, g, h0)
        plt.plot(x, y, label=f"Angle = {theta}°")
    
    plt.xlabel("Horizontal Distance (m)")
    plt.ylabel("Height (m)")
    plt.title(f"Projectile Trajectories (Initial velocity = {v0} m/s)")
    plt.grid(True)
    plt.legend()
    plt.savefig("figures/trajectories.png")
    plt.show()

# 4. Comparison: Analyze the effect of different initial conditions
def compare_different_conditions():
    """
    Compare the range for different initial velocities and heights.
    """
    v0_values = [10, 20, 30]  # Different initial velocities
    h0_values = [0, 10]  # Different initial heights
    angles = np.linspace(0, 90, 91)  # Angles from 0 to 90 degrees
    
    plt.figure(figsize=(10, 6))
    for v0 in v0_values:
        for h0 in h0_values:
            ranges = []
            for theta in angles:
                range_x, _, _ = projectile_motion(theta, v0, g=9.81, h0=h0)
                ranges.append(range_x)
            plt.plot(angles, ranges, label=f"v0 = {v0} m/s, h0 = {h0} m")
    
    plt.xlabel("Launch Angle (degrees)")
    plt.ylabel("Horizontal Range (m)")
    plt.title("Range Comparison for Different Initial Conditions")
    plt.grid(True)
    plt.legend()
    plt.savefig("figures/comparison.png")
    plt.show()

# Main program
if __name__ == "__main__":
    # Define initial parameters
    v0 = 20  # Initial velocity in m/s
    angles = [15, 30, 45, 60, 75]  # List of angles to plot trajectories
    
    # Step 1: Analyze the range as a function of the launch angle
    print("Analyzing the range as a function of the launch angle...")
    analyze_range_vs_angle(v0)
    
    # Step 2: Plot trajectories for different angles
    print("Plotting trajectories for different angles...")
    plot_trajectories(v0, angles)
    
    # Step 3: Compare the effect of different initial conditions
    print("Comparing the effect of different initial conditions...")
    compare_different_conditions()