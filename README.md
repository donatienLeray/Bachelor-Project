# Blockchain Consensus for Dynamic Robot Swarm Networks

This repository contains the implementation, report, and presentation for my bachelor project on blockchain-based consensus mechanisms in dynamic multi-robot systems. (2026-04)

## 📖 Overview

This project explores the use of blockchain consensus protocols in robot swarms, where decentralized agents must maintain a consistent global state under dynamic network conditions.

In addition to evaluating existing approaches such as Proof-of-Work (PoW) and Proof-of-Authority (PoA), this work introduces a novel consensus mechanism:

> **Connectivity-aware Proof-of-Authority (C-PoA)**

C-PoA prioritizes well-connected nodes for block production to improve block propagation and overall consensus efficiency in environments with intermittent communication and changing network topology.

---

## 🚀 Key Contributions

* Implementation of **C-PoA**, a connectivity-aware consensus mechanism
* Comparative evaluation with:

  * Proof-of-Work (PoW)
  * Proof-of-Authority (PoA)
  * Randomized PoA (R-PoA)
* Simulation-based analysis in a **robot swarm environment (ARGoS + Toychain)**
* Evaluation of:

  * Block propagation
  * Consensus efficiency
  * Fairness (block production inequality)

---

## 📊 Results Summary

* C-PoA shows **improved or comparable efficiency** compared to PoA
* Enables **faster global state updates** through better block propagation
* Connectivity-based selection reduces fork likelihood
* R-PoA suggests **controlled randomness can improve performance**
* A rare **deadlock issue** (⌊N/2⌋ + 1 constraint) was identified

---

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone --recurse-submodules https://github.com/donatienLeray/Bachelor-Project.git
cd Bachelor-Project
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

---

### 2. Requirements

* Python (for simulation scripts)
* ARGoS simulator
* Toychain framework (included as submodule)

> Exact setup may depend on your system and ARGoS installation.

---

### 3. Run experiments

```bash
cd toychain-argos/BachelorProjekt/
./run-experiment.sh  -r -s
```

---

### 3. Analyse results

by using the `toychain-argos/BachelorProjekt/results/plots.ipynb`

---

## 📄 Report & Presentation

* 📘 **Project Report**: available in `/report`
* 📊 **Presentation Slides**: available in `/presentation`

---

## 🔮 Future Work

* Resolve deadlock caused by ⌊N/2⌋ + 1 constraint
* Evaluate in more complex swarm tasks (e.g., exploration, mapping)
* Analyze robustness against adversarial behavior
* Investigate relaxing the fairness constraint
* Further validate results with statistically significant experiments

---

## 📚 References

This project builds on:

* [Toychain framework](https://github.com/teksander/toychain)
* [ARGoS robot simulator](https://www.argos-sim.info/)
* Existing research on blockchain in swarm robotics (See report)

---

## 🙏 Acknowledgments

I would like to thank:

- **[Andreagiovanni Reina](https://www.giovannireina.com/index.php)** for supervising this project and providing valuable guidance.
- **[Alexandre Melo Pacheco](https://www.researchgate.net/profile/Alexandre-Pacheco-7)** for his support, feedback, and helpful discussions. 

