# GASHAP: Alzheimer's Disease Prediction via an explainable CNN using Genetic Algorithm and SHAP values 

This repository contains the implementation of the **GASHAP** framework introduced in:

> Mohammad Zahedipour, Mohammad Saniee Abadeh, Shakila Shojaei (2025).
> *Alzheimer’s Disease Prediction via an Explainable CNN using Genetic Algorithm and SHAP values.*  
> PLOS ONE.

---

## 🧠 Overview

GASHAP integrates **Deep SHAP** explanations with a **Genetic Algorithm (GA)** to generate anatomically interpretable regional masks from a 3D-CNN model trained on MRI brain scans.  
It enables both accurate classification and transparency in Alzheimer’s disease diagnosis.

**Key features:**
- 3D-CNN architecture with 3 convolutional blocks (kernel sizes 5×5×5, 3×3×3, 3×3×3)  
- SHAP-based voxel-level importance mapping  
- Genetic Algorithm optimization (population=200, generations=500, α=0.025, β=0.975)  
- Produces interpretable brain-region masks  

---

## 📊 Dataset

MRI data used in this study were obtained from the **Alzheimer’s Disease Neuroimaging Initiative (ADNI)** database  
👉 [https://adni.loni.usc.edu/](https://adni.loni.usc.edu/)

The ADNI dataset is **publicly available** to registered users upon approval of a Data Use Agreement.  
No personal or identifying information is included.

---

## ⚙️ How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/MohammadZp/GASHAP.git
   cd GASHAP
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Prepare your data:
   - MRI volumes: `X_train.npy`, `X_val.npy`, `X_test.npy`  
   - Labels: `y_train.npy`, `y_val.npy`, `y_test.npy`  
   - Atlas masks: `BMAPS.npy` (or `atlas_masks.npz`)  
   - Optional: `TEMPLATE.npy`

4. Run the notebook:
   - Open **GASHAP_main.ipynb** in **Google Colab** or **Jupyter Notebook**.
   - Adjust paths if needed.
   - Run all cells to reproduce the results.

---

## 📁 Outputs
After execution, the following files are generated in the `outputs/` folder:
- `best_model.h5` – trained CNN model  
- `best_DNA.npy` – selected chromosome  
- `best_mask.npy` – final brain-region mask  
- `ga_history.npy` – GA evolution statistics  

---

## 🧩 Requirements
See [`requirements.txt`](requirements.txt).

---

## 🧾 License
This code is released under the [MIT License](LICENSE).

---

## 🧪 Citation
If you use this code or method, please cite:

> Mohammad Zahedipour, Mohammad Saniee Abadeh, Shakila Shojaei (2025). 
> *Alzheimer’s Disease Prediction via an Explainable CNN using Genetic Algorithm and SHAP values.*  
> PLOS ONE.
