# QACO_implementation

# QACO_implementation

Implementation (in Jupyter notebooks) of a **hybrid quantum–classical Ant Colony Optimization** approach for solving **NP-hard combinatorial optimization**, with the **Quadratic Assignment Problem (QAP)** as a reference benchmark, following the “implementable” QACO framework by Garcia de Andoin & Echanobe. :contentReference[oaicite:2]{index=2}

> **Goal of this repository**
> - Provide a readable, runnable implementation of:
>   1) a **classical ACO baseline** for QAP  
>   2) a **hybrid quantum–classical QACO** variant (unconstrained + constrained exploration ideas)  
> - Enable repeated experiments (e.g., 200–1000 runs) and collect **mean fitness** / statistics.

---

## Background (short)

### Quadratic Assignment Problem (QAP)
QAP is a classic **NP-hard** assignment problem where the objective involves **pairwise (quadratic) interaction costs** between assigned facilities/locations. It quickly becomes intractable to solve exactly as the size grows, making metaheuristics (like ACO) attractive. :contentReference[oaicite:3]{index=3}

### Classical ACO in one paragraph
Ant Colony Optimization (ACO) is a bio-inspired metaheuristic: candidate solutions are sampled probabilistically using “pheromone” information that is iteratively reinforced according to solution quality. ACO is approximate by design: it trades guaranteed optimality for practicality on hard problems. :contentReference[oaicite:4]{index=4}

### Why “hybrid quantum” here?
This project does **not** claim that quantum computers “solve NP-hard problems efficiently.” Instead, the quantum component is used as an **exploration mechanism** (sampling new candidate solutions), while evaluation and update steps remain classical. The target is a practical NISQ-style hybrid workflow. :contentReference[oaicite:5]{index=5}

---

## Repository structure

The repository is organized into three main folders: :contentReference[oaicite:6]{index=6}

- `ACO_algorithm/`  
  Classical baseline ACO implementation and experiments (QAP).

- `QACO_algorithm/`  
  Hybrid quantum–classical QACO notebooks (simulation and/or IBM execution).

- `Trial_matrices/`  
  Input instances / trial matrices used to test QAP.

---

## Quick start

### 1) Clone
```bash
git clone https://github.com/QuantumAlbe/QACO_implementation.git
cd QACO_implementation