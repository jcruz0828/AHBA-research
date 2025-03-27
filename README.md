# **AHBA Data Acquisition and Analysis with Abagen**

## **Overview**
This repository contains comprehensive notes and scripts to analyze **gene expression data** from the **Allen Human Brain Atlas (AHBA)** using the **Abagen** library. The main goal is to leverage gene expression data to uncover brain functions and analyze gene regulation patterns.

---

## **Features**
- **Data Acquisition:**
  - Fetch RNA-Seq data for multiple donors.
  - Fetch raw MRI (T1w/T2w) images for brain mapping.
  - Fetch gene group data for functional analysis.
  - Fetch microarray data for gene expression profiling.

- **Data Visualization:**
  - Interactive visualization of MRI slices using `ipywidgets`.
  - Left-to-right slice navigation for donor 9861.

- **Gene Expression Analysis:**
  - Quantification of gene expression levels using TPM.
  - Differential expression analysis.
  - Gene co-expression network analysis.
  - Multimodal data integration with RNA-Seq, microarray, and MRI data.

- **Machine Learning Applications:**
  - Predicting gene expression from brain anatomy.
  - Clustering gene expression profiles.
  - Predictive modeling of brain functions based on gene data.

---

## **Installation**
To get started with the project, clone the repository and install the required packages:

```bash
git clone https://github.com/username/ahba-abagen-analysis.git
cd ahba-abagen-analysis
pip install -r requirements.txt
