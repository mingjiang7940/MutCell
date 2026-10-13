# MutCell

**Mutation-associated Cell population inference in tumor single-cell transcriptomes**

---

## 🧠 Overview

Linking driver mutation status to malignant-cell transcriptional heterogeneity at single-cell resolution remains challenging because sparse mutation coverage and limited matched genomic data hinder reliable mutation-status assignment.

**MutCell** To link specific driver mutations to transcriptionally defined malignant cell states and populations in transcriptome-only scRNA-seq datasets. We developed MutCell, a transcriptome-based framework combining cross-cancer transfer learning from >8,000 tumors across 31 cancer types with calibration on a colorectal cancer single-cell atlas of ~1.01 million cells from 557 samples to identify driver mutation-associated cells without directly detecting mutant alleles.

---

## 🚀 Workflow Overview

MutCell consists of four main steps, corresponding to the project structure:

---

### **Step 1. Model Training (`Step1_ModelTraining`)**

- Train mutation prediction models via **multi-cancer transfer learning on bulk transcriptomic datasets**
- Learn **mutation-associated transcriptional signals**  

---

### **Step 2. Atlas Construction (`Step2_AtlasConstruction`)**

- Construct a **large-scale single-cell atlas**  

---

### **Step 3. Boundary Learning (`Step3_BoundaryLearning`)**

- Project bulk-derived signals into the single-cell expression space 
- Learn **decision boundaries** in the single-cell atlas  
- Identify stable regions corresponding to mutant and wild-type states  

---

### **Step 4. MutCell Inference (`Step4_MutCloneInference`)**

- Apply selected bulk-trained models to scRNA-seq data  
- Predict **mutation probability for each cell**  
- Infer mutation status using **confidence-based decision boundaries**  

---

## 🔧 Supporting Modules

- `Function/` — utility functions used across all steps  
- `0.Data/`   — input datasets and processed data  
- `Results/`  — prediction outputs  

---

## 🎯 Summary

**MutCell (Mutation-associated Cell population inference), an atlas-calibrated transfer learning framework for inferring driver mutation-associated cells.**
