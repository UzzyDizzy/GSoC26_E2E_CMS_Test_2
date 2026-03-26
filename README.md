# GSoC 2026: ML4SCI - Discovery of Hidden Symmetries and Conservation Laws

![Organization](https://img.shields.io/badge/Organization-ML4SCI-blue)
![Program](https://img.shields.io/badge/Program-GSoC_2026-orange)
![Status](https://img.shields.io/badge/Status-Test_Submission-success)

This repository contains the test submission for the Google Summer of Code (GSoC) 2026 project **"Discovery of hidden symmetries and conservation laws"** under the **Machine Learning for Science (ML4SCI)** umbrella organization.

## 📌 Project Overview

Recent successes in the domain of unsupervised and semi-supervised learning have advanced the development of Physics-Aware and Symmetry-Aware Machine Learning techniques. This project focuses on developing models that learn the symmetries of a dataset as a meta-task, inherently learning the underlying physics.

While standard particle physics symmetries are well-defined in 4-vector or 4-momenta bases, they can become elusive and difficult to work with following representation changes. This project aims to utilize machine learning techniques to uncover the representation of given symmetries via conserved quantities in abstract spaces. These physics-aware operations yield neural networks that are mathematically invariant to these symmetries—making them more robust, stable, interpretable, and data-efficient.

### 🎯 Objectives
- **Symmetry Discovery:** Develop a deep learning model capable of uncovering the symmetries present in toy datasets and extending them to abstract use cases.
- **Phase Space Probing:** Use the identified symmetries to probe the phase space of CMS (Compact Muon Solenoid) datasets.
- **Physics-Aware Modeling:** Build specialized physics-aware neural networks utilizing these symmetries.
- **Benchmarking:** Compare the developed models against previous works in terms of data efficiency and invariance with respect to symmetry operations.

---

## 📂 Repository Structure

```text
.
├── ML4SI_Test_2_X.ipynb    # Jupyter notebook containing exploratory symmetry models and initial tests
├── ML4SI_Test_2_Y.ipynb    # Jupyter notebook containing phase space probing and CMS dataset evaluations
└── README.md               # Project documentation (this file)
```

*(Note: The provided Jupyter notebooks include comprehensive implementations covering data preprocessing, symmetry extraction, physics-aware constraints, and corresponding model evaluation.)*

---

## 🧠 Methodology & Approach

The methodology implemented in this test builds strictly upon theoretical backgrounds from recent literature to establish frameworks capable of identifying abstract invariant spaces.

1. **Transformation to Abstract Space**: We analyze kinematic variables by applying representational shifts, testing the model's ability to locate hidden symmetries without explicitly formulating them beforehand.
2. **Conserved Quantity Extraction**: Formulating loss functions and network architectures that reward the preservation of physical constraints, functioning as an unsupervised discovery mechanism.
3. **Application to CMS Datasets**: The discovered symmetry representations are incorporated back into practical high-energy physics data mappings to demonstrate data-efficient learning.
4. **Metric Evaluation**: Neural network invariance is tested directly against algebraic symmetry operations, measuring resilience and stability.

---

## 🛠️ Technologies & Requirements

This test submission relies on standard deep learning and structural toolkits:
- **Languages:** Python 3.8+ (Proficiency in C++ implicitly applies to underlying frameworks)
- **Deep Learning:** PyTorch / TensorFlow 
- **Data Science Stack:** NumPy, SciPy, Matplotlib, pandas

---

## 🚀 How to Run locally

1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd ML4SCI_Test_2
   ```

2. **Install dependencies:**
   Ensure you have a working Python environment. You can install all standard packages via `pip`:
   ```bash
   pip install torch tensorflow numpy pandas matplotlib jupyter
   ```

3. **Launch the Jupyter Notebooks:**
   ```bash
   jupyter notebook
   ```
   Open `ML4SI_Test_2_X.ipynb` and `ML4SI_Test_2_Y.ipynb` to view the code, read through the mathematical processes, and run the training / evaluation cells.

---

## 📚 References

The theories and mathematical formulations implemented in this repository are deeply influenced by the following literature:
1. **[Paper 1]** *Discovery of physics from data: universal laws and discrepancies* - [arXiv:2109.09721](https://arxiv.org/abs/2109.09721)
2. **[Paper 2]** *Machine-learning hidden symmetries* - [arXiv:2301.05638](https://arxiv.org/abs/2301.05638)
3. **[Paper 3]** *Learning representations by maximizing symmetry* - [arXiv:2302.00236](https://arxiv.org/abs/2302.00236)

---

**Mentors:**
Diptarko Choudhury (NISER) | Sergei Gleyzer (University of Alabama) | Ruchi Chudasama (University of Alabama) | Samuel Campbell (University of Alabama) | Emanuele Usai (University of Alabama) | Alex Roman (University of Alabama)

*Submitted as part of the GSoC 2026 application process.*
