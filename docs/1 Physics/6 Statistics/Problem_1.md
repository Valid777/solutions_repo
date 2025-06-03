# 🧮 Problem 2: Exploring the Central Limit Theorem through Simulations

## 📘 Motivation

The Central Limit Theorem (CLT) is a cornerstone of probability and statistics. It states that the **sampling distribution of the sample mean approaches a normal distribution** as the sample size increases, regardless of the population’s original distribution.

This theorem is crucial in practice because it:

- 📈 Justifies the use of normal approximations in statistical inference
- 🔍 Helps estimate population parameters from samples
- 🛠️ Is used in quality control and hypothesis testing

Simulations provide a hands-on, intuitive way to **visualize and understand** this powerful concept.

---

## 🎯 Task Breakdown

### 1️⃣ Simulating Sampling Distributions

Choose and simulate from the following population distributions:

- 📏 **Uniform distribution**
- ⏱ **Exponential distribution**
- 🎲 **Binomial distribution**

For each distribution, generate a large population dataset (e.g., 100,000 values).

---

### 2️⃣ Sampling and Visualization

For each distribution:

- Randomly take samples of sizes `n = 5, 10, 30, 50`
- Compute the **sample mean**
- Repeat the sampling process many times (e.g., 1000 repetitions)
- Plot histograms of the sample means for each `n`

👉 **Observe how the distribution of sample means becomes more normal as `n` increases.**

---

### 3️⃣ Parameter Exploration

Investigate:

- 📏 How sample size `n` affects the convergence to a normal distribution
- 🔺 The effect of the original distribution’s shape on convergence speed
- ⚖️ The impact of population variance on the spread of sampling distributions

---

### 4️⃣ Practical Applications

Reflect on where CLT is used in real life:

- 📊 **Estimating population means** in surveys or experiments
- 🏭 **Quality control** in manufacturing processes
- 💸 **Predictive modeling** in economics and finance
- 📐 **Risk analysis** in engineering and insurance

---

## 📦 Deliverables

- ✅ A Colab notebook or Markdown report with all steps
- 📉 Histograms for all sample sizes and distributions
- 🧪 Python code used for simulations
- 💬 Discussion of how results align with CLT expectations

---

## 🧠 Hints & Tools

- 🔢 Use `numpy` for generating random data:
  - `np.random.uniform(...)`
  - `np.random.exponential(...)`
  - `np.random.binomial(...)`
- 📊 Use `matplotlib.pyplot` or `seaborn` to draw histograms
- 🔁 Loop through different sample sizes and store sample means
- 📝 Label axes and titles clearly to show convergence visually
- 📚 Start with simpler distributions (e.g., uniform) before exploring complex ones

---

## 🌐 Applications

- 📐 Statistical Inference
- ⚡ Power Grid Forecasting
- 🧪 Simulation Models
- 🧠 Machine Learning Model Evaluation

