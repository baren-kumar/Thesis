Here is a professional **GitHub README** for your thesis project.

---

# Physics-Informed Explainable Deep Learning for Mechanical Property and Ply-Wise Failure Prediction of UD CFRP Laminates

## Project Overview

This repository contains the implementation of a **Physics-Informed Neural Network (PINN)** for predicting the mechanical behavior and failure characteristics of **Unidirectional Carbon Fiber Reinforced Polymer (UD CFRP) laminates**. The framework combines finite element simulation data, physics-based constraints, and explainable artificial intelligence (XAI) to improve prediction accuracy and model interpretability.

The project integrates:

* Physics-Informed Neural Networks (PINNs)
* Classical Laminate Theory (CLT)
* Orthotropic Elasticity
* Generalized Hooke's Law
* Deep SHAP Explainability
* TensorFlow Deep Learning
* ANSYS Simulation Dataset

---

# Dataset Description

The dataset used in this project is generated from **ANSYS Composite PrepPost (ACP)** simulations of UD CFRP laminates under static loading conditions.

### Input Features

| Feature               | Description                   |
| --------------------- | ----------------------------- |
| Fiber Volume Fraction | Fiber reinforcement ratio     |
| Fabric Thickness      | Laminate thickness            |
| Ply 1–6 Angle         | Fiber orientation of each ply |
| Force X Component     | Applied tensile load (N)      |
| E1, E2, E3            | Orthotropic Young's Modulus   |
| G12, G23, G31         | Shear Modulus                 |
| ν12, ν13, ν23         | Poisson's Ratios              |

### Output Targets

* Total Deformation Maximum (mm)
* Equivalent Stress Maximum (MPa)
* Equivalent Elastic Strain Maximum
* Inverse Reserve Factor (IRF)

---

# Physics Constraints

The PINN incorporates multiple physical laws during training:

* Generalized Hooke's Law
* Orthotropic Elastic Constitutive Equation
* Classical Laminate Theory (CLT)
* Strain Energy Constraint
* Failure Constraint using Inverse Reserve Factor

The total loss function combines data loss with physics-based residual losses.
**Total Loss Function**

L_Total = L_Data + λ₁L_Hooke + λ₂L_CLT + λ₃L_Energy + λ₄L_Failure
--

# Explainable AI

To improve model transparency, **Deep SHAP** is used to analyze feature importance and prediction behavior.

Generated explanations include:

* SHAP Summary Plot
* Waterfall Plot
* Force Plot
* Feature Importance Ranking
* Individual Prediction Explanation

---

# Technologies

* Python
* TensorFlow
* NumPy
* Pandas
* Scikit-learn
* SHAP
* Matplotlib
* ANSYS ACP
* Python Colab



# Research Objectives

* Predict the mechanical properties of UD CFRP laminates.
* Improve prediction accuracy using physics-informed learning.
* Integrate Classical Laminate Theory into deep learning.
* Reduce dependence on computationally expensive FEA simulations.
* Provide explainable predictions using Deep SHAP.

---

# Future Work

* Multi-objective optimization
* Progressive damage prediction
* Ply-wise failure localization
* Uncertainty quantification
* Experimental validation
* Extension to hybrid composite laminates

---

# Citation

If you use this repository in your research, please cite the corresponding thesis or publication.

---

**Author:** Engineer Baren Kumar Baidya
**Research Area:** Physics-Informed Deep Learning • Composite Materials • Machine Learning • Explainable AI • Finite Element Analysis
