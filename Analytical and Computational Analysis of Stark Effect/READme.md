# The Stark Effect: Analytical and Computational Study

## Overview
This project explores the **Stark Effect**—the shifting and splitting of spectral lines of atoms due to an external electric field $\vec{E}$. 

The folder contains analytical derivations using Time-Independent Perturbation Theory with a computational Python implementation to visualize the physics. We analyze two distinct cases:
1. **Linear Stark Effect:** Degenerate states (Hydrogen $n=2$).
2. **Quadratic Stark Effect:** Non-degenerate states (Hydrogen $n=1$).

## Project Structure
* `Analytical_solution.pdf`: Complete handwritten derivation of the 1st and 2nd order energy corrections, selection rules, and matrix elements.
* `Linear_Stark.ipynb`: Python simulation for the $n=2$ level, visualizing the splitting and hybrid orbitals.
* `Quadratic_Stark.ipynb`: Python simulation for the $n=1$ level, calculating polarizability and investigating the continuum contribution.

---

## 1. Theoretical Background
Based on the derivations in `Analytical_solution.pdf`:
* The interaction Hamiltonian is $H_1 = -\vec{d} \cdot \vec{E} = e z E$.
* **Selection Rules:** The dipole operator has odd parity. It only connects states with opposite parity ($l \neq l'$).
* **Linear Effect:** Only occurs in degenerate bases (like $2s$ and $2p$) where the field can mix states to form hybrid orbitals with a permanent dipole.
* **Quadratic Effect:** Occurs in non-degenerate states ($1s$). The field induces a dipole moment first ($d_{ind} = \alpha E$), leading to an energy shift $\Delta E \propto E^2$.

---

## 2. Linear Stark Effect ($n=2$)
For the $n=2$ shell of Hydrogen, we have 4 states: $|2s,0\rangle, |2p,0\rangle, |2p,\pm 1\rangle$.
The electric field mixes $|2s\rangle$ and $|2p,0\rangle$, lifting the degeneracy for the strong field approximation.

### Key Results:
* **Energy Splitting:** The energy levels split linearly as $E^{(1)} = \pm 3 e a_0 E$.
* **Hybridization:** The new eigenstates are superpositions $\psi_{\pm} = \frac{1}{\sqrt{2}}(|2s\rangle \pm |2p\rangle)$.
* **Charge Asymmetry:** The electron cloud shifts, creating a permanent dipole shape (the "egg" shape).

<p align="center">
  <img src="Analytical and Computational Analysis of Stark Effect/plots/linearstarksplitting.png" width="600" alt="Linear Splitting Graph">
</p>
 
<p align="center">
  <img src="Analytical and Computational Analysis of Stark Effect/plots/polarizationagainst.png" width="600" alt="Hybrid Orbital against field">
</p>

<p align="center">
  <img src="Analytical and Computational Analysis of Stark Effect/plots/polarizationwith.png" width="600" alt="Hybrid Orbital with field">
</p>

---

## 3. Quadratic Stark Effect ($n=1$)
For the ground state, the first-order correction is zero due to parity. We calculate the second-order shift:
$$\Delta E^{(2)} = \sum_{n \neq 1} \frac{|\langle 1s | H_1 | n \rangle|^2}{E_1 - E_n} = -\frac{1}{2} \alpha E^2$$

### Key Results:
* **Binding Energy:** The shift is always negative (lowering energy).
* **Potential Tilting:** The external field adds a linear term $+eEz$ to the Coulomb potential, creating a barrier that allows for **tunneling** (ionization) at high fields.

---

## 4. The Continuum Problem (Physics Insight)
In `Quadratic_Stark.ipynb`, we computed the Stark coefficient by summing over bound states ($n=2$ to $n=20$).

* **Theoretical Coefficient:** $\approx -2.25$
* **Computed Coefficient:** $\approx -1.83$
* **Error:** ~18.6%

  <p align="center">
  <img src="Analytical and Computational Analysis of Stark Effect/plots/coefferror.png" width="600" alt="Coefficient discrepancy">
</p>

This discrepancy is **not** a calculation error. It represents the contribution of the **Continuum States** (unbound electrons). The sum over discrete bound states saturates at ~81%, proving that the continuum is physically required to complete the basis set.
