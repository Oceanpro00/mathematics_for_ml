# Mathematics for Machine Learning Exercises

## Table of Contents

* [Project Overview](#project-overview)
* [Vector Math Visualization](#vector-math-visualization)
* [Vector Math – Key Concepts](#vector-math--key-concepts)
* [Vector Math – Why This Is Useful](#vector-math--why-this-is-useful)
* [Repository Structure](#repository-structure)
* [Credits](#credits)

---

## Project Overview

This repository tracks my hands-on exercises and notes from the Coursera course **Mathematics for Machine Learning: Linear Algebra** by **Imperial College London**. Rather than strictly following a week-by-week format, I’m creating individual tools and notebooks that help me better understand key topics through code and visualization.

Each notebook is meant to serve as a standalone explanation of a concept I find important, and something I can easily refer back to.

---

## Vector Math Visualization

This notebook explores **vector addition**, **subtraction**, and **scalar multiplication** using a plotting approach in Python with `matplotlib`. It includes an interactive section where vectors are appended to a list and visualized using a custom function.

In addition to scalar multiplication and directional plotting, the notebook demonstrates the **commutative property** of vector addition by shuffling the order of vectors and showing that the final position remains unchanged.

The plot shows how vectors:

* Chain tip-to-tail
* Change length with scaling
* Reverse direction with subtraction or negative scalars
* Accumulate position

**Original Order Plot:**

![Ordered Vector Plot](assets/vector_plot_example.png)

**Shuffled Order Plot (Commutativity Check):**

![Shuffled Vector Plot](assets/vector_plot_commutative.png)

Notebook location:

```bash
Subjects/vector_math/vector_math.ipynb
```

Key additions in this version:

* A function to build and visualize vectors step-by-step
* Scalar multiplication applied through repetition
* Comparison of ordered vs. shuffled vectors to confirm commutativity

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

## Repository Structure

```
Subjects/
└── vector_math/
    └── vector_math.ipynb       # Vector operations visualization
assets/
├── vector_plot_example.png         # Ordered vector plot
└── vector_plot_commutative.png     # Shuffled vector plot (commutativity)
README.md                           # This file
```

---

## Credits

* Course: [Mathematics for Machine Learning](https://www.coursera.org/learn/linear-algebra-machine-learning) by Imperial College London
* Visual explanations based on my interpretation of course material
* Plots generated using `matplotlib`

---

**Made by Sean Schallberger**
Exploring math and machine learning through code, one concept at a time.
