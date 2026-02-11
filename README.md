# QACO_implementation

Implementation (in Jupyter notebooks) of a hybrid quantum-classical Ant Colony Optimization (QACO) approach for NP-hard combinatorial optimization, using the Quadratic Assignment Problem (QAP) as a benchmark. The implementation follows the "implementable" QACO framework by Garcia de Andoin and Echanobe.

## Overview

- Classical ACO baseline for QAP.
- Hybrid QACO variants (unconstrained, constrained, and parameter studies).
- Optional IBM Quantum runtime experiments.

The quantum part is used as an exploration mechanism for sampling candidate solutions. Evaluation and pheromone updates remain classical.

## Repository structure

- `ACO_algorithm/` - Classical ACO baseline notebook.
- `QACO_algorithm/` - QACO notebooks (simulation and IBM runtime).
- `Trial_matrices/` - QAP instances used in experiments (.csv and .txt).

## Notebooks

### ACO baseline

- `ACO_algorithm/ACO_unconstrained.ipynb` - Classical ACO for QAP.

### QACO simulation

- `QACO_algorithm/QACO_unconstrained.ipynb` - QACO unconstrained variant.
- `QACO_algorithm/QACO_constrained.ipynb` - QACO with constrained exploration.
- `QACO_algorithm/QACO_unconstrained_BETAparametric.ipynb` - Parameter study over beta.

### IBM Quantum runtime

- `QACO_algorithm/QC_implementation/QACO_IBM_unconstrained.ipynb` - QACO on IBM runtime.
- `QACO_algorithm/QC_implementation/Real_Transpilation_for_IBMrun.ipynb` - Transpilation and runtime workflow details.

## Quick start

### 1) Clone

```bash
git clone https://github.com/QuantumAlbe/QACO_implementation.git
cd QACO_implementation
```

### 2) Create an environment

Use any Python environment you prefer (venv, conda). For example:

```bash
python -m venv .venv
```

### 3) Install dependencies

The notebooks rely on standard scientific Python packages and Qiskit. Install only what you need for the notebooks you plan to run.

Core packages:

```bash
pip install numpy pandas matplotlib
```

Qiskit simulation (QACO notebooks):

```bash
pip install qiskit qiskit-aer
```

IBM Quantum runtime (optional):

```bash
pip install qiskit-ibm-runtime qiskit-ibm-transpiler qiskit-ibm-catalog
```

### 4) Run notebooks

Open a notebook in Jupyter or VS Code and run cells top-to-bottom. Adjust QAP instance files and experiment parameters in the first configuration cells.

## Data

Trial matrices are stored in `Trial_matrices/` as both .csv and .txt. The notebooks typically load these as QAP instances; update the file path in the configuration cell if you want to switch instances.

## IBM Quantum notes (optional)

IBM runtime notebooks require valid credentials. Follow IBM Quantum setup instructions and set your API token before running.

## Citation

If you use this work, please cite the QACO framework by Garcia de Andoin and Echanobe, and reference this repository.
