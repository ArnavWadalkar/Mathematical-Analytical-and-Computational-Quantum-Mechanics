# The Zeeman Effect in Hyperfine Muonium Atom

## Overview
This project models the behavior of **Muonium**, a hydrogen-like atom consisting of a positive muon ($\mu^+$) and an electron ($e^-$), when placed in a homogeneous magnetic field along the z-axis.

The simulation solves for the energy eigenvalues of the system by constructing the full Hamiltonian, accounting for both the internal **Hyperfine coupling** and the external **Zeeman effect**. The code visualizes how energy levels split and mix as the magnetic field strength increases, demonstrating phenomena such as the **Quadratic Zeeman effect** and the **Paschen-Back effect**.

## Theoretical Background

### The Hamiltonian
The total Hamiltonian of the system is defined as:

$$H = H_0 - [\vec{\mu}(\mu) + \vec{\mu}(e)] \cdot \vec{B} - \frac{8\pi}{3} \vec{\mu}(\mu) \cdot \vec{\mu}(e) \cdot \delta(\vec{r})$$

1.  **$H_0$:** The unperturbed atom Hamiltonian (kinetic + potential energy).
2.  **Zeeman Term:** $-[\vec{\mu}(\mu) + \vec{\mu}(e)] \cdot \vec{B}$. This represents the interaction with the external magnetic field. The field twists the particles to align their spins for lower energy.
3.  **Interaction Term (Fermi Contact Term):** Describes the hyperfine structure where $e^-$ and $\mu^+$ spins interact with each other. This term causes splitting even when $B=0$.

Once the magnetic field is turned on, two forces compete:
* **Hyperfine Coupling:** The spins want to couple to each other (align or anti-align).
* **Zeeman Effect:** The external field $B$ wants to twist both spins to align with the z-axis.

### Mixing and Basis States
The mathematical solution involves transforming between the **coupled basis** $|F, M\rangle$ and the **uncoupled basis** $|m_s^{(e)}, m_s^{(\mu)}\rangle$.

* **Case A ($M = \pm 1$):** The spins are already parallel. There is no conflict between the effects, and no mixing occurs. The energy shift is linear.
* **Case B ($M = 0$):** Mixing occurs between the **Triplet** ($|1,0\rangle$) and **Singlet** ($|0,0\rangle$) states. The magnetic field acts as a bridge, allowing the system to hop between these states. This is solved using the mixing matrix $W$.

## Computational Methodology
The Python notebook (`Zeemaneffect.ipynb`) calculates the energy spectrum numerically:

1.  **Constants:** Defines Bohr magnetons ($\mu_B$), g-factors ($g_e, g_\mu$), and the hyperfine splitting constant ($\Delta E$).
2.  **Matrix Construction:** Uses Pauli matrices ($\sigma_x, \sigma_y, \sigma_z$) and Kronecker products to construct the $4 \times 4$ Hamiltonian matrix in the uncoupled spin basis.
3.  **Diagonalization:** Solves the eigenvalue problem (`np.linalg.eigh`) for a range of magnetic field strengths ($B$) to obtain the four energy eigenstates.

## Visual Results

### 1. The Breit-Rabi Diagram (Energy Splitting)
This plot visualizes the energy eigenvalues as a function of the magnetic field.

<p align="center">
  <img src="plots/Zeeman_effect.png" width="600" alt="Energy Splitting">
</p>

* **Weak Fields ($x \ll 1$):** The system exhibits the **Quadratic Zeeman effect**.
* **Strong Fields ($x \gg 1$):** The system transitions to the **Linear Zeeman effect** (or **Paschen-Back effect**). Here, the electron and muon spins become independent (ignorant of each other) because the external field interactions dominate the internal coupling.

### 2. Transition Frequencies
These plots show the frequency of transitions between energy levels, which corresponds to spectroscopic observables.

<p align="center">
  <img src="plots/transitionfreq2.png" width="600" alt="Low Frequency">
</p>

* **Low Field:** The hyperfine splitting transition ($\nu_{12}$) decreases as the field mixes the states.

<p align="center">
  <img src="plots/Transitionfreq.png" width="600" alt="High Frequency">
</p>

* **High Field:** The transition frequency increases linearly, characteristic of the dominant Zeeman effect on the electron spin.

## Theoretical Remarks

### Level Crossing Resonance
The simulation allows us to identify **Level Crossing Resonance**. This phenomenon occurs when the external magnetic field is tuned such that two energy levels become degenerate (energy gap $\Delta E \to 0$). In this state, the system becomes resonant with the static environment, allowing even tiny interactions to cause transitions.

### Unified Formula
The code validates the unified energy formula derived in the theory:

$$E(F,M) = E_{1s} - \frac{1}{4}\Delta E - g^{(\mu)}\mu_B^{(\mu)}MB + (-1)^{F+1} \frac{\Delta E}{2} \sqrt{1 + 2Mx + x^2}$$
