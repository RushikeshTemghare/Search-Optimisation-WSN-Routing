# 🔍 Search & Optimisation — Wireless Sensor Network Routing

## Multiple-Objective Routing Path Optimisation (COMP7065) — MSc Research Project

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Algorithms](https://img.shields.io/badge/Algorithms-Dijkstra%20|%20ACO%20|%20GA-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📌 Project Overview

This project was developed as part of the **MSc Data Science & Artificial Intelligence**
coursework for the **Search and Optimisation (COMP7065)** module at Bournemouth University.

The project addresses a real-world **multiple-objective optimisation problem** for Wireless
Sensor Networks (WSNs) deployed in the New Forest, England. Hundreds of wireless sensors
collect environmental data and must find optimal routing paths to base stations at
**Beaulieu (5000, -5000)** and **Lyndhurst (-5000, 5000)**.

---

## 📂 Repository Structure

Search-Optimisation-WSN-Routing/
│
├── report/
│   └── Search_&Optimisation_Report.pdf
│
├── code/
│   └── Search&_Optimisation_Code.ipynb
│
├── poster/
│   └── Individual_Poster_Rushikesh_Temghare.pdf
│
├── LICENSE
└── README.md

---

## 🎯 Problem Statement

Each wireless sensor node must find an optimal routing path to a base station while
simultaneously optimising two conflicting objectives:

| Objective | Description |
|---|---|
| **Minimise Latency** | Sum of all delays across links (30ms per link) |
| **Maximise Transmission Rate** | Minimum transmission rate along the path |

### Constraints
- ❌ No communication if distance between nodes exceeds **3000m**
- ✅ All routing paths must end at one of the two base stations
- 📡 Transmission rate determined by distance between nodes

### Transmission Rate Table

| Distance | Transmission Rate |
|---|---|
| d >= 3000m | 0 Mbps (No connection) |
| 2500m - 3000m | 1 Mbps |
| 2000m - 2500m | 2 Mbps |
| 1500m - 2000m | 3 Mbps |
| 1000m - 1500m | 4 Mbps |
| 500m - 1000m | 5 Mbps |
| d < 500m | 7 Mbps |

---

## 🤖 Optimisation Algorithms Implemented

### 1. 🗺️ Dijkstra's Algorithm
- Deterministic shortest path algorithm
- Guarantees minimum latency path
- Best for static networks
- Fastest execution time

### 2. 🐜 Ant Colony Optimisation (ACO)
- Bio-inspired metaheuristic algorithm
- Simulates ant foraging behaviour using pheromone trails
- Highly adaptable for dynamic networks
- Also implemented an **Optimised ACO** version using parallel processing

### 3. 🧬 Genetic Algorithm (GA)
- Evolutionary optimisation approach
- Uses selection, crossover and mutation operators
- Best average transmission rate performance
- Balances multiple objectives effectively

---

## 📊 Results & Evaluation

### Performance Comparison

| Metric | Dijkstra | ACO | Optimised ACO | GA |
|---|---|---|---|---|
| **Execution Time (s)** | 2.307 | 2457.451 | 1151.921 | 102.541 |
| **Avg Transmission Rate (Mbps)** | 1.47 | 1.39 | 1.31 | 2.05 |
| **Adaptability** | Limited | High | High | Moderate |
| **Computational Cost** | Low | High | Moderate | Moderate |

### Key Findings
- ✅ **Dijkstra** — fastest execution, best for latency-critical static networks
- ✅ **ACO** — most adaptable, but highest computational cost
- ✅ **Optimised ACO** — halved execution time while maintaining adaptability
- ✅ **GA** — best average transmission rate at 2.05 Mbps, most versatile

---

## 🛠️ Technologies Used

- **Python 3.8+**
- **NumPy** — Matrix operations and distance calculations
- **Pandas** — Dataset management
- **Matplotlib** — Path visualisation
- **NetworkX** — Graph representation
- **SciPy** — Euclidean distance calculations
- **Multiprocessing** — Parallel ACO optimisation

---

## 🖼️ Individual Poster

An individual research poster was produced summarising:
- Problem definition and objectives
- Dijkstra's Algorithm implementation
- Performance comparison results
- Conclusions and future scope

Available in the `poster/` folder.

---

## 🔮 Future Scope

- 🔋 **Energy-aware routing** — protocols to extend network lifespan
- 🔄 **Dynamic adaptability** — handling node mobility and interference
- 🤖 **AI/ML integration** — enhanced routing decisions
- 🔗 **Hybrid approaches** — combining Dijkstra efficiency with ACO/GA adaptability

---

## 👤 Author

**Rushikesh Temghare**
MSc Data Science & Artificial Intelligence
Bournemouth University

---

## 📄 License

This project is licensed under the MIT License.
