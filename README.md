# Hi, I'm Christian Schulz

**Heidelberg University** | **Algorithm Engineering Group** | **Amazon Scholar**

![C++](https://img.shields.io/badge/-C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MPI](https://img.shields.io/badge/-MPI-8B0000?style=flat-square&logo=openmpi&logoColor=white)
![OpenMP](https://img.shields.io/badge/-OpenMP-183A61?style=flat-square&logo=data:image/png;base64,&logoColor=white)
![CMake](https://img.shields.io/badge/-CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![pybind11](https://img.shields.io/badge/-pybind11-F7D44C?style=flat-square&logo=python&logoColor=black)
![Linux](https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![LaTeX](https://img.shields.io/badge/-LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
[![Website](https://img.shields.io/badge/-schulzchristian.github.io-FF5722?style=flat-square&logo=google-chrome&logoColor=white)](https://schulzchristian.github.io/)

> My group engineers high-performance C++ solvers for NP-hard combinatorial problems, then ships them as open source. We care about both theoretical quality guarantees and real-world speed.

---

## What We Work On

Our research sits at the intersection of algorithm theory and high-performance engineering. We attack NP-hard problems on graphs and hypergraphs through multilevel methods, evolutionary algorithms, data reduction, kernelization, local search, and parallelism.

### Graph & Hypergraph Decomposition

Splitting large graphs into balanced pieces while minimizing the edges cut between them. This is the foundation for parallel computing, VLSI design, route planning, and scientific simulations. Unified in the [**KaHIP**](https://github.com/KaHIP) org.

| Problem | Solver | What it does |
|---------|--------|-------------|
| Graph Partitioning | [**KaHIP**](https://github.com/KaHIP/KaHIP) | Multilevel k-way partitioning in Strong/Eco/Fast modes, evolutionary, distributed (ParHIP), edge partitioning, node ordering |
| Hypergraph Partitioning | [**KaHyPar**](https://github.com/kahypar/kahypar) | n-level hypergraph partitioning with direct k-way and recursive bisection |
| Parallel Hypergraph Part. | [**Mt-KaHyPar**](https://github.com/kahypar/mt-kahypar) | Multi-threaded hypergraph partitioning for massive instances |
| Parallel Partitioning | [**KaMinPar**](https://github.com/KaHIP/KaMinPar) | Shared-memory and distributed-memory parallel graph partitioning |
| Streaming Partitioning | [**HeiStream**](https://github.com/KaHIP/HeiStream) | Buffered streaming graph partitioning for graphs that don't fit in memory |
| Compressed Streaming | [**StreamCPI**](https://github.com/KaHIP/CompressedStreamingGraphPartitioning) | Memory-efficient streaming partitioning via run-length compression |
| Streaming Hypergraph Part. | [**FREIGHT**](https://github.com/KaHIP/FREIGHT) | Fast one-pass streaming hypergraph partitioning (**SEA 2023 Best Paper**) |

### Cuts & Clustering

Finding minimum cuts, maximum cuts, and natural communities in networks. Unified in the [**KaHIP**](https://github.com/KaHIP) org.

| Problem | Solver | What it does |
|---------|--------|-------------|
| Minimum Cut | [**VieCut**](https://github.com/KaHIP/VieCut) | Shared-memory parallel exact and inexact minimum cuts, cactus representations, multiterminal cuts |
| Maximum Cut | [**fpt-max-cut**](https://github.com/KaHIP/fpt-max-cut) | FPT kernelization + exact/heuristic solvers for max-cut |
| Hypergraph Min-Cut | [**HeiCut**](https://github.com/KaHIP/HeiCut) | Exact minimum cuts in hypergraphs using FPT kernelization |
| Connectivity Augmentation | [**HeiConnect**](https://github.com/HeiConnect/HeiConnect) | Algorithms for edge connectivity augmentation |
| Community Detection | [**VieClus**](https://github.com/KaHIP/VieClus) | Evolutionary modularity-maximizing graph clustering |
| Correlation Clustering | [**SCC**](https://github.com/KaHIP/ScalableCorrelationClustering) | Multilevel and memetic correlation clustering on signed graphs |
| Motif Clustering | [**HeidelbergMotifClustering**](https://github.com/KaHIP/HeidelbergMotifClustering) | Triangle-motif-based local clustering via flow/partitioning |
| Streaming Clustering | [**CluStRE**](https://github.com/KaHIP/CluStRE) | Streaming graph clustering with multi-stage refinement |

### Independence & Packing Problems

Finding the largest set of non-adjacent vertices, or the heaviest independent set, in a graph. Fundamental NP-hard problems with applications in scheduling, resource allocation, and network analysis. Unified in the [**KaMIS**](https://github.com/KarlsruheMIS) org.

| Problem | Solver | What it does |
|---------|--------|-------------|
| Maximum Independent Set | [**KaMIS**](https://github.com/KarlsruheMIS/KaMIS) | Branch-and-reduce, evolutionary, local search solvers for large sparse graphs |
| Max Weight Independent Set | [**CHILS**](https://github.com/KarlsruheMIS/CHILS) | Concurrent local search heuristic for MWIS |
| GNN-Guided Reductions | [**LearnAndReduce**](https://github.com/KarlsruheMIS/LearnAndReduce) | Graph neural network guided preprocessing for MWIS |
| Hypergraph Indep. Set | [**HyperMIS**](https://github.com/KarlsruheMIS/HyperMIS) | Kernelization + ILP for hypergraph independent sets |
| Hypergraph b-Matching | [**HeiHGM/Bmatching**](https://github.com/HeiHGM/Bmatching) | Solver for b-matching in hypergraphs using reductions, ILP, and local search |
| Streaming Hypergraph Matching | [**HeiHGM/Streaming**](https://github.com/HeiHGM/Streaming) | Streaming algorithms for hypergraph matching |
| 2-Packing Set | [**red2pack**](https://github.com/KarlsruheMIS/red2pack) | Branch-and-reduce solver for the 2-packing set problem |

### Dynamic Graph Algorithms

Maintaining solutions as graphs change over time, without recomputing from scratch. Unified in the [**DynGraphLab**](https://github.com/DynGraphLab) org.

| Problem | Solver | What it does |
|---------|--------|-------------|
| Dynamic Edge Orientation | [**DynDeltaOrientation**](https://github.com/DynGraphLab/DynDeltaOrientation) | Fully dynamic exact and heuristic delta-orientation |
| Dynamic Orient. Approx. | [**DynDeltaApprox**](https://github.com/DynGraphLab/DynDeltaApprox) | Dynamic edge orientation approximation algorithms |
| Dynamic Matching | [**DynMatch**](https://github.com/DynGraphLab/DynMatch) | Fully dynamic maximal matching algorithms |
| Dynamic Indep. Set | [**DynWMIS**](https://github.com/DynGraphLab/DynWMIS) | Fully dynamic maximum weight independent set |
| Dynamic Reachability | [**DynReach**](https://github.com/DynGraphLab/DynReach) | Fully dynamic reachability algorithms |

### Process Mapping & HPC

Mapping communication graphs of parallel applications onto processor topologies to minimize communication overhead. Unified in the [**KaHIP**](https://github.com/KaHIP) org.

| Problem | Solver | What it does |
|---------|--------|-------------|
| Process Mapping | [**VieM**](https://github.com/KaHIP/VieM) | Multilevel process mapping and sparse quadratic assignment |
| Shared-Memory Mapping | [**SharedMap**](https://github.com/KaHIP/SharedMap) | Parallel algorithm for hierarchical process mapping |
| Integrated Mapping | [**IntegratedProcessMapping**](https://github.com/KaHIP/IntegratedProcessMapping) | Multi-level integrated process mapping |
| Streaming Mapping | [**OnlineMultiSection**](https://github.com/KaHIP/OnlineMultiSection) | Streaming process mapping |

---

## The Unified Python Frontend

All of the above, accessible from Python with a single install:

```bash
pip install chszlablib
```

[**CHSZLabLib**](https://github.com/CHSZLab/CHSZLabLib) wraps 350k+ lines of C++ into a consistent Python API with zero-copy NumPy arrays. 26 algorithm modules, one `Graph` / `HyperGraph` interface. Designed to be usable by both humans and AI agents.

---

## Awards & Recognition

- **DIMACS Implementation Challenge Winner** (Graph Partitioning and Clustering)
- **PACE Challenge Winner** (Vertex Cover, 2019)
- **Best Paper Award**, IPDPS 2018 (Communication-free Massively Distributed Graph Generation)
- **Best Paper Award**, IEEE CLUSTER 2020 (Efficient Process-to-Node Mapping)
- **Best Paper Award**, SEA 2023 (FREIGHT: Fast Streaming Hypergraph Partitioning)
- **Heinz Billing Prize** and **KIT Doctoral Award**
- **120+ publications** across ACM, IEEE, SIAM
- **Steering Committee Chair**, SIAM ALENEX

---

## What I'm Doing

- **Leading the [Algorithm Engineering Group](https://ae.ifi.uni-heidelberg.de)** at Heidelberg University
- **Amazon Scholar** working on supply chain optimization
- **Shipping open source solvers** for NP-hard graph problems at scale
- **Bridging theory and practice**: quality guarantees that actually run fast

---
</details>

---

## Connect

[![Website](https://img.shields.io/badge/-schulzchristian.github.io-FF5722?style=flat-square&logo=google-chrome&logoColor=white)](https://schulzchristian.github.io/)
[![Google Scholar](https://img.shields.io/badge/-Google_Scholar-4285F4?style=flat-square&logo=google-scholar&logoColor=white)](https://scholar.google.de/citations?hl=de&user=SZ_vC90AAAAJ)
[![LinkedIn](https://img.shields.io/badge/-Christian_Schulz-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-schulz-/)
[![Email](https://img.shields.io/badge/-christian.schulz@uni--heidelberg.de-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:christian.schulz@informatik.uni-heidelberg.de)
[![GitHub](https://img.shields.io/badge/-Follow-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/schulzchristian)

---

> *"The goal is not just to prove that a fast algorithm exists, but to build one that people actually use."*
