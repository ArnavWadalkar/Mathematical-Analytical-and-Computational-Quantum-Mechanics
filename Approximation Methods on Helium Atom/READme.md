The Helium Atom (Approximation Methods)
**File:** `Helium_Atom-2.pdf`

### The Problem
The Helium atom is a classic "Three-Body Problem" (One nucleus, two electrons). Because the electrons repel each other, the Schrödinger equation cannot be separated into solvable parts.

The full Hamiltonian is:
$$H = -\frac{\hbar^2}{2m}(\nabla_1^2 + \nabla_2^2) - \frac{Ze^2}{4\pi\epsilon_0}\left(\frac{1}{r_1} + \frac{1}{r_2}\right) + \frac{e^2}{4\pi\epsilon_0 |r_1 - r_2|}$$

The last term (electron-electron repulsion) is the troublemaker. This document derives solutions using three levels of approximation.

### 1. The Naive Approach
If we simply ignore the repulsion term, Helium looks like two independent Hydrogen atoms.
* **Calculated Energy:** $-109 \text{ eV}$
* **Experimental Value:** $-79.0 \text{ eV}$
* **Verdict:** A $38\%$ error. Clearly, electrons *do* notice each other.

### 2. First-Order Perturbation Theory
We treat the repulsion term as a small perturbation $H'$ and calculate its expectation value $\langle \psi_0 | H' | \psi_0 \rangle$.
* **Calculated Energy:** $-74.8 \text{ eV}$
* **Verdict:** Much better! This confirms that electron correlation is a major energy component.

### 3. The Variational Method (Screening)
We introduce a trial wavefunction with an adjustable parameter $\alpha$ (effective nuclear charge). We ask: "What effective charge does one electron 'see' when the other electron is in the way?"
* **The Physics:** This accounts for **Screening**. One electron clouds the view of the nucleus for the other, effectively reducing the nuclear charge from $Z=2$ to $Z_{eff} = 1.6875$.
* **Calculated Energy:** $-77.5 \text{ eV}$
* **Verdict:** The closest approximation to reality in this set.
---

## Author
**Arnav Wadalkar**
*National Institute of Technology, Rourkela*
