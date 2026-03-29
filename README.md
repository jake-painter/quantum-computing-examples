# quantum-computing-examples

Hands-on notebooks exploring quantum computing concepts using [Qiskit](https://qiskit.org/) and the Aer simulator. Each notebook is self-contained, runnable in Google Colab, and built to make quantum intuitive through code and visualization.

## What's Here

### 01 — Superposition & Measurement

Covers the most fundamental idea in quantum computing: superposition. A single Hadamard gate transforms |0⟩ into an equal superposition of |0⟩ and |1⟩, and the notebook explores what that actually means from two angles:

- **QASM Simulator** — Runs the circuit with measurement across 102,400 shots. The result is a near-perfect 50/50 split, showing how quantum randomness plays out statistically.
- **Statevector Simulator** — Skips measurement entirely and inspects the raw quantum state. Confirms the expected [1/√2, 1/√2] amplitudes and visualizes the state on a Bloch sphere (arrow pointing along +X).

Key takeaway: measurement collapses superposition into classical outcomes. Without it, you can see the full quantum state.

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

- Entanglement and Bell states
- Quantum gates deep dive (X, Y, Z, CNOT, Toffoli)
- Multi-qubit circuits
- Quantum teleportation
- Basic quantum algorithms (Deutsch-Jozsa, Grover's, etc.)
- Noise models and error mitigation

## Tech Stack

- **Qiskit** — IBM's open-source quantum SDK
- **Qiskit Aer** — High-performance simulators (QASM, Statevector)
- **Matplotlib** — Histograms and Bloch sphere plots
- **Google Colab** — Zero-setup notebook environment

## License

MIT
