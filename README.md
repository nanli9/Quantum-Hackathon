# Quantum Simulation of the LiH Ground State Energy

This project leverages **quantum computing**, specifically the **Variational Quantum Eigensolver (VQE)** algorithm, to calculate the ground state energy of the Lithium Hydride (LiH) molecule.  
The primary goal is to generate the molecule's **Potential Energy Surface (PES)** by simulating the bond energy at various interatomic distances.  
From this, we determine key chemical properties such as **equilibrium bond length** and **bond strength**.

The simulation is implemented using the **modern, primitives-based Qiskit framework**, showcasing a current and efficient approach to quantum chemistry problems.

---

## 🔬 Key Features
- **Ground State Calculation**: Utilizes the VQE algorithm to find the lowest energy state of the LiH molecule.  
- **Potential Energy Surface (PES)**: Calculates the bond energy across a range of interatomic distances to plot the PES curve.  
- **Chemical Property Analysis**: Determines equilibrium bond length and bond dissociation energy.  
- **Electron Density Visualization**: 3D visualization of the electron density cloud at the optimal bond length (via `py3Dmol`).  
- **Modern Qiskit Implementation**: Built with the latest **Qiskit Nature** and **Primitives (Estimator)** workflow.  
- **Benchmarking**: Compares VQE results against a **classical NumPyMinimumEigensolver** to validate accuracy.  

---

## 🧪 Scientific Background

### Potential Energy Surface (PES)
The **PES** describes the energy of a molecule as a function of its geometry.  
For a diatomic molecule like **LiH**, the PES is a 2D curve: **total energy vs. atomic separation**.  

- The **lowest point** corresponds to the most stable configuration.  
- The **x-coordinate** is the equilibrium bond length.  
- The **well depth** gives the bond energy.  

### Variational Quantum Eigensolver (VQE)
VQE is a **hybrid quantum-classical algorithm** to find the lowest eigenvalue of a Hamiltonian (the molecular ground state energy).  

1. **Ansatz**: A parameterized quantum circuit (e.g., `EfficientSU2`) prepares a trial wavefunction.  
2. **Quantum Step**: The circuit is run on a quantum computer/simulator to measure the energy.  
3. **Classical Step**: An optimizer (e.g., SPSA, COBYLA) updates the circuit parameters to minimize energy.  
4. This loop continues until the **ground state energy** is reached.  

---

## 🛠️ Technologies Used
- Python 3.8+  
- [Qiskit](https://qiskit.org/) – Core quantum computing framework  
- [qiskit-nature](https://qiskit.org/ecosystem/nature/) – Quantum chemistry tools  
- [qiskit-aer](https://qiskit.org/documentation/apidoc/aer.html) – High-performance simulators  
- [PySCF](https://pyscf.org/) – Classical chemistry driver  
- NumPy – Numerical computations  
- Matplotlib – PES curve plotting  
- py3Dmol – Interactive 3D electron density visualization  

---

## 🚀 Setup and Installation

```bash
git clone https://github.com/nanli9/Quantum-Hackathon.git
cd Quantum-Hackathon
pip install -r requirements.txt
jupyter notebook simulatingLiH.ipynb  

