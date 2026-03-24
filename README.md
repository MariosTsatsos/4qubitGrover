# Grover's Algorithm — 4 Qubits

Jupyter notebook implementation of Grover's quantum search algorithm for a 4-qubit register, marking the state |0010⟩.

---

## Notebooks

| Notebook | Description |
|---|---|
| [`Grovers_algo-4_qubits.ipynb`](Grovers_algo-4_qubits.ipynb) | Original (2020) — Qiskit 0.x, includes live IBM Q hardware run on `ibmq_essex` |
| [`Grovers_algo-4_qubits_qiskit1x.ipynb`](Grovers_algo-4_qubits_qiskit1x.ipynb) | Refactored for **Qiskit 1.x** — updated APIs, rich explanations, simulator-ready |

---

## What it covers

- **Theory** — oracle construction, Grover diffuser, iteration count derivation ($k = \lfloor\pi/4 \cdot \sqrt{N}\rfloor = 3$ for $N=16$)
- **`n_controlled_Z`** — explicit decomposition of the multi-controlled Z gate for 1, 2, and 3 controls using the phase-gate ladder ($T$-gate decomposition of Toffoli)
- **Simulation** — AerSimulator run showing ~96% success probability on the marked state
- **Legacy hardware section** — original IBM Q cells preserved with migration notes

---

## Qiskit 1.x migration notes

| Old (0.x) | New (1.x) |
|---|---|
| `from qiskit import BasicAer` | `from qiskit_aer import AerSimulator` |
| `execute(circuit, backend, shots=N)` | `backend.run(transpile(circuit, backend), shots=N)` |
| `circuit.cu1(θ, a, b)` | `circuit.cp(θ, a, b)` |
| `from qiskit import IBMQ` | `from qiskit_ibm_runtime import QiskitRuntimeService` |
| `from qiskit.tools.monitor import job_monitor` | Removed — use `job.status()` |

---

## Requirements

```bash
pip install qiskit qiskit-aer matplotlib
```

For running on real IBM hardware (optional):

```bash
pip install qiskit-ibm-runtime
```

---

## Reference

Figgatt et al. — [Complete 3-Qubit Grover Search on a Programmable Quantum Computer](http://www.diva-portal.org/smash/get/diva2:1214481/FULLTEXT01.pdf)
