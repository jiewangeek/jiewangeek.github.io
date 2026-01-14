<center>
     <h1>Jie Wang</h1>
     <div>
         <span>
             <img src="assets/phone-solid.svg" width="18px">
             WeChat: jiewang7657
         </span>
         ·
         <span>
             <img src="assets/envelope-solid.svg" width="18px">
             Email: jiewangeek@163.com
         </span>
         ·
         <span>
             <img src="assets/rss-solid.svg" width="18px">
             <a href="https://scholar.google.com/citations?user=YTeQmzEAAAAJ&hl=en">Academic Publications</a>
         </span>
     </div>
</center>

## <img src="assets/info-circle-solid.svg" width="30px"> Personal Information 

 - Gender: Female
 - Career Focus: Compilation/Performance Optimization, AI Infra, Program Analysis
 - Preferred Location: Beijing
 - Current Employer: Huawei

## <img src="assets/graduation-cap-solid.svg" width="30px"> Education

- **Postdoctorate**, Peking University / Alibaba Joint Program, Computer Software and Theory, 2018.12 ~ 2020.12
- **Ph.D. / Master**, Institute of Software, Chinese Academy of Sciences (ISCAS), Computer Software and Theory, 2012.9 ~ 2018.6
- **Bachelor**, Jilin University, Computer Science and Technology, GPA (Top 3% / 370 students), 2008.9 ~ 2012.6
- **English**: CET-6

## <img src="assets/briefcase-solid.svg" width="30px"> Work Experience

- **2022.5 ~ Present, Huawei, Technical Expert in Program Analysis**
 
- **2018.7 ~ 2022.5, Ant Group, Data Technology - Distributed Computing Dept, Technical Expert**

## <img src="assets/project-diagram-solid.svg" width="30px"> Project Experience
  
- **Compilation/Operator Development DSL - DSL & Compilation Optimization [In Progress]**
  
  1. Adaptation and hardware-affinity optimization for DSL ecosystems like Triton, Gluon, and Tilelang. Tasks include: triton-like tile op design for domain-specific hardware, automatic pipelining, synchronization insertion, etc.
  2. Computation-Communication Overlap: Development and optimization of computation-communication overlap operators.
   
- **Compilation/AI Performance Optimization - Operator Tuning Tools**
  
  With the explosion of Large Language Models (LLMs), hardware requirements have escalated, making software-level operator acceleration critical. Operator optimization involves iterative adjustments of tiling parameters, pipeline scheduling, data layout, computation order, and overlap, often taking weeks or even months. We conduct automated tuning in the following areas:

  1. **Parameter Tuning**: Given specific parameters, automatically search for the optimal combination. Methods include Genetic Algorithm (GA) search and offline performance modeling. Achieved 30%+ performance gains for 10+ typical commercial operators.
  2. **Compiler-based Deep Tuning**: Explored two methods for migration to new hardware: (1) **Micro-kernel (DietCode)**: Kernel computation is typically split into blocks for concurrent execution. This method defines a universal block size space; performance modeling includes $f_m$ (predicting single block performance, shape-independent) and $f_{adapt}$ (linear combination of blocks for kernel performance, shape-dependent). This reduces tuning time via shared universal blocks. (2) **Super-optimization (Mirage)**: Proposed a multi-layer graph abstraction (Kernel, Block, Thread layers) for CUDA programming to automatically search for equivalent logic, fusion, and tiling parameters.

- **AI/LLM Application - Sliding Window RAG for Code Completion**
  
  *LLM, RAG, SFT, Prompting*

  Reproduced the iterative RAG scheme from the RepoCoder paper for code continuation scenarios. Improved code completion accuracy for C/Java/Rust by 10%. Observations: 1. ~34% of direct LLM generations are correct (skipping RAG saves overhead). 2. ~10% of cases worsen with RAG. We proposed a lightweight method training a small model to selectively perform RAG, improving line completion efficiency by 21%-46% and API completion by 14%-40%. [Paper published]

- **AI/LLM Application - Similar Code Retrieval & HPC Application Optimization (2023)**

   *Code Clone, LLM, Embedding, GNN, Subgraph Matching, Code Property Graph*

  Addressed code retrieval challenges where LLM embeddings are insensitive to variable renaming or statement reordering. 1. Used program analysis to extract structural semantics (Data/Control dependencies) represented as DAGs. 2. Implemented GNN-based subgraph matching (e.g., SimGNN) on DAGs. Achieved 98%+ accuracy for thousand-line HPC code within 1s.

- **Program Analysis/Symbolic Execution - C Language Memory Defect Checking (2023)**

  *Memory Defects, Code Security, C Language, Static Analysis, CSA, Symbolic Execution*

  Developed resource management defect detection based on Clang Static Analyzer (CSA). Supports 10+ resource-related issues (leaks, UAF, double-free, etc.) with cross-file analysis at compilation unit granularity. Improved analysis speed using value range strategies.

- **Program Analysis/Parallelization Framework - Parallel Pointer Analysis for C (2022)**

  *Pointer Analysis, C Language, Andersen Algorithm*

  Explored a parallel framework for program analysis using graph computing to handle exponential complexity. Partitioned graph algorithms into subgraphs with inter-node communication for computational scalability and used out-of-core/distributed graph databases for storage scalability.
  
