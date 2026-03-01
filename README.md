# 🌟 DNN Surrogates for Charged Anisotropic Compact Stars
*Stability Boundary Learning · Parameter Manifold Mapping · Bayesian Inverse Inference*  

> **Manuscript:** *A Deep Neural Network Surrogate for Exact Einstein–Maxwell Stellar Solutions*  

---

## 🚀 Overview
This repository implements **deep neural network (DNN) surrogates** for modeling **charged anisotropic compact stars**. The surrogate replaces expensive ODE-based solutions of the Einstein–Maxwell equations with a high-fidelity, differentiable neural network, enabling rapid **stability boundary learning**, **parameter manifold mapping**, and **Bayesian inverse inference**.

---

## ⚙️ Features

| Feature | Details |
|---|---|
| Architecture | 8-layer ResNet, width 256, SiLU activations |
| Physics loss | MSE + Jacobian regularisation (γ = 1e-3) |
| Stability | Autograd turning-point detection |
| Inference | `emcee` affine-invariant MCMC, 128 walkers |
| Speedup | ~O(10⁴) vs direct ODE integration |

---

## ✨ Novel Contributions
1. First surrogate trained *exclusively* on closed-form Einstein–Maxwell solutions, eliminating numerical integration error.  
2. Jacobian-regularised loss enforcing gradient fidelity for downstream autodiff.  
3. Fisher Information Matrix (FIM) used for information-geometric parameter ranking.  
4. Herrera cracking hypersurface mapped via batch autograd.  
5. Deep ensemble uncertainty quantification feeding directly into MCMC likelihoods.  

---

## 🛠 Installation

# Create environment (recommended)
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt# DNN-Surrogates-for-Charged-Anisotropic-Compact-Stars-Stability-Boundary-Learning-
