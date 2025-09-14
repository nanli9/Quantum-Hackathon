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
jupyter notebook simulatingCH4.ipynb  
```

## Results
Methane (CH4) ground state simulation graph: 

<img width="413" height="276" alt="image" src="https://github.com/user-attachments/assets/af7e44ed-393a-4d2b-b28a-ae6896b71c3f" />

Low bond distance simulation:

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/59abc31d-d141-42e0-9854-18fc9498df45" />

Appropriate bond distance simulation:

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/713ecd2b-fcd8-4072-8b32-a7ad878822e0" />

Very large bond distance simulation (makes the individual exist atoms apart):

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/cce351fe-b230-412d-8d8c-38d825f9ce92" />

Highest Occupied Molecular Orbital (HOMO) and Lowest Unoccupied Molecular Orbital (LOMO) for CH4:

<img width="300" height="200" alt="image" src="https://github.com/user-attachments/assets/bb957b83-3996-4263-b8ec-d11d0f32a86b" />




LiH ground state simulation graph:


<img width="413" height="276" alt="image" src="https://github.com/user-attachments/assets/3506a191-b4fa-42de-a417-497452b05dd9" />


