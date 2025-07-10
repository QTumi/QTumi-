# ⚡ Quantum Optimization of Ghana’s Hydro Energy Network using QAOA

This project applies **Quantum Approximate Optimization Algorithm (QAOA)** to optimize the energy distribution across key hydro and township nodes in Ghana. Using the Max-Cut formulation, we model and solve an infrastructure planning problem that minimizes transmission costs by smartly partitioning the network.

---

## 📌 Problem Overview

Ghana’s energy grid has multiple generation points (hydro dams like **Akosombo**, **Bui**, and **Akuse**) and demand centers (townships like **Tema**, **Nima**, **Ashaiman**, and **Aboadze**). The goal is to:

> 🔋 **Partition the network** such that total weighted edge cut (representing transmission infrastructure cost) is maximized — which helps in identifying optimized energy flow channels.

This is mathematically equivalent to the **Max-Cut** problem on a weighted graph.

---

## 🧠 Methodology

### 1. Graph Construction
- Nodes represent **Hydro dams** and **Townships**
- Edges are weighted by estimated **distances** between nodes (used as proxy for infrastructure cost)

### 2. Max-Cut Formulation
- Problem encoded into a **Quadratic Program** using Qiskit’s `Maxcut` class
- Converted to **Ising Hamiltonian** for quantum optimization

### 3. QAOA Execution
- Utilizes `Qiskit`'s modern **Sampler-based QAOA**
- Solved using **COBYLA** optimizer
- Partition results interpreted using bitstrings from solution

### 4. Visualization
- Plots the partitioned graph using `networkx` and `matplotlib`
- Nodes colored by group and type (Hydro vs Town)

---

## 🧪 Technologies Used

- `Python 3.10+`
- `Qiskit`
- `NetworkX`
- `Matplotlib`
- `Pandas`

---

## 📊 Results

- Graph partitioned into two groups representing optimal infrastructure distribution
- Cut value (total distance of edges crossing the cut) calculated
- Visual graph output for easy interpretation

---

## 🧱 Project Structure

