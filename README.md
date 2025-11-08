# Robust & Interpretable Phishing Detection using RF-PSO and LIME

This repository contains the implementation for a hybrid phishing detection system that combines a **Random Forest (RF)** classifier, optimized with **Particle Swarm Optimization (PSO)**, and explained using **LIME** for model interpretability.

##  Objective

To develop a robust, high-performance, and interpretable phishing detection system by integrating:
*   **Random Forest (RF)** for powerful classification.
*   **Particle Swarm Optimization (PSO)** for automated hyperparameter tuning.
*   **LIME (Local Interpretable Model-agnostic Explanations)** for providing transparent, human-readable explanations of model predictions.

##  Key of Contributions

*   **Hybrid RF-PSO Model:** Utilizes PSO to optimize RF hyperparameters (e.g., number of trees, max depth) without feature selection, preserving the integrity of all input features.
*   **Multi-Dataset Validation:** Rigorously evaluated on three distinct public phishing datasets (**Zieni, UCI, Mendeley**) to ensure generalization and robustness.
*   **Explainable AI (XAI):** Integrates LIME to demystify the "black box" model, providing clear insights into the features driving each prediction.
*   **Comprehensive Evaluation:** Performance assessed using a suite of eight metrics: Accuracy, Precision, Recall, F1-Score, Matthews Correlation Coefficient (MCC), ROC-AUC, and Training/Testing Time.

##  Methodology

1.  **Datasets:**
    *   **Zieni Dataset:** 10,000 samples, 74 features.
    *   **UCI Phishing Websites:** 11,055 samples, 30 features.
    *   **Mendeley Phishing Dataset:** 10,000 samples, 48 features.
    
    ** Dataset Source:** All datasets used in this study are available on Kaggle: [Multi-Dataset Phishing Collection](https://www.kaggle.com/datasets/yasserhessein/multi-dataset-phishing/data)

2.  **Preprocessing:** Handled byte-encoded labels, applied standardization, and used a 90:10 train-test split.
3.  **PSO Configuration:** 30 particles over 10 iterations to optimize 6 key RF hyperparameters.
4.  **Baseline Models:** Compared against Logistic Regression (LR), AdaBoost, Multi-layer Perceptron (MLP), Decision Tree (DT), standard Random Forest (RF), K-Nearest Neighbors (KNN), Support Vector Machine (SVM), and Stochastic Gradient Descent (SGD).

##  Results

The proposed **RF-PSO model** achieved state-of-the-art performance:

| Dataset        | Accuracy | ROC-AUC  |
|----------------|----------|----------|
| **Zieni**      | 90.30%   | 0.9653   |
| **UCI**        | 97.11%   | 0.9955   |
| **Mendeley**   | 98.70%   | 0.9989   |

The model consistently outperformed all baseline models in both accuracy and AUC, while maintaining reasonable computational time.

##  Explainability with LIME

LIME analysis identified the most critical features for distinguishing phishing from legitimate sites, enhancing trust and usability. Key influential features included:
*   `Feature_8`, `Feature_28` in the Zieni dataset.
*   `Feature_38` in the UCI dataset.
*   `Feature_41` in the Mendeley dataset.

##  Comparative Analysis

When compared with 10 recent studies, the proposed model stands out by:
*   Providing a **full suite of performance metrics**, not just accuracy.
*   Incorporating **model explainability** via LIME.
*   Demonstrating **excellent cross-dataset generalization**.
*   Showing **statistically significant performance gains** (validated by Wilcoxon test, p < 0.05).

##  Conclusion & Future Work

The **RF-PSO + LIME** framework provides an optimal balance between predictive accuracy, model interpretability, and computational efficiency for phishing detection.

**Future work will focus on:**
*   Integration with deep learning architectures (e.g., CNN, BiLSTM).
*   Expanding to multilingual and social media phishing detection.
*   Real-time deployment and testing for adversarial robustness.

---

#  Author

<div align="center">

** Dr. Yasir Hussein Shakir**  
*AI Research Scientist | Artificial intelligence*

>  **Note:** If you encounter any issues with this code, please don't hesitate to contact me.

##  Contact Information

<div align="center">

| Platform | Address | Badge |
|----------|---------|-------|
| **🏫 Uniten** | `pe20911@uniten.edu.my` | ![Academic](https://img.shields.io/badge/%F0%9F%93%A7_Academic-00A2FF?style=flat-square) |
| **📮 Yahoo** | `yasserhesseinshakir@yahoo.com` | ![Personal](https://img.shields.io/badge/%F0%9F%93%A8_Personal-720E9E?style=flat-square) |
| **📚 Google Scholar** | [`Yasir Hussein`](https://scholar.google.com/citations?user=37iNJq0AAAAJ&hl=en) | ![Scholar](https://img.shields.io/badge/%F0%9F%93%9A_Scholar-4285F4?style=flat-square) |
| **🏆 Kaggle** | [`yasserhessein`](https://www.kaggle.com/yasserhessein) | ![Competitions](https://img.shields.io/badge/%F0%9F%A5%87_Competitions-20BEFF?style=flat-square) |
| **💻 GitHub** | [`yasserhessein`](https://github.com/yasserhessein) | ![Code](https://img.shields.io/badge/%F0%9F%90%99_Code-181717?style=flat-square) |
| **💼 LinkedIn** | [`Yasir Hussein`](https://www.linkedin.com/in/yasir-hussein-314a65201/) | ![Professional](https://img.shields.io/badge/%F0%9F%91%94_Professional-0077B5?style=flat-square) |

</div>