- **Program Analysis/Call Graph - Performance-Accuracy Balanced Callgraph for C (2022)**
  
  *Callgraph, MLTA, SVF*
    
  Traditional Andersen-based SVF tools are accurate but slow, while MLTA is fast but imprecise for 10M-100M line systems. This project overlaid use-def analysis on MLTA to achieve a balance between performance and accuracy.
  
- **Program Analysis/Data Flow Analysis: Taint Analysis for Large-scale Java (2020)**

  *Static Data Flow, Java/Soot, IFDS, On-demand Analysis, Sparse Value Flow*
  
  Developed an (online) taint analysis/data lineage platform to track how key data fields propagate across thousands of microservices at Ant Group. Currently applied in change defense, fund reconciliation, and full-stack data link construction. Published 1 CCF-A paper (FSE'20, 1st Author) and 2 patents.

- **Compilation/Auto-Vectorization - Dataframe Program Compilation Optimization (2022)**

  *Python, JIT, Vectorization/Parallelization, Numba, Dataframe*
  
  Developed a Python JIT tool where users add a `@jit` annotation to optimize code. Compiles Python to high-performance machine code and automatically parallelizes logic (e.g., for-loops) into multi-threaded code. Applied to distributed Dataframe scenarios, achieving ~5x performance improvement.

- **Compilation/Performance Optimization - GC & Performance Tools for Ray (2019)**

  *Distributed Engine, Dynamic Dataflow, Ray, GC, Scheduling, Peephole Optimization*
  
  Optimized Ray's object management and performance. Used static analysis to obtain task dependencies and automatically optimized specific patterns via instrumentation. Proposed a lightweight, fault-tolerant distributed GC scheme based on reference counting.

- **Program Analysis/Fault Diagnosis - Log-based Root Cause Localization (2021)**
  
  *Distributed System RCA, Log-based, DSL*

  Developed a rule-based fault localization method defining a DSL to describe failure characteristics (e.g., fault recovery, distributed GC). Designed for high expressiveness, ease of use, and scalability. 1 Patent published.

- **Program Analysis/Error Detection - Node.js Concurrency Bug Detection (2017)**

  *JavaScript, Concurrency, Atomicity Violation, Event-driven*

  Conducted an empirical study on JS concurrency bugs, finding atomicity violations account for 65%. Designed a "happens-before" relationship for Node.js and established atomicity violation patterns. Outperformed Node.fz in efficiency and bug discovery. 2 papers published (ASE'17, ICSE'19).

- **Program Analysis/Fault Reproduction - Javascript Record & Replay Tool (2015)**

  *JavaScript, Fault Reproduction, Record/Replay, Program Slicing, Dynamic Analysis*
  
  Developed JSTrace to remove error-irrelevant events from logs to enable fast reproduction. Used dynamic program slicing based on runtime data dependencies. 3 papers published (ISSRE'15, JSS'18, ICST'18).

## Publication List
<a href="https://scholar.google.com/citations?user=YTeQmzEAAAAJ&hl=en">Google Scholar</a>
- C Wang, et al. *EVOC2RUST: A Skeleton-guided Framework for Project-Level C-to-Rust Translation* (ICSE SEIP 2026, CCF A).
- Wenrui Zhang, et al., **Jie Wang***. *A Lightweight Framework for Adaptive Retrieval In Code Completion With Critique Model*.
- Dong Chen, et al., **Jie Wang**, et al. *Coder: Issue resolving with multi-agent and task graphs*.
- **Jie Wang**, et al. *Combating the Problem of Indirection in Distributed Dynamic Dataflow* (Ant Group, Technical Report).
- **Jie Wang**, et al. *Scaling static taint analysis to industrial SOA applications: a case study at Alibaba* (FSE 2020, CCF A).
- Xiaoning Chang, et al., **Jie Wang**, et al. *Detecting atomicity violations for event-driven Node.js applications* (ICSE 2019, CCF A).
- **Jie Wang**, et al. *A Comprehensive Study on Real World Concurrency Bugs in Node.js* (ASE 2017, CCF A).
- **Jie Wang**. *Characterizing and Taming Non-deterministic Bugs in JavaScript Applications* (ASE 2017-Doctoral Symposium).
- **Jie Wang**. *Constraint-based Event Trace Reduction* (FSE 2016-SRC).
- **Jie Wang**, et al. *JSTrace: Fast Reproducing Web Application Errors* (JSS, CCF B).
- **Jie Wang**, et al. *Fast Reproducing Web Application Errors* (ISSRE 2015, CCF B).
- **Jie Wang**, et al. *Context-Based Event Trace Reduction in Client-Side JavaScript Applications* (ICST 2018, CCF C).

## Honors & Awards

- 2024, Inner Source Gold Badge Project
- 2024, Outstanding Sub-committee Project
- 2023, Outstanding Coach * 2
- 2023, President's Award
- 2022, Outstanding Coach
- 2022, Golden Network Award
- 2020, Ant Group Annual "Golden Key" (Innovation Award)
- 2017, National Scholarship for Doctoral Students, CAS
- 2016, Merit Student Pacesetter, UCAS
- 2013-2016, Merit Student, UCAS
- 2013-2014, Outstanding Student Cadre, UCAS
- 2012, Outstanding Intern Scholarship, ISCAS
- 2009-2012, National Encouragement Scholarship, Jilin University
