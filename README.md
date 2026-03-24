<div align="center">
  <img src="https://ext.macno.org/typing-svg/?font=Fira+Code&weight=600&size=28&pause=1000&color=2ecc71&center=true&vCenter=true&width=600&lines=PiML+Fault+Diagnosis;Physics-Informed+Machine+Learning;TLS-DMD+%2B+PINN+Features+%2B+RF;CWRU+Bearing+Dataset" alt="Typing SVG" />
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Badge" />
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn Badge" />
  <img src="https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=white" alt="SciPy Badge" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas Badge" />
  <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black" alt="Matplotlib Badge" />
</p>

# ⚙️ PiML Fault Diagnosis — CWRU Bearing Dataset

> **An advanced, end-to-end framework for condition monitoring using Physics-Informed Machine Learning (PiML).**
> This repository strictly contains the essential codebase to execute the data processing and machine learning pipeline, maintaining a clean and minimal footprint.
---

## 🌟 Overview

This project implements a **Physics-Informed Machine Learning (PiML)** pipeline for mechanical fault diagnosis using the popular **CWRU Bearing Dataset**. It achieves a highly realistic target accuracy of **98–99%** by innovatively combining **TLS-DMD (Total Least Squares Dynamic Mode Decomposition)** with physics-informed features and an optimized Random Forest classifier.

### ✨ Key Highlights

- 🧠 **Physics-Informed Features:** Extraction of fundamental fault frequencies (BPFI, BPFO, BSF) and exponential decay constraints directly from the envelope spectrum.
- 📉 **TLS-DMD Integration:** Uses spatial-temporal decomposition to effectively separate underlying structural vibration modes from local fault impulse transients.
- 🚀 **Robust Classification:** A deeply tuned Random Forest classifier evaluated via strict `GroupKFold` cross-validation to prevent data leakage.
- 📊 **Comprehensive Analysis Engine:** The `main_pipeline.py` script automatically processes the dataset, trains the model, and generates **35 detailed plots**, including raw signals, envelope spectra, STFT spectrograms, 3D eigenvalue footprints, and model comparison benchmarks.

---

## 🛠️ Required Files

This repository aims for strict isolation of execution logic. Presentation files, uncompiled reports, and LaTeX sources have been purposefully excluded.

- `main_pipeline.py`: The core script that performs data loading, PiML feature extraction, model training, and generates all 35 high-quality figures in the `Results/` directory.
- `requirements.txt`: Lightweight list of strictly required Python dependencies.
- `.gitignore`: Excludes very large datasets, local results outputs, and latex generation code.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd piml-fault-diagnosis
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Data Setup:**
   - Create a `Dataset/` folder in the root directory.
   - Place the necessary `CWRU` MATLAB `.mat` files inside the `Dataset/` folder. The required classes are `Normal`, `IR021`, `B021`, and `OR021@6`.

4. **Execute the pipeline:**
   ```bash
   python main_pipeline.py
   ```
   > 📌 **Note:** Running the pipeline will automatically create a `Results/` folder populated with 35 `.png` analysis plots and will output cross-validation models details to the terminal.

<br>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=2ecc71&height=120&section=footer" alt="Wave Footer" />
</div>
