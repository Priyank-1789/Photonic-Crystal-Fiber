# Estimation of Optical Properties of Photonic Crystal Fibers using Machine Learning

## 📌 Project Overview

This project presents a **machine learning-based approach** for predicting the optical properties of **Photonic Crystal Fibers (PCFs)** using various structural parameters as inputs. The study aims to reduce the dependence on computationally expensive simulation tools like **COMSOL Multiphysics**, offering a faster and scalable alternative using supervised learning algorithms.

---

## 🎯 Problem Statement

Traditional methods for determining PCF optical properties (e.g., FEM, FDTD) are **accurate but computationally intensive**. The challenge is:

> Can we accurately predict optical properties such as **effective refractive index (Neff)**, **effective mode area (Aeff)**, **dispersion**, and **confinement loss** using machine learning models based on the fiber’s structural parameters?

---

## 🧪 Objectives

- To **develop and evaluate ML models** capable of predicting PCF optical properties.
- To **reduce computational cost** and **time** compared to conventional simulation methods.
- To establish a **data-driven framework** for PCF design and analysis.

---

## 📊 Dataset Description

- **Total Samples:** 1118  
- **Data Source:** Simulations from COMSOL Multiphysics  
- **Input Features:**
  - Core refractive index
  - Cladding refractive index
  - Number of cladding rings
  - Airhole diameter (d)
  - Pitch (Λ)
  - Operating wavelength (µm)
- **Target Variables:**
  - Effective refractive index (Neff)
  - Effective mode area (Aeff)
  - Dispersion (ps/nm·km)
  - Confinement loss (log-scaled)

---

## ⚙️ Methodology

1. **PCF Modeling**: Designed using COMSOL with varying geometries.
2. **Data Generation**: Extracted optical properties from simulation results.
3. **Preprocessing**: Feature scaling (MinMaxScaler), reshaping, normalization.
4. **Model Training**: Applied four ML models using `scikit-learn`.

### Machine Learning Models Used:
- 🔵 **Artificial Neural Network (ANN)**
- 🟢 **Random Forest Regression (RFR)**
- 🟣 **Support Vector Regression (SVR)**
- 🟠 **K-Nearest Neighbours Regression (KNNR)**

### Evaluation Metrics:
- Mean Squared Error (MSE)
- Mean Absolute Percentage Error (MAPE)
- R² Score

---

## 📈 Results Summary

| Model | Neff R² | Aeff R² | Dispersion R² | Confinement Loss R² |
|-------|---------|---------|----------------|----------------------|
| **SVR** | 0.9999 | 0.9966 | 0.9986 | 0.9943 |
| **ANN** | 0.9929 | 0.9950 | 0.9189 | 0.9842 |
| **RFR** | 0.9900 | 0.9790 | 0.9920 | 0.9650 |
| **KNNR** | 0.9777 | 0.9699 | 0.9080 | 0.9872 |

✅ **SVR** was found to be the most accurate and robust model overall.

---

## 🧠 Key Insights

- ML algorithms significantly **reduce prediction time** compared to FEM simulations.
- **SVR** and **ANN** perform best in capturing nonlinear relationships in PCF design.
- **RFR** is highly interpretable and stable, suitable for engineering applications.
- **KNNR** is simple but less consistent with complex outputs like dispersion.

---

## 🧩 Future Work

- Expand dataset to include more diverse PCF geometries.
- Explore **inverse design** frameworks for structural parameter prediction.
- Integrate **hybrid models** with physics-informed constraints.
- Develop **GUI tools** for optical property prediction using trained ML models.

---

## 👨‍🎓 Author

**Priyankkumar Umeshkumar Gadliwala**  
M.Tech Bioinformatics (MBI2023007)  
Indian Institute of Information Technology, Allahabad  
Supervised by: Dr. Akhilesh Tiwari

---

## 📄 References

1. Sunny Chugh et al., "Machine learning approach for computing optical properties of a photonic crystal fiber," *Optics Express*, 2019.  
2. Md. Kaium and Md. Mollah, "Optical properties estimation of PCF using Gaussian Process Regression," *Opt. Continuum*, 2024.  
3. Jabin & Fok, "Prediction of Photonic Crystal Fiber Properties Using MLP in Deep Learning," *IEEE Photonics Letters*, 2022.
