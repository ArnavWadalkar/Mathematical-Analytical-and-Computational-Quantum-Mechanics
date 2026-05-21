## Group Theoretic Analysis of the Nuclear Shell Model

**Files:** * `Nulcear_Shell_Model.pdf` (Analytical Derivations)
* `Nuclear_shell_model.html` (Interactive Visualization, AI-generated)

**NOTE:** The interactive HTML simulation in this module was generated with the assistance of AI.

### The Problem
The Nuclear Shell Model explains how nucleons arrange themselves into discrete energy levels, but deriving the exact energy gaps (and the resulting "magic numbers") is complex. Instead of just solving brute-force differential equations, this module tracks the problem through the lens of **Group Theory**—watching how fundamental symmetries are preserved or broken as we make the nuclear potential more realistic.

### 1. The Isotropic Harmonic Oscillator (SU(3) Symmetry)
We start by approximating the nucleus as a simple 3D parabolic bowl. 
* **The Physics:** The spatial dimensions ($x, y, z$) completely decouple. This creates a massive $SU(3)$ symmetry.
* **The Effect:** Energy levels are highly degenerate and depend *only* on the total principal quantum number $N$. All allowed orbital angular momentum ($l$) states for a given $N$ share the exact same energy.

### 2. Square Wells & Woods-Saxon Potential (SO(3) Symmetry)
Real nuclei have relatively flat interiors and sharp (or slightly rounded) boundaries. We transition to an Infinite/Finite Square Well.
* **The Physics:** Flattening the bottom of the potential breaks the $SU(3)$ symmetry, but the nucleus is still a perfect sphere, preserving $SO(3)$ symmetry. 
* **The Effect (Centrifugal Relief):** High-$l$ states experience a strong centrifugal push outward. In the Harmonic Oscillator, this forced them to climb a steep wall (costing potential energy). In the flat-bottomed square well, they get an energy "discount" at the boundary, breaking the degeneracy and dropping their energy relative to lower-$l$ states.

### 3. Spin-Orbit Coupling (SU(2) Symmetry)
The final step to match experimental data is acknowledging that a nucleon's orbital angular momentum ($\vec{L}$) interacts strongly with its intrinsic spin ($\vec{S}$).
* **The Physics:** The Hamiltonian no longer commutes with $\vec{L}$ or $\vec{S}$ individually, but only with the total angular momentum $\vec{J} = \vec{L} + \vec{S}$. The symmetry collapses into the smaller $SU(2)$ group.
* **The Effect:** The unperturbed states undergo Clebsch-Gordan splitting into $j = l + 1/2$ and $j = l - 1/2$. Because the strong force coupling is negative, the higher $j$ state is driven violently downwards, creating the massive energy gaps and "intruder states" observed in real nuclei.

---

## Author
**Arnav Wadalkar**
*National Institute of Technology, Rourkela*
