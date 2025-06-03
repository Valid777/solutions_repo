# Problem 2: Estimating Pi using Monte Carlo Methods

## Motivation
Monte Carlo simulations are a powerful class of computational techniques that use randomness to solve problems or estimate values. One of the most elegant applications of Monte Carlo methods is estimating the value of $\pi$ through geometric probability. By randomly generating points and analyzing their positions relative to a geometric shape, we can approximate $\pi$ in an intuitive and visually engaging way.

This problem connects fundamental concepts of probability, geometry, and numerical computation. It also provides a gateway to understanding how randomness can be harnessed to solve complex problems in physics, finance, and computer science. The Monte Carlo approach to $\pi$ estimation highlights the versatility and simplicity of this method while offering practical insights into convergence rates and computational efficiency.

## Task

### Part 1: Estimating $\pi$ Using a Circle

#### 1. Theoretical Foundation
- Explain how the ratio of points inside a circle to the total number of points in a square can be used to estimate $\pi$.
- Derive the formula $\pi \approx 4 \times (\text{points inside circle} / \text{total points})$ for a unit circle.

#### 2. Simulation
- Generate random points in a 2D square bounding a unit circle.
- Count the number of points falling inside the circle.
- Estimate $\pi$ based on the ratio of points inside the circle to the total points.

#### 3. Visualization
- Create a plot showing the randomly generated points, distinguishing those inside and outside the circle.

#### 4. Analysis
- Investigate how the accuracy of the estimate improves as the number of points increases.
- Discuss the convergence rate and computational considerations for this method.

### Part 2: Estimating $\pi$ Using Buffon’s Needle

#### 1. Theoretical Foundation
- Describe Buffon’s Needle problem, where $\pi$ can be estimated based on the probability of a needle crossing parallel lines on a plane.
- Derive the formula $\pi \approx (2 \times \text{needle length} \times \text{number of drops}) / (\text{line spacing} \times \text{number of crossings})$.

#### 2. Simulation
- Simulate the random dropping of a needle on a plane with parallel lines.
- Count the number of times the needle crosses a line.
- Estimate $\pi$ based on the derived formula.

#### 3. Visualization
- Create a graphical representation of the simulation, showing the needle positions relative to the lines.

#### 4. Analysis
- Explore how the number of needle drops affects the estimate’s accuracy.
- Compare the convergence rate of this method to the circle-based approach.

## Deliverables

1. **Markdown Document:**

    - Clear explanations of the methods and their corresponding formulas.
    - A detailed discussion of the theoretical foundations and simulation results.

2. **Python Scripts or Jupyter Notebooks Implementing the Simulations:**

    - Code for the circle-based Monte Carlo method.
    - Code for the Buffon’s Needle method.

3. **Graphical Outputs:**

    - Scatter plots displaying random points for the circle-based method, with points inside and outside the circle clearly distinguished.
    - Visualizations illustrating needle positions relative to parallel lines for Buffon’s Needle.

4. **Analysis:**

    - Tables or graphs depicting the convergence of the estimated $\pi$ value as a function of the number of iterations for both methods.
    - A comparison of the two methods, evaluating their accuracy and computational efficiency.

## Hints and Resources
- Use Python libraries such as NumPy for random number generation and Matplotlib for visualizations.
- For the circle-based method, ensure the random points are uniformly distributed within the square.
- For Buffon’s Needle, pay attention to geometric constraints, such as the relationship between the needle length and the distance between lines.
- Start with a small number of iterations to validate the implementation, then increase the sample size to observe convergence.