
## Final Project of the Qiskit 2020 Summer School

**Objective:** Simulate the ground state of the molecule Lithium Hydride (LiH) with the lowest energy and error. The goal is to complete the molecular simulation in the *fewest number of steps* and the *highest level of chemical accuracy*.

---

In this project, we design, implement, and simulate a Variational Quantum Eigensolver (VQE) algorithm for calculating the ground state energy of the LiH molecule. Each team member explores a different optimization path using the same base model. LiH is a 12-body molecule containing 4 protons, 4 electrons, and 4 neutrons. This creates a 12-body model, which becomes intractable when simulating it both with a classical and quantum computer. So, this model reduces the First Quantized Molecular Hamiltonian to one two-body interaction between two electrons in the hybridized p orbital and four one-body interactions with their respective nuclei.

Let's begin by describing the intermolecular forces of this molecule conceptually:

$$
\text{Molecular Hamiltonian} = - \sum \text{(Electron Kinetic Energy)} - \sum \text{(Nuclear Kinetic Energy)} - \sum \text{(Electron to Nuclear Coulombic Forces)} + \sum \text{(Electron to Electron Coulombic Forces)} + \sum \text{(Nuclear to Nuclear Coulombic Forces)}
$$

#### Electron Kinetic Energy

The kinetic energy of a single electron can be described using classical mechanics:

$$
\text{Electron Kinetic Energy} = \frac{1}{2} m v^{2}
$$

Where $ m $ is the mass of an electron and $ v $ is the velocity of an electron in meters per second.

$$
m = 9.10938356 \times 10^{-31} \, \text{kg}
$$
$$
v = \frac{\text{m}}{\text{s}}
$$

Quantum mechanics simplifies the calculation of the energy of particles with wave-particle duality (like electrons) by dividing the energy into components: translational, rotational, and vibrational energy. This is known as the Born-Oppenheimer approximation, a fundamental concept in the description of quantum states for molecules and atoms. We apply this approximation to the quantum states of qubits to estimate the electron's velocity, using qubits as a representational model of quantum mechanical interactions.

**Key Note:** Obtaining the precise velocity or position of an electron is impossible due to its small size. Hence, we estimate electron kinetic energy using qubits.

#### Nuclear Kinetic Energy

The kinetic energy of protons is described using classical mechanics:

$$
\text{Proton Kinetic Energy} = \frac{1}{2} m v^{2}
$$

Where $ m $ is the mass of a proton and $ v $ is the velocity of a proton in meters per second.

$$
m = 1.6726219 \times 10^{-27} \, \text{kg}
$$
$$
v = \frac{\text{m}}{\text{s}}
$$

**Key Note:** The nuclear kinetic energy of Lithium Hydride is negligible due to the size of the lithium nucleus. However, this property should not always be neglected, as some atoms, like Technetium, have significant nuclear kinetic energy. Technetium is the first element in the periodic table to emit a helium nucleus periodically, with a half-life of 4.21 million years, decaying into Niobium.

#### Electron to Nuclear Coulombic Force

...

#### Electron to Electron Coulombic Force

...

#### Nuclear to Nuclear Coulombic Force

...

#### First Quantized Molecular Hamiltonian

The First Quantized Molecular Hamiltonian for LiH can be described using the following vector calculus formula:

$$
\hat{H} = -\sum_{i=1}^{N}\frac{1}{2}\nabla_{i}^{2} - \sum_{A=1}^{M}\frac{1}{2M_{A}}\nabla_{A}^{2} - \sum_{i=1}^{N}\sum_{A=1}^{M}\frac{Z_{A}}{r_{iA}} + \sum_{j>i}\frac{1}{r_{ij}} + \sum_{B>A}\frac{Z_{A}Z_{B}}{R_{AB}}
$$

In this project, we design Variational Quantum Eigensolver (VQE) algorithms and compare their performance under different assumptions, including classical computed exact solutions and realistic device-specific noises.

When designing an algorithm for a quantum computer, many variables and choices depend on hardware specifications, so there is no one correct answer. The goal is to understand the different components of a VQE algorithm and showcase this understanding by comparing algorithm performance.

### The Project Team

- **Bektor Murzaliev**, The Netherlands
- **Peter Tunstall**, Denmark
- **Mostafa Atallah**, Egypt
- **Eduardo Pedicillio**, Italy
- **Rooney Muller**, Germany

