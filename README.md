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

NOTE - This article provides an overview of the mathemematical theorems required to justify Quantum Mehchanics and it's formalisms. There is no proof provided for any theorem. However they can be found in many of the excellent mathematical physics texts available. Further, if mathematical foundations of Quantum Mechanics be an ocean, the article only provides a structural map of the surface of it. It does not provide the rigorous mathematical justifications, origin or underlying proofs. The article however provides intuitive or elementary justifications of selected topics.

This module establishes the rigorous mathematical language required to describe quantum systems, moving beyond basic wave mechanics into functional analysis and measure theory.

* **Hilbert Space Formalism:** Inner product spaces, dual spaces, and the Riesz Representation Theorem.
* **Linear Operators:** Bounded vs. unbounded operators, self-adjoint observables, and Stone's Theorem.
* **Spectral Theory:** Generalizing diagonalization for infinite-dimensional spaces, Projection-Valued Measures (PVM), and the Spectral Theorem.
* **Statistical States & Measurement:** Density matrices, Schatten-class operators, POVMs, and Quantum Bayesianism.
* **Quantum Kinetics:** Symmetry groups (Wigner’s theorem), Canonical Commutation Relations (CCR), and the classical limit.
* **Entanglement:** Tensor products, Schmidt decomposition, Bell’s Theorem, and von Neumann entropy.

### 2. The Stark Effect
*Folder: `Analytical and Computational Analysis of Stark Effect`*

NOTE - The plots are produced with the help of AI. I have used the wonderful book Quantum Physics by Florian Sheck as a reference for the mathematical work of this article.

An analytical and computational study of the shifting and splitting of spectral lines under an external electric field $\vec{E}$.

* **Linear Stark Effect:** Analyzes degenerate state splitting (Hydrogen $n=2$) and the formation of hybrid orbitals.
* **Quadratic Stark Effect:** Investigates non-degenerate shifts (Hydrogen $n=1$) and electric polarizability.
* **The Continuum Problem:** Demonstrates the necessity of continuum states (unbound electrons) by quantifying the discrepancy between discrete bound-state summation and theoretical values (~18.6% contribution from the continuum).
* **Key Files:** `Linear_Stark.ipynb`, `Quadratic_Stark.ipynb`, `Analytical_solution.pdf`.

### 3. The Zeeman Effect (Muonium)
*Folder: `Analytical and Computational Analysis of Zeeman Effect`*

NOTE - The plots are produced with the help of AI. I have used the wonderful book Quantum Physics by Florian Sheck as a reference for the mathematical work of this article.

Models the behavior of **Muonium** ($\mu^+ e^-$) in a homogeneous magnetic field, solving for the interplay between internal Hyperfine coupling and the external Zeeman effect.

* **Hamiltonian Construction:** Includes the unperturbed atom, Zeeman terms, and the Fermi contact interaction.
* **Basis Transformation:** Solves mixing between the Coupled basis ($|F, M\rangle$) and Uncoupled basis using numerical diagonalization.
* **Visualizations:**
    * **Breit-Rabi Diagram:** Maps energy splitting from the quadratic regime (weak field) to the Paschen-Back effect (strong field).
    * **Level Crossing Resonance:** Identifies magnetic field strengths where energy levels degenerate, allowing for resonant transitions.
* **Key Files:** `Zeemaneffect.ipynb`, `Zeeman_Effect_Muonium.pdf`.

### 4. Approximation methods on Helium Atom
*Folder: `Approximation Methods on Helium Atom'*

NOTE - I have used the wonderful book Quantum Physics by Florian Sheck as a reference for the mathematical work of this article.

A theoretical study of the ground state of the Helium atom, addressing the classic "Three-Body Problem" where the electron-electron interaction term ($e^2/r_{12}$) prevents an exact analytical solution.

* **Perturbation Theory:** Treats the electron repulsion as a first-order perturbation to the independent particle model, significantly correcting the naive energy estimate (-109 eV $\to$ -74.8 eV).
* **Variational Method:** Implements trial wavefunctions with an adjustable effective nuclear charge parameter ($\alpha$).
* **Nuclear Screening:** Demonstrates how one electron "screens" the nucleus from the other, resulting in an optimal effective charge $Z_{eff} \approx 1.69$ rather than the bare nuclear charge $Z=2$.
* **Key Files:** `Helium_Atom-2.pdf`.

### 5. Group Theoretic Analysis of the Nuclear Shell Model
*Folder: `Nuclear Shell Model`*

> **NOTE:** The interactive HTML simulation in this module was generated with the assistance of AI. Further, the structure and content of the article is inspired and influenced by Modern Quantum Mehcanics by JJ Sakurai and Jim Napolitano.

An exploration of how nucleons arrange into discrete energy levels by tracking the evolution of the nuclear potential and its fundamental symmetries.
* **Core Topics:** SU(3) symmetry in Isotropic Harmonic Oscillators, SO(3) symmetry in Infinite/Finite Square Wells, Woods-Saxon potential boundaries, and SU(2) collapse via Spin-Orbit Coupling.
* **Key Files:** `Nulcear_Shell_Model.pdf`, `Nuclear_shell_model.html`

## Techniques
* **Python:** `numpy`, `scipy` (Linear Algebra, Special Functions), `matplotlib` (Visualization).
* **Mathematics:** Introductory Functional Analysis, Perturbation Theory, Introductory Group Theory.
* **Documentation:** LaTeX-generated analytical derivations.

## License
This project is open for educational and research use.
