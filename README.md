# 🏭 SmartFactory — Industrial Analytics & DSA Platform

[![Java](https://img.shields.io/badge/Java-25%20LTS-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-22c55e?style=for-the-badge&logo=github)](https://sriram743.github.io/SmartFactory/)
[![DSA](https://img.shields.io/badge/Algorithms-CO--1%20to%20CO--6-06b6d4?style=for-the-badge)](https://github.com/SriRam743/SmartFactory)
[![Dataset](https://img.shields.io/badge/Dataset-10%2C050%20Records-f59e0b?style=for-the-badge)](https://github.com/SriRam743/SmartFactory/tree/main/dataset)

> **Live Deployed Web Application & Demo:**  
> 👉 [https://sriram743.github.io/SmartFactory/](https://sriram743.github.io/SmartFactory/)

---

## 📌 Project Overview

**SmartFactory** is an end-to-end industrial IoT and manufacturing analytics platform built in Java. It processes **10,050 real-time telemetry records** from 10 factory machines, diagnosing thermal overshoots, vibration anomalies, and rotational degradation while solving complex industrial optimization problems using advanced Data Structures & Algorithms (DSA).

The project is structured around 6 comprehensive Course Outcomes (**CO-1 through CO-6**), accompanied by an interactive **34-option console application** and a **live-deployed web dashboard**.

---

## 🌐 Live Deployment Link (For Teachers / Evaluators)

- **Interactive Web Demo:** [https://sriram743.github.io/SmartFactory/](https://sriram743.github.io/SmartFactory/)
- **GitHub Repository:** [https://github.com/SriRam743/SmartFactory](https://github.com/SriRam743/SmartFactory)

---

## 🎯 Course Outcomes (CO) & Algorithm Mapping

| Outcome | Focus Area | Implemented Algorithms | Real-World Smart Factory Use Case |
| :--- | :--- | :--- | :--- |
| **CO-1** | **Pattern Searching** | • Knuth-Morris-Pratt (KMP)<br>• Z-Algorithm<br>• Rabin-Karp (Rolling Hash)<br>• Aho-Corasick Automaton | Searching for error signatures, vibration alerts, and specific machine IDs across massive log streams in $O(N+M)$ time. |
| **CO-2** | **Suffix Structures & Indexing** | • Suffix Array<br>• SA-IS Linear Suffix Sorter<br>• Kasai LCP Array<br>• Suffix Tree<br>• Suffix Automaton | Rapid indexing of past maintenance logs; identifying recurring maintenance phrases and cyclical sensor fault sequences. |
| **CO-3** | **Dynamic Programming & Heuristics** | • Levenshtein Distance<br>• Damerau-Levenshtein<br>• Weighted Edit Distance<br>• Matrix-Chain Multiplication DP<br>• Bitmask DP Machine Selection<br>• Subset DP Resource Allocation | Automatic correction of manual operator typos; minimizing latency in multi-stage product assembly batches. |
| **CO-4** | **Network Flow & Bottlenecks** | • Ford-Fulkerson Method<br>• Edmonds-Karp Algorithm<br>• Dinic’s Blocking Flow<br>• Bipartite Matching<br>• Max-Flow Min-Cut Theorem | Maximizing raw-material pipeline throughput; assigning operators to compatible machines; identifying bottleneck piping conduits. |
| **CO-5** | **NP-Completeness & Approximation** | • 3-SAT Solver (DPLL)<br>• 3-SAT $\rightarrow$ CLIQUE Reduction<br>• CLIQUE $\rightarrow$ Independent Set $\rightarrow$ Vertex Cover<br>• 2-Approximation Vertex Cover | Resolving conflicting machine schedules and power-draw safety constraints; selecting minimum safety sensor checkpoints. |
| **CO-6** | **Randomized & Parallel Algorithms** | • Randomized QuickSort<br>• Miller-Rabin Primality Test<br>• Reservoir Sampling<br>• Blelloch Parallel Scan<br>• Parallel Tree Reduce<br>• Brent's Theorem Speedup Model | Prioritizing urgent work orders; generating cryptographic tokens for machine auth; computing cumulative energy consumption across parallel cores. |

---

## 📊 Dataset Specifications

The project includes an industrial sensor dataset (`dataset/smart_factory_datset.csv`) containing:
- **Total Records:** 10,050
- **Machines Tracked:** 10 units (`M-01` through `M-10`)
- **Normal Operations:** 9,721 records (96.73%)
- **Fault Incidents:** 329 records (3.27%)
- **Key Metrics:** Temperature (°C), Vibration (mm/s), RPM, Pressure (bar), Power Consumption (kW)

---

## 📁 Repository Structure

```
smartfactory/
│
├── dataset/
│   └── smart_factory_datset.csv        # 10,050 industrial telemetry records
│
├── src/
│   ├── app/
│   │   └── SmartFactoryApp.java        # Interactive 34-option CLI platform
│   ├── data/
│   │   └── FactoryDataLoader.java      # CSV streaming & parsing engine
│   ├── factory/
│   │   ├── FactorySearchManager.java   # KMP, Z-Function pattern matching
│   │   ├── FaultDetection.java         # Aho-Corasick multi-fault detection
│   │   ├── MachineSearch.java          # Machine ID lookups
│   │   └── MaintenancePatternFinder.java
│   ├── flow/
│   │   ├── BipartiteMatching.java      # Worker-machine assignment
│   │   ├── DinicAlgorithm.java         # Dinic O(V²E) max flow
│   │   ├── EdmondsKarp.java            # BFS-based flow augmentation
│   │   ├── FordFulkerson.java          # Basic augmenting paths
│   │   ├── MinCutBottleneckFinder.java # Min-cut bottleneck cutset identification
│   │   └── ProductionFlowManager.java
│   ├── model/
│   │   ├── FactoryRecord.java          # POJO for machine telemetry
│   │   ├── Machine.java
│   │   ├── Inventory.java
│   │   └── Production.java
│   ├── np/
│   │   ├── ConflictGraphReduction.java # CLIQUE to Vertex Cover reduction
│   │   ├── ConstraintReduction.java    # 3-SAT to CLIQUE reduction
│   │   ├── ProductionConstraintManager.java
│   │   ├── SATConstraintSolver.java    # DPLL solver
│   │   └── VertexCoverApproximation.java # 2-approximation algorithm
│   ├── optimization/
│   │   ├── DataEntryCorrection.java    # Typo correction DP
│   │   ├── MachineSelection.java       # Bitmask DP
│   │   ├── ProcessingOrderOptimizer.java # Matrix chain multiplication
│   │   └── ResourceCombinationPlanner.java # Subset DP
│   ├── parallel/
│   │   ├── BlellochScan.java           # Work-efficient parallel scan
│   │   ├── BrentsTheoremAnalyzer.java  # Theoretical speedup bounds
│   │   ├── MillerRabinPrimality.java   # Randomized token verification
│   │   ├── ParallelReduce.java         # Parallel tree reduction
│   │   ├── RandomizedQuickSort.java    # Work order priority ranking
│   │   └── ReservoirSampling.java      # Real-time stream telemetry sampling
│   └── reports/
│       ├── FastReportSearch.java       # Suffix automaton
│       ├── LargeReportIndexer.java     # SA-IS linear suffix sort
│       ├── RepeatedIssueFinder.java    # Kasai LCP longest repeated substrings
│       └── ReportIndexer.java          # Suffix Array
│
├── index.html                          # Deployed interactive web dashboard (GitHub Pages)
├── .gitignore
├── .classpath
├── .project
└── README.md
```

---

## 💻 How to Run the Java Console Platform

### Prerequisites
- Java JDK 17 or higher (tested with JDK 25)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/SriRam743/SmartFactory.git
   cd SmartFactory
   ```

2. **Compile all Java packages:**
   ```bash
   javac -d bin -sourcepath src src/app/SmartFactoryApp.java
   ```

3. **Run the application:**
   ```bash
   java -cp bin app.SmartFactoryApp
   ```

4. **Select any option from the menu (1 to 34):**
   - Option `1`: Factory Dashboard (Dataset overview & telemetry summary)
   - Options `3`–`6`: CO-1 Pattern Search (KMP, Z-Algorithm, Rabin-Karp, Aho-Corasick)
   - Options `7`–`11`: CO-2 Suffix Structures (Suffix Array, SA-IS, LCP Kasai)
   - Options `12`–`17`: CO-3 Dynamic Programming (Levenshtein, Matrix Chain, Bitmask DP)
   - Options `18`–`22`: CO-4 Network Flow (Ford-Fulkerson, Edmonds-Karp, Dinic, Min-Cut)
   - Options `23`–`26`: CO-5 NP-Completeness (3-SAT DPLL, Reductions, 2-Approx Vertex Cover)
   - Options `27`–`32`: CO-6 Randomized & Parallel (QuickSort, Miller-Rabin, Blelloch Scan)
   - Option `34`: Exit

---

## ⏱️ Algorithmic Complexity Reference

| Module | Algorithm | Time Complexity | Space Complexity |
| :--- | :--- | :--- | :--- |
| **CO-1** | KMP String Matching | $O(N + M)$ | $O(M)$ |
| **CO-1** | Z-Algorithm | $O(N + M)$ | $O(N + M)$ |
| **CO-1** | Rabin-Karp | $O(N + M)$ average | $O(1)$ |
| **CO-1** | Aho-Corasick | $O(N + \sum M_i + Z)$ | $O(\sum M_i \cdot \Sigma)$ |
| **CO-2** | SA-IS Linear Suffix Sort | $O(N)$ | $O(N)$ |
| **CO-2** | Kasai LCP Algorithm | $O(N)$ | $O(N)$ |
| **CO-3** | Levenshtein Edit Distance | $O(M \cdot N)$ | $O(M \cdot N)$ or $O(\min(M, N))$ |
| **CO-3** | Matrix Chain Multiplication | $O(N^3)$ | $O(N^2)$ |
| **CO-3** | Bitmask DP Machine Selection | $O(N^2 \cdot 2^N)$ | $O(N \cdot 2^N)$ |
| **CO-4** | Edmonds-Karp Max Flow | $O(V \cdot E^2)$ | $O(V + E)$ |
| **CO-4** | Dinic’s Blocking Flow | $O(V^2 \cdot E)$ | $O(V + E)$ |
| **CO-4** | Hopcroft-Karp / Bipartite Match | $O(E \sqrt{V})$ | $O(V + E)$ |
| **CO-5** | 3-SAT DPLL Solver | $O(2^V)$ worst-case | $O(V)$ recursion |
| **CO-5** | Vertex Cover 2-Approximation | $O(V + E)$ | $O(V)$ |
| **CO-6** | Randomized QuickSort | $O(N \log N)$ expected | $O(\log N)$ stack |
| **CO-6** | Miller-Rabin Primality | $O(k \log^3 N)$ | $O(1)$ |
| **CO-6** | Blelloch Parallel Scan | $O(N)$ Work, $O(\log N)$ Span | $O(N)$ |

---

## 👨‍💻 Author Information

- **Student Name:** Sri Ram
- **GitHub:** [@SriRam743](https://github.com/SriRam743)
- **Institution:** KL University
