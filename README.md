# Paktron-Version-6.0.0
# 🚀 PKTron Quantum HPC & SDK Simulator

### Top Quantum Computing Framework in Asia & South Asia | Global Top 5 by Feature Breadth

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Downloads](https://img.shields.io/badge/Downloads-10K+-brightgreen.svg)
![GPU](https://img.shields.io/badge/GPU-CUDA%20Supported-orange.svg)
![MPI](https://img.shields.io/badge/MPI-Distributed-red.svg)
![HPC](https://img.shields.io/badge/HPC-Ready-purple.svg)

---

## 🌟 Overview

**PKTron v6.0.0** is a unified **Quantum Computing + High Performance Computing (HPC) + Software Development Kit (SDK)** platform designed to provide researchers, engineers, educators, and industry teams with a complete quantum ecosystem in a single package.

With over **10,000 downloads on PyPI**, PKTron delivers one of the most extensive collections of quantum simulation, quantum algorithms, quantum chemistry, quantum machine learning, quantum cryptography, error correction, and HPC acceleration capabilities available in an open-source framework.

```bash
pip install pktron
```

One installation gives access to:

✅ 13 Quantum Simulators

✅ 50+ Quantum Algorithms

✅ Full HPC Runtime

✅ Quantum Chemistry Suite

✅ Quantum Machine Learning Stack

✅ Error Correction & Mitigation

✅ Quantum Cryptography Framework

✅ Finance & Defense Industry Modules

✅ GPU & MPI Distributed Execution

✅ Qiskit, Cirq, PennyLane Interoperability

---

# ⚡ Why PKTron?

PKTron combines the functionality of multiple quantum software ecosystems into a single framework.

### Included Technologies

| Category          | Capability                                      |
| ----------------- | ----------------------------------------------- |
| Simulators        | 13 Backend Types                                |
| Algorithms        | 50+ Quantum Algorithms                          |
| QML               | 10+ Quantum AI Models                           |
| Quantum Chemistry | UCCSD, ADAPT-VQE, Molecular Hamiltonians        |
| Error Correction  | 6 Full Quantum Error-Correcting Codes           |
| Error Mitigation  | 9+ Mitigation Techniques                        |
| QKD               | 6 Quantum Cryptography Protocols                |
| HPC               | AVX-512, OpenMP, CUDA, MPI                      |
| Tensor Networks   | MPS, PEPS, MERA, DMRG                           |
| Industry Modules  | Finance & Defense                               |
| Interoperability  | Qiskit, Cirq, PennyLane, OpenQASM, Quil, Braket |

---

# 🚀 Installation

### Standard Installation

```bash
pip install pktron
```

### GPU Acceleration

```bash
pip install pktron[gpu]
```

---

# ⚡ Quick Start

## Bell State

```python
import pktron as pk

qc = pk.QuantumCircuit(2)

qc.h(0)
qc.cx(0,1)

result = pk.StatevectorSimulator().run(qc, shots=1024)

print(result["counts"])
```

Expected:

```python
{'00': ~512, '11': ~512}
```

---

## One-Line Execution

```python
import pktron as pk

qc = pk.QuantumCircuit(2)

qc.h(0)
qc.cx(0,1)

print(pk.execute(qc, shots=1024))
```

---

## Grover Search

```python
import pktron as pk

grover = pk.GroverSearch(
    n_qubits=4,
    marked_states=[5,10]
)

result = grover.run()

print(result["found"])
```

---

## Variational Quantum Eigensolver (VQE)

```python
import pktron as pk

H = pk.QuantumChemistry.h2_hamiltonian(
    distance=0.735
)

result = pk.VQE(H).run(
    ansatz_depth=2,
    max_iter=200
)

print(result["energy"])
```

---

## E91 Quantum Key Distribution

```python
import pktron as pk

result = pk.E91Protocol.run(
    n_pairs=2048,
    eavesdrop=False
)

print(result["chsh_s"])
```

---

# 🆕 What's New in v6.0.0

### New Features

| Feature                 | Description                                          |
| ----------------------- | ---------------------------------------------------- |
| Pauli Class             | Symplectic representation with full algebra          |
| SparsePauliOp           | Promoted to top-level API                            |
| E91Protocol             | Entanglement-based QKD with CHSH security testing    |
| M3MeasurementMitigation | Matrix-free readout mitigation                       |
| DMRGSolver              | Added to tensor network namespace                    |
| MPS Fix                 | Corrected SVD implementation for entangling circuits |

---

# 🖥 Quantum Simulation Backends

PKTron includes 13 major simulator engines:

* Statevector Simulator
* Density Matrix Simulator
* MPS Simulator
* Clifford Simulator
* Extended Stabilizer Simulator
* Superoperator Simulator
* Quantum Trajectory Simulator
* Pulse-Level Simulator
* Tensor Network Simulator
* PEPS Simulator
* MERA Simulator
* Multi-GPU Simulator
* Distributed MPI Simulator

Specialized Engines:

* Matchgate Simulator
* Fermionic Gaussian Simulator
* Adaptive MPS Simulator

---

# 🧠 Quantum Algorithms

### Search & Optimization

* Grover Search
* Amplitude Amplification
* Quantum Counting
* QAOA
* Quantum Annealing

### Number Theory

* Shor's Algorithm

### Function Problems

* Deutsch-Jozsa
* Simon's Algorithm

### Phase Estimation

* Quantum Phase Estimation
* Quantum Fourier Transform

### Linear Algebra

* HHL Algorithm

### Advanced Algorithms

* Quantum Metropolis
* Quantum SDP
* LCU Framework
* Adiabatic Optimization
* GRAPE Quantum Optimal Control
* Quantum NAS
* Quantum Error Learning

Total: **50+ Algorithms**

---

# ⚛ Quantum Chemistry

PKTron includes a complete quantum chemistry stack.

### Supported Molecules

* H₂
* N₂
* CH₄
* CO₂
* NH₃
* C₂H₄

### Supported Methods

* VQE
* UCCSD
* ADAPT-VQE
* Jordan-Wigner
* Bravyi-Kitaev
* Parity Mapping
* Active Space Reduction
* Freeze Core Reduction

---

# 🤖 Quantum Machine Learning

### Included Models

* Quantum Neural Networks
* Quantum CNN
* QSVM
* Quantum GAN
* Quantum Autoencoder
* Quantum Boltzmann Machine
* Quantum Reinforcement Learning
* Quantum Federated Learning
* Quantum Transfer Learning

Advanced Models:

* BarrenPlateauFreeQNN
* Quantum Kernel Trainer
* Quantum Meta Learner

---

# 🛡 Quantum Error Correction

Supported Quantum Error Correcting Codes:

* Steane [[7,1,3]]
* Surface Code
* Bacon-Shor Code
* Color Code
* Repetition Code
* Heavy-Hex Code

Supported Decoders:

* MWPM Decoder
* PyMatching Decoder
* Threshold Estimation

---

# 📉 Error Mitigation

Included mitigation techniques:

* Zero Noise Extrapolation (ZNE)
* Probabilistic Error Cancellation (PEC)
* Clifford Data Regression (CDR)
* M3 Measurement Mitigation
* Dynamical Decoupling
* Symmetry Verification
* Virtual Distillation
* Pauli Twirling
* Clifford Twirling

---

# 🔐 Quantum Cryptography

Supported protocols:

* BB84
* E91
* B92
* Twin-Field QKD
* MDI-QKD
* Device Independent QKD

Additional technologies:

* Blind Quantum Computing
* Quantum Digital Signatures
* Quantum Secret Sharing
* Quantum Money
* Post-Quantum Cryptography

---

# 💰 Finance Applications

* Portfolio Optimization
* Quantum Monte Carlo
* Quantum Credit Risk
* Quantum Option Pricing
* Value at Risk (VaR)
* Expected Shortfall (ES)

---

# 🎯 Defense Applications

* Vehicle Routing Optimization
* Mission Scheduling
* Quantum Swarm Optimization
* Quantum Target Detection
* Quantum Cryptanalysis
* Quantum Game Theory

---

# ⚡ High Performance Computing

### CPU Acceleration

* AVX-512
* AVX2
* SSE
* OpenMP

### GPU Acceleration

* CUDA
* CuPy
* Raw Kernels

### Distributed Computing

* MPI Runtime
* Multi-GPU Execution
* Async Task Scheduling

### Additional HPC Features

* Circuit Cache
* Tensor Network Kernels
* Circuit Fusion
* Kernel Scheduler

---

# 🔄 Interoperability

PKTron works with:

* Qiskit
* Cirq
* PennyLane
* OpenQASM 2.0
* OpenQASM 3.0
* Quil
* Amazon Braket
* IonQ

---

# 📊 Framework Comparison

| Feature                | PKTron | Typical Framework |
| ---------------------- | ------ | ----------------- |
| Simulator Backends     | 13     | 3–5               |
| Quantum Algorithms     | 50+    | 10–20             |
| QML Models             | 13     | 2–4               |
| Error Correction Codes | 6      | 1–2               |
| Error Mitigation       | 9+     | 1–2               |
| QKD Protocols          | 6      | 1                 |
| Finance Module         | ✅      | ❌                 |
| Defense Module         | ✅      | ❌                 |
| HPC Kernel             | ✅      | Rare              |
| GPU Backend            | ✅      | Limited           |
| MPI Runtime            | ✅      | Rare              |
| Tensor Networks        | ✅      | Limited           |
| Open Source            | ✅ MIT  | Mixed             |

---

# 🏛 Organization

Developed and maintained by:

**CETQAC — Centre of Excellence for Technology, Quantum & AI**

Canada 🇨🇦 | Pakistan 🇵🇰

---

# 📈 Project Statistics

* 10,000+ Downloads
* 150+ Classes
* 26 Functions
* 39 Submodules
* 13 Simulators
* 50+ Algorithms
* 10+ QML Models
* 6 QEC Codes
* 9+ Error Mitigation Methods

---

# 🤝 Contributing

Contributions are welcome.

```bash
git clone https://github.com/yourusername/pktron
cd pktron
pip install -e .
```

Please submit pull requests, bug reports, and feature requests through GitHub Issues.

---

# 📜 License

MIT License

Copyright © 2024–2026 CETQAC

---

## ⭐ Star the Repository

If PKTron helps your research, teaching, or development work, please consider giving the repository a star.

**Building the Future of Quantum Computing from Canada & Pakistan.**
