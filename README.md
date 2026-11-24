# Qrisp Workshop: Hamiltonian Simulation, Jasp and QEC Experiments

Slides and hands-on notebooks of a two-session workshop on [Eclipse Qrisp](https://qrisp.eu), the high-level quantum programming framework.
Each session is a 45-minute lecture followed by a hands-on coding session.

| Session | Lecture | Hands-on |
|---|---|---|
| **1** | [Qrisp and Hamiltonian Simulation](slides/session1_qrisp_and_hamiltonian_simulation.pdf): QuantumVariables, quantum types, memory management, quantum environments; Pauli, ladder and fermionic operators, molecules from PySCF, expectation values, Trotterization | [`session1_hands_on/`](session1_hands_on): from qubits to chemistry with the H₂ molecule. Stretch goal: the double-slit experiment |
| **2** | [Jasp and QEC Experiments](slides/session2_jasp_and_qec_experiments.pdf): tracing quantum programs, real-time classical feedback, one program with many interpreters, resource estimation; quantum error correction with the repetition code and `DetectorExperiment` | [`session2_hands_on/`](session2_hands_on): Chapter 1, thinking in Jasp; Chapter 2, a repetition-code memory experiment |

## Notebooks

| Notebook | Content | Time |
|---|---|---|
| `session1_hands_on/qrisp_chemistry_tutorial_exercises.ipynb` | Qrisp basics, H₂ from PySCF, Jordan–Wigner, Trotterization, expectation values, QITE vs. QPE resource estimation, with two small tasks | 45 min |
| `session1_hands_on/double_slit_exercises.ipynb` | Stretch goal: the double-slit experiment with `QuantumFloat`, automatic uncomputation, Grover's algorithm and the QFT | for fast participants |
| `session2_hands_on/ch1_jasp_exercises.ipynb` | Static vs. dynamic values, `control`, `jrange`, repeat-until-success; stretch: measurement-based uncomputation, boolean simulation, QPE resource estimation | about 20 min (core) |
| `session2_hands_on/ch2_repetition_code_exercises.ipynb` | Parity warm-up, one syndrome round, detectors across rounds, logical error rates with `DetectorExperiment` | about 22 min |

Every exercise ends with a check cell that prints ✅ or ❌ with a hint.
The `*_solutions.ipynb` notebooks contain the solutions and their outputs.

## Setup

Tested with Python 3.12:

```bash
pip install -r requirements.txt
jupyter lab
```

* **PySCF** does not install on native Windows. Use WSL, Linux, macOS or [Google Colab](https://colab.research.google.com); without PySCF the chemistry notebook falls back to a stored H₂ Hamiltonian.
* On Colab, uncomment the `%pip install` line in the first code cell of each notebook.
* Session 2, Chapter 2 needs `iqm-client[qrisp]` (it brings Stim and PyMatching). No access to quantum hardware is needed.

## Further reading

* Qrisp documentation and tutorials: [qrisp.eu](https://qrisp.eu)
* Jasp tutorial: [qrisp.eu/general/tutorial/Jasp.html](https://qrisp.eu/general/tutorial/Jasp.html)
* `DetectorExperiment` tutorial, including runs on IQM hardware: [docs.iqm.tech](https://docs.iqm.tech/iqm-client/user_guide_qrisp/detector_experiment_demo.html)
* Free access to IQM quantum computers (IQM Resonance Starter plan): [resonance.iqm.tech/signup](https://resonance.iqm.tech/signup)
* Questions: [GitHub](https://github.com/eclipse-qrisp/Qrisp) and the Qrisp Discord
