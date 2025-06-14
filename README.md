**Molecular docking** is the process of identifying the optimal binding configuration between a **ligand** (typically a drug-like molecule) and the **active site** of a **protein**. This interaction can either inhibit or activate certain protein functions, making it highly relevant for therapeutic applications. However, determining the optimal configuration is computationally challenging due to the vast number of possible spatial conformations.

In the [*Molecular Docking via DC-QAOA* tutorial](https://nvidia.github.io/cuda-quantum/latest/applications/python/digitized_counterdiabatic_qaoa.html) provided by NVIDIA CUDA-Q, the authors use a variant of the **Quantum Approximate Optimization Algorithm (QAOA)** called **DC-QAOA** — where "DC" stands for **Digitized-Counterdiabatic** — to address this problem. Their implementation is based on the paper [*Molecular Docking via Quantum Approximate Optimization Algorithm*](https://arxiv.org/pdf/2308.04098).

Separately, in the preprint [*Quantum Computing for Optimizing Aircraft Loading*](https://arxiv.org/abs/2504.01567), another quantum optimization algorithm is proposed: the **Multi-Angle Layered Variational Quantum Eigensolver (MAL-VQE)**. This approach is structurally similar to DC-QAOA, but according to the authors, it can achieve better results compared to standard QAOA.

This notebook explores the application of the **MAL-VQE algorithm** to the **molecular docking** problem.

The workflow is as follows:
1. Reproduce the DC-QAOA implementation from the NVIDIA CUDA-Q tutorial.
2. Adapt the method to implement MAL-VQE for comparison.
