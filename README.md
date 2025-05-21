# Vector Math Visualizer (Mathematics for Machine Learning Exercises)

## Table of Contents

* [Project Overview](#project-overview)
* [Vector Math Visualization](#vector-math-visualization)
    * [Vector Math – Key Concepts](#vector-math--key-concepts)
    * [Vector Math – Why This Is Useful](#vector-math--why-this-is-useful)
* [Dot Product Trial](#dot-product-trial)
  * [Dot Product – Key Concepts](#dot-product--key-concepts)
  * [Dot Product – Why This Is Useful](#dot-product--why-this-is-useful)
* [Repository Structure](#repository-structure)
* [Credits](#credits)

---

## Project Overview

This repository tracks my hands-on exercises and notes from the Coursera course **Mathematics for Machine Learning: Linear Algebra** by **Imperial College London**. Rather than strictly following a week-by-week format, I’m creating individual tools and notebooks that help me better understand key topics through code and visualization.

Each notebook is meant to serve as a standalone explanation of a concept I find important, and something I can easily refer back to.

---

## Vector Math Visualization

This notebook explores **vector addition**, **subtraction**, and **scalar multiplication** using a plotting approach in Python with `matplotlib`. It includes an interactive section where you can:

* Manually input vector components
* Choose a scalar multiplier
* Toggle between **addition** and **subtraction** mode
* Visualize chained vector movement from origin
* Shuffle vectors to test the **commutative property**
* Track each run in a persistent history log

Each plot displays cumulative vector movement using tip-to-tail logic. The final endpoint is marked and printed, showing the total displacement.

### Sample Output

```console
 VECTOR ADDITION HISTORY
Addition #1 - Ordered Vector Addition (Mode: subtract, Repeats: 4)
                Each vector added: [2, 2]
Addition #2 - Ordered Vector Addition (Mode: add, Repeats: 2)
                Each vector added: [-3, 1]
Addition #3 - Ordered Vector Addition (Mode: add, Repeats: 5)
                Each vector added: [0, -1]

 FINAL VECTOR POSITION IS
The net deplacement vector position is [-14, -11]

 SHUFFLED VECTOR ADDITION (COMMUTATIVITY CHECK)
The vectors are the same but appear in a random order.
Notice that the endpoint remains the same, demonstrating commutativity.

 FINAL VECTOR POSITION IS
The net deplacement vector position is [-14, -11]
```

### Original Order Plot:

![Ordered Vector Plot](assets/vector_plot_example.png)

### Shuffled Order Plot (Commutativity Check):

![Shuffled Vector Plot](assets/vector_plot_commutative.png)

### Notebook Location

```bash
Subjects/vector_math/vector_math.ipynb
```

---

## Vector Math – Key Concepts

* Vectors as directed quantities
* Tip-to-tail addition and subtraction
* Scalar multiplication and scaling effects
* Coordinate representations using basis vectors (i, j)
* Commutativity and associativity in vector addition

---

## Vector Math – Why This Is Useful

This notebook is built on the early vector lessons of the course, where we first explored what makes a vector and how we can manipulate them algebraically and geometrically. It helped clarify how:

* Vectors describe direction and magnitude
* Scalar multiplication changes size without changing direction
* Subtraction flips the vector
* Vector addition creates chained movement from point to point

In the course, vectors are introduced not just as arrows in space, but also as lists of attributes — which becomes important later in machine learning. This notebook makes those early lessons easier to see in action and gives me something to review or extend as I move deeper into the math.

Vectors also play a foundational role in machine learning. They’re used to represent input features, model weights, and encoded objects like words or images. Understanding how vectors behave when added, subtracted, or scaled makes it easier to understand how models transform data, how optimization works through gradients, and how data moves through high-dimensional spaces.

---

## Dot Product Trial

This notebook demonstrates how the **dot product** reveals directional relationships between two vectors, and expands into **scalar** and **vector projections** with clear explanations and step-by-step calculations.

### Features

* Generate or manually input two n-dimensional vectors
* Calculate:

  * Magnitudes (vector size)
  * Dot product
  * Cosine of the angle between vectors
  * Scalar projections
  * Vector projections
* Understand results through clean breakdowns:

  * Pythagorean theorem for magnitude
  * Cosine formula for dot product
  * Projection formulas and geometric interpretations

### Sample Output

```console
Vector 1 looks like:
[3, -4, 0]
and has a magnitude/ size of 5.0

Vector 2 looks like:
[10, 5, -6]
and has a magnitude/ size of 12.2474

MAGNITUDE BREAKDOWN
→ |v₁| = √(3² + -4² + 0²) = √(25) = 5.0

DOT PRODUCT RESULT:
The Dot product of vectors 1 and 2 is -10.0, which means that the vectors point in opposite directions

COSINE FORMULA BREAKDOWN
vector1 · vector2 = |v1| × |v2| × cos(θ)
-10.0 = 5.0 × 12.2474 × -0.1633
-10.0 = -10.0

GEOMETRIC INTERPRETATION OF COS(θ)
To put simply, this tells us:
- If θ = 0°, then cos(θ) = 1 → vectors point in the same direction
- If θ = 90°, then cos(θ) = 0 → vectors are perpendicular
- If θ = 180°, then cos(θ) = -1 → vectors point in opposite directions
→ The dot product combines the size of both vectors and the cosine of the angle between them

SCALAR PROJECTION OF VECTOR 1 ONTO VECTOR 2
The Scalar Projection of Vector 1 onto Vector 2 is -1.6329
→ This is the length of the 'shadow' cast by Vector 1 onto Vector 2

SCALAR PROJECTION FORMULA
Let:
  a = Vector 1
  b = Vector 2
scalar_proj = (a · b) / |b|

VECTOR PROJECTION OF VECTOR 1 ONTO VECTOR 2
The Vector Projection of Vector 1 onto Vector 2 is [-1.3322, -0.6661, 0.7993]
→ This is the vector that shows how much of Vector 1 lies *along* Vector 2

VECTOR PROJECTION FORMULA
Let:
  a = Vector 1
  b = Vector 2
vector_proj = [(a · b) / (b · b)] × b
```

### Notebook Location

```bash
Subjects/vector_math/dot_product_trial.ipynb
```

---

## Dot Product – Key Concepts

* The dot product measures how aligned two vectors are
* Cosine rule: **a · b = |a||b|cos(θ)**
* Scalar projection = the length of one vector "shadowed" onto another
* Vector projection = the actual directional vector formed from this shadow
* Interpretation:

  * Positive → same direction
  * Zero → perpendicular
  * Negative → opposite direction

---

## Dot Product – Why This Is Useful

Understanding dot products is essential for both geometry and machine learning:

* It tells us **how much two vectors "agree" in direction**
* Cosine similarity (based on dot product) is used in:

  * Natural language processing (text similarity)
  * Recommender systems
  * Image embedding comparisons
* Projections help:

  * Understand how much of one vector points in the direction of another
  * Analyze directional components in high-dimensional space
  * Support dimensionality reduction and optimization logic in ML

---

## Repository Structure

```
Subjects/
└── vector_math/
    ├── vector_math.ipynb            # Vector operations visualization
    └── dot_product_trial.ipynb      # Dot product + projection calculator and explanation
assets/
├── vector_plot_example.png          # Ordered vector plot
└── vector_plot_commutative.png      # Shuffled vector plot (commutativity)
README.md                            # This file
```

---

## Credits

* Course: [Mathematics for Machine Learning](https://www.coursera.org/learn/linear-algebra-machine-learning) by Imperial College London
* Visual explanations based on my interpretation of course material
* Plots generated using `matplotlib`

---

**Made by Sean Schallberger**
Exploring math and machine learning through code, one concept at a time.
