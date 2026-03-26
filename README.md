# GSoC 2026: ML4SCI
## Specific Task 2: Discovery of Hidden Symmetries and Conservation Laws

![Organization](https://img.shields.io/badge/Organization-ML4SCI-blue)
![Program](https://img.shields.io/badge/Program-GSoC_2026-orange)
![Status](https://img.shields.io/badge/Status-Test_Submission-success)

This repository contains the test submission for the Google Summer of Code (GSoC) 2026 project **"Discovery of hidden symmetries and conservation laws"** under the **Machine Learning for Science (ML4SCI)** umbrella.

## 📌 Project Overview

Recent successes in the domain of unsupervised and semi-supervised learning have advanced the development of Physics-Aware and Symmetry-Aware Machine Learning techniques. This project focuses on developing models that learn the symmetries of a dataset as a meta-task, inherently learning the underlying physics.

This repository implements the full evaluation criteria required for the test, extensively covering:
- **Task 1: Dataset Preparation & Latent Space Creation**
- **Task 2: Supervised Symmetry Discovery**
- **Task 3: Unsupervised Symmetry Discovery** (Logit-preserving topological mapping)
- **Bonus Task: Rotation Invariant Network Design**

---

## 📂 Repository Structure & Methodological Differences

To robustly address the prompt's encouragement to "explore different approaches," the solution is bifurcated into two distinct computational notebooks. Each explores a valid, advanced technique for resolving symmetry bounds in neural networks:

```text
.
├── ML4SI_Test_2_X.ipynb    # Implementation X: Cycle-Consistent Continuous Geometry
├── ML4SI_Test_2_Y.ipynb    # Implementation Y: Explicit Algebraic Constraint Imposition
└── README.md               # Project documentation (this file)
```

### 🧠 Difference in Implementations (X vs. Y)

While both notebooks successfully execute the four tasks and yield accurate translation matrices mapped across the $z \\in \\mathbb{R}^8$ latent space, their core philosophies for **Task 3 (Unsupervised Discovery)** and the **Bonus Task (Invariant Classifier)** differ substantially.

#### **Notebook X (The Organic Cycle-Consistency Approach)**
- **Methodology:** Unconstrained generation via Neural Networks (`Generators`). 
- **Mechanism:** Notebook X relies on the framework presented in *"Discovery of physics from data: universal laws and discrepancies"*. It utilizes parameterized multi-layer perceptrons acting as topological generators. By strictly enforcing a cycle-consistency geometric loss across the full unstructured 8-dimensional representation, the network organically **"discovers"** the optimal symmetry mapping—which manifests as $SO(2)$ rotation—completely autonomously.
- **Advantage:** Highly scalable to unknown, uncharacterized symmetries in complex physics data where the strict underlying mathematical mapping is completely unknown.

#### **Notebook Y (The Algebraic Structural Constraint Approach)**
- **Methodology:** Explicit $SO(2)$ subspace rotation boundary mapping.
- **Mechanism:** Notebook Y adopts an explicitly structured rigid approach. Rather than relying purely on cycle-loss optimizations to organically generate the geometry, the 8-dimensional space is rigorously partitioned ($\mathbb{R}^6 \\times \mathbb{R}^2$). A textbook 2D mathematical rotation operator (an analytic rotation matrix using precise sine and cosine terms) is explicitly applied to the decoupled $\mathbb{R}^2$ rotational subspace.
- **Advantage:** Provides absolute, mathematically perfect invariance and deterministic boundaries. Because the topological bounds strictly obey the textbook definitions, rotation-prediction mappings suffer zero computational drift.

---

## 🛠️ Technologies & Requirements

This evaluation pipeline relies heavily on the standard physics deep learning stack:
- **Languages:** Python 3.8+ 
- **Deep Learning Formats:** PyTorch, TorchVision
- **Data Engineering:** NumPy, SciPy, Matplotlib

---

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd ML4SCI_Test_2
   ```

2. **Install dependencies:**
   Ensure you have a modern Python tensor environment initialized. 
   ```bash
   pip install torch torchvision numpy matplotlib scikit-learn tqdm jupyter
   ```

3. **Launch the Evaluation Notebooks:**
   ```bash
   jupyter notebook
   ```
   Execute the cells iteratively to evaluate the $SO(2)$ metrics across the VAE architectures.

---

## 📚 References

The neural topological logic, structural formulations, and generalized models synthesized in this repository are rigorously influenced by:
1. **[Paper 1]** *Discovery of physics from data: universal laws and discrepancies* - [arXiv:2109.09721](https://arxiv.org/abs/2109.09721)
2. **[Paper 2]** *Machine-learning hidden symmetries* - [arXiv:2301.05638](https://arxiv.org/abs/2301.05638)
3. **[Paper 3]** *Learning representations by maximizing symmetry* - [arXiv:2302.00236](https://arxiv.org/abs/2302.00236)

---

**Mentors:**
Diptarko Choudhury (NISER) | Sergei Gleyzer (University of Alabama) | Ruchi Chudasama (University of Alabama) | Samuel Campbell (University of Alabama) | Emanuele Usai (University of Alabama) | Alex Roman (University of Alabama)

*Submitted as part of the GSoC 2026 ML4SCI candidate evaluation.*
