## Quantum Billiards (Numerical Solver)
**File:** `2DSE_Solver.ipynb`

### The Problem
The particle-in-a-box is a standard undergraduate problem, but what happens when the "box" isn't a simple square? This project implements a **Finite Difference** solver to find the energy eigenstates of a particle confined in arbitrary geometries (Circles, Stadiums, etc.).

### Computational Methodology
The notebook builds the Hamiltonian matrix from scratch using grid discretization:

1.  **The Grid:** We create a discrete $N \times N$ lattice to represent continuous space.
2.  **The Kinetic Energy:** We construct the Laplacian operator $\nabla^2$ using a sparse matrix representation of the Central Finite Difference method.
3.  **The Geometry (Penalty Method):** instead of complicated boundary conditions, we use a "mask."
    * Inside the shape: $V(x,y) = 0$
    * Outside the shape: $V(x,y) = 10^{10}$ (effectively infinite)
    * This forces the wavefunction to vanish at the boundaries naturally.
4.  **The Solver:** We use `scipy.sparse.linalg.eigsh` to find the lowest $k$ eigenvalues (energy levels) and eigenvectors (wavefunctions).

### Visual Results
The code produces visualizations of the probability density $|\psi|^2$.

* **Symmetry:** In the circle and square, you will see clean geometric symmetries.
* **Quantum Chaos:** In the **Bunimovich Stadium** shape, you may observe "Quantum Scars"—places where the probability density concentrates along unstable classical periodic orbits.
