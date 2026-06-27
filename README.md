# quantum-computing-examples

### 01 — Superposition & Measurement

Covers the most fundamental idea in quantum computing: superposition. A single Hadamard gate transforms |0⟩ into an equal superposition of |0⟩ and |1⟩, and the notebook explores what that actually means from two angles:

- **QASM Simulator** — Runs the circuit with measurement across 102,400 shots. The result is a near-perfect 50/50 split, showing how quantum randomness plays out statistically.
- **Statevector Simulator** — Skips measurement entirely and inspects the raw quantum state. Confirms the expected [1/√2, 1/√2] amplitudes and visualizes the state on a Bloch sphere (arrow pointing along +X).

Key takeaway: measurement collapses superposition into classical outcomes. Without it, you can see the full quantum state.

### 02 — Entanglement & Bell States

Builds on superposition by introducing multi-qubit systems and entanglement. Walks through the CNOT gate, then combines it with a Hadamard to create all four Bell states from scratch.

- **CNOT Gate** — Quantum conditional logic: flip the target only if the control is |1⟩. Demonstrated with classical inputs first, then with superposition to produce entanglement.
- **Bell State |Φ+⟩** — (|00⟩ + |11⟩) / √2. Measurement across 102,400 shots produces only `00` and `11`, never `01` or `10`.
- **Bloch Sphere Paradox** — Each qubit individually looks like a completely random mixed state (arrow at the origin). The information lives in the correlation, not the individual qubits.
- **All Four Bell States** — Φ+, Φ-, Ψ+, Ψ- built and measured side by side.
- **Multi-basis Verification** — Measures in both Z and X bases to confirm genuine entanglement, not just classical correlation.

Key takeaway: entanglement links qubits so measuring one instantly determines the other. The information is in the relationship, not the parts.

## Getting Started

### Run in Colab (Recommended)

Each notebook includes an "Open in Colab" badge. Click it and you're running in seconds with zero local setup.

### Run Locally

```bash
pip install qiskit qiskit-aer matplotlib pylatexenc
```

Then open any notebook with Jupyter:

```bash
jupyter notebook
```

## Prerequisites

No quantum physics background required. Each notebook explains concepts from the ground up. Familiarity with Python helps, but the code is straightforward and heavily commented.

## Roadmap

This project is a work in progress. More notebooks will be added covering topics such as:

- Quantum gates deep dive (X, Y, Z, phase gates, Toffoli)
- Multi-qubit circuits
- Quantum teleportation
- Basic quantum algorithms (Deutsch-Jozsa, Grover's, etc.)
- Noise models and error mitigation

## Tech Stack

- **Qiskit** — IBM's open-source quantum SDK
- **Qiskit Aer** — High-performance simulators (QASM, Statevector)
- **Matplotlib** — Histograms and Bloch sphere plots
- **Google Colab** — Zero-setup notebook environment
