# Quantum Mechanics: Analytical & Computational Studies

**Author:** Arnav Wadalkar  
**Department:** Department of Physics and Astronomy, NIT Rourkela

## Overview
This repository serves as a comprehensive collection of theoretical frameworks and computational simulations in Quantum Mechanics. It bridges the gap between rigorous mathematical formalism (Hilbert spaces, Spectral theory) and practical application (perturbation theory, numerical simulations of atomic systems).

The project is divided into distinct modules, each containing detailed analytical derivations (PDFs) and Python implementations (Jupyter Notebooks) to visualize quantum phenomena.

---

## Repository Structure

### 1. Mathematical Foundations of Quantum Mechanics
*Folder: `Mathematical Foundations in Quantum Mechanics`*

This module establishes the rigorous mathematical language required to describe quantum systems, moving beyond basic wave mechanics into functional analysis and measure theory.

* **Hilbert Space Formalism:** Inner product spaces, dual spaces, and the Riesz Representation Theorem.
* **Linear Operators:** Bounded vs. unbounded operators, self-adjoint observables, and Stone's Theorem.
* **Spectral Theory:** Generalizing diagonalization for infinite-dimensional spaces, Projection-Valued Measures (PVM), and the Spectral Theorem.
* **Statistical States & Measurement:** Density matrices, Schatten-class operators, POVMs, and Quantum Bayesianism.
* **Quantum Kinetics:** Symmetry groups (Wigner’s theorem), Canonical Commutation Relations (CCR), and the classical limit.
* **Entanglement:** Tensor products, Schmidt decomposition, Bell’s Theorem, and von Neumann entropy.

### 2. The Stark Effect
*Folder: `Analytical and Computational Analysis of Stark Effect`*

An analytical and computational study of the shifting and splitting of spectral lines under an external electric field $\vec{E}$.

* **Linear Stark Effect:** Analyzes degenerate state splitting (Hydrogen $n=2$) and the formation of hybrid orbitals.
* **Quadratic Stark Effect:** Investigates non-degenerate shifts (Hydrogen $n=1$) and electric polarizability.
* **The Continuum Problem:** Demonstrates the necessity of continuum states (unbound electrons) by quantifying the discrepancy between discrete bound-state summation and theoretical values (~18.6% contribution from the continuum).
* **Key Files:** `Linear_Stark.ipynb`, `Quadratic_Stark.ipynb`, `Analytical_solution.pdf`.

### 3. The Zeeman Effect (Muonium)
*Folder: `Analytical and Computational Analysis of Zeeman Effect`*

Models the behavior of **Muonium** ($\mu^+ e^-$) in a homogeneous magnetic field, solving for the interplay between internal Hyperfine coupling and the external Zeeman effect.

* **Hamiltonian Construction:** Includes the unperturbed atom, Zeeman terms, and the Fermi contact interaction.
* **Basis Transformation:** Solves mixing between the Coupled basis ($|F, M\rangle$) and Uncoupled basis using numerical diagonalization.
* **Visualizations:**
    * **Breit-Rabi Diagram:** Maps energy splitting from the quadratic regime (weak field) to the Paschen-Back effect (strong field).
    * **Level Crossing Resonance:** Identifies magnetic field strengths where energy levels degenerate, allowing for resonant transitions.
* **Key Files:** `Zeemaneffect.ipynb`, `Zeeman_Effect_Muonium.pdf`.

---

## Future Work

The following modules are currently in development and will be added to the repository soon:

* **Variational Method for Helium:** Implementing trial wavefunctions to approximate the ground state energy of the Helium atom, accounting for electron-electron repulsion.
* **Quantum Monte Carlo (QMC) for Helium:** A stochastic approach to solving the many-body Schrödinger equation for high-precision energy estimates.

---

## Technologies
* **Python:** `numpy`, `scipy` (Linear Algebra, Special Functions), `matplotlib` (Visualization).
* **Mathematics:** Functional Analysis, Perturbation Theory, Group Theory.
* **Documentation:** LaTeX-generated analytical derivations.

## License
This project is open for educational and research use.
