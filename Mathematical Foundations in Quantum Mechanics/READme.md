# Mathematical Foundations of Quantum Mechanics

**Author:** Arnav Wadalkar
|
**Department:** Department of Physics and Astronomy, NIT Rourkela

## Overview
This project develops the mathematical framework that describes the features of quantum systems, such as superposition, interference, quantum uncertainty, etc.

## Table of Contents

### 1. Hilbert Space Formalism
This section introduces the Hilbert space, which is a complete inner product space.
* **Physical Motivation:** We need a complex linear vector space to support linear superposition and continuous rotational symmetry, as seen in the double slit experiment.
* **Inner Products:** The inner product space is a normed linear space that defines angles and orthogonality.
* **Dual Space:** Introduces the Riesz Representation Theorem, which connects vectors (kets) to unique continuous linear functionals (bras).
* **Projections:** Discusses the Orthogonal Projection Theorem and how the projection operator splits the Hilbert space into a subspace and its orthogonal complement.
* **Quantum States:** Explains why states are "rays" in a projective Hilbert space rather than just vectors, due to the unobservable global phase.

### 2. Linear Operators in Hilbert Space
To measure, evolve, or rotate a system, we use operators that preserve the structure of the space.
* **Bounded vs. Unbounded:** Distinguishes between bounded operators (continuous) and unbounded operators (discontinuous, defined on a dense subset).
* **Adjoints and Self-Adjoint:** Physical observables are always self-adjoint operators because they guarantee real eigenvalues.
* **Unitary Operators:** These preserve the inner product and the norm. Stone's Theorem links strongly continuous unitary groups to self-adjoint generators.

### 3. Spectral Theory
This chapter generalizes diagonalization for infinite-dimensional spaces where standard matrix methods fail.
* **Spectrum and Resolvent:** Defines the spectrum as the set where the operator is not boundedly invertible. It is split into point, continuous, and residual spectra.
* **Projection-Valued Measures (PVM):** A map that assigns projections to Borel sets. This is the mathematical bridge between projections and measurement.
* **Spectral Theorem:** Provides a method to rewrite a self-adjoint operator as a multiplication by its eigenvalues using an integral over the spectral measure.

### 4. Statistical States and Measuring Theory
Formulates quantum mechanics as a statistical theory.
* **States:** Defined as positive, normalised linear functionals on the algebra of observables.
* **Density Matrices:** Uses the Schatten-class duality theorem to represent states via trace-class operators. It distinguishes between pure states and mixed states.
* **POVMs:** Introduces Positive Operator-Valued Measures (POVMs) as a more general form of measurement than PVMs. They are "unsharp" measurements.
* **Measurement Dynamics:** Describes the state update using Kraus operators and quantum instruments, interpreted as Bayesian conditioning on a noncommutative probability space.

### 5. Quantum Kinetics and Representation Theory
This section discusses the physical space and the dynamics of the system.
* **Symmetry and Groups:** Physical space is defined by groups of spatial translations and rotations. Wigner's theorem proves that physically equivalent descriptions must give the same probabilities.
* **Canonical Commutation Relations (CCR):** Uses Weyl’s relation to derive operators X and P. Explains the Schwartz space as the domain for these unbounded operators.
* **Schrödinger vs. Heisenberg:** Compares the active transformation (state evolution) and passive transformation (operator evolution).
* **Classical Limit:** Discusses Ehrenfest's theorem and the Wigner function to show how quantum mechanics connects to classical mechanics when $\hbar \to 0$.

### 6. Composite Quantum System and Entanglement
Characterises systems made of multiple parts using the tensor product structure.
* **Tensor Product:** The state space of a composite system is the tensor product of subsystem spaces, not the Cartesian product.
* **Schmidt Decomposition:** A method to write a bipartite pure state as a sum of perfectly correlated orthonormal states. The Schmidt rank defines if a state is entangled.
* **Entanglement:** Defined as the failure of separability. A global pure state can have mixed subsystems (improper mixing).
* **Bell's Theorem:** Proves that no theory satisfying local realism can reproduce all quantum mechanical predictions.
* **Entropy:** Quantifies entanglement using the von Neumann entropy of the reduced state, which equals the Shannon entropy of the Schmidt coefficients.


