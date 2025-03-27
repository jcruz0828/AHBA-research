# **AHBA Data Acquisition and Analysis with Abagen**

## **Overview**
This repository contains a comprehensive collection of notes and scripts to analyze gene expression data from the **Allen Human Brain Atlas (AHBA)** using the **Abagen** library. The primary focus is on acquiring, preprocessing, and analyzing gene expression data from various data types such as **RNA-Seq**, **Microarray**, **Gene Group**, and **MRI** data. 

---

## **Features**
- **Data Acquisition:**
  - Fetch **Desikan-Killiany** data for donor information and brain structure labels.
  - Fetch **Donor Information** including demographic and medical attributes.
  - Fetch **Gene Group** data to categorize genes by functional relevance.
  - Fetch **Microarray Data** including gene expression and structural metadata.
  - Fetch **Raw MRI Images** (T1-weighted and T2-weighted) for high-resolution brain mapping.
  - Fetch **RNA-Seq Data** for high-resolution gene expression analysis.

- **Data Visualization:**
  - Display donor brain images (NIFTI format).
  - Generate interactive MRI slice visualizations.
  - Display gene expression matrices for exploratory analysis.

- **Gene Expression Analysis:**
  - Quantification of gene expression levels using **TPM**.
  - Cross-comparison of gene expression across samples.
  - Exploration of **gene attributes** including chromosome mapping and exon counts.

- **Data Processing:**
  - **Annotation Data:** Includes metadata such as brain structure, coordinates, and tissue quality.
  - **Ontology Data:** Hierarchical information about brain regions.
  - **Pacall Data:** Binary data indicating gene probe detection.
  - **Probes Data:** Maps probes to gene symbols and chromosomal locations.

---

## **Installation**
To install the required packages and dependencies, use the following commands:

```bash
git clone https://github.com/username/ahba-data-analysis.git
cd ahba-data-analysis
pip install -r requirements.txt
```

---

## **Usage**

### **1. Data Acquisition**

#### **Fetch Desikan-Killiany Data**
The `abagen.fetch_desikan_killiany()` function retrieves brain structure information and NIFTI images of donor brains. It provides insight into brain regions and hemispheric structures.

#### **Fetch Donor Information**
Fetch metadata for six donors including medical ID, age, sex, ethnicity, medical conditions, and post-mortem hours. Useful for linking gene expression data to demographic variables.

#### **Fetch Gene Group Data**
The `abagen.fetch_gene_group()` function returns a list of gene acronyms corresponding to specified biological or anatomical groups, such as `neuron`, `brain`, or `synaptome`.

---

### **2. Data Processing and Analysis**

#### **Microarray Data**
The `abagen.fetch_microarray()` function downloads gene expression data for six donors. It returns nested dictionaries containing:
- Annotation
- Microarray
- Ontology
- Pacall
- Probes

#### **RNA-Seq Data**
The `abagen.fetch_rnaseq()` function downloads RNA sequencing data, including:
- **Counts Data:** Raw RNA-seq read counts.
- **TPM Data:** Normalized transcript expression.
- **Annotation Data:** Metadata for RNA samples.
- **Genes Data:** Detailed gene attributes.
- **Ontology Data:** Brain region hierarchy.

#### **Raw MRI Images**
The `abagen.fetch_raw_mri()` function downloads high-resolution T1w and T2w images for anatomical brain mapping. These images can be visualized slice by slice.

---

## **3. Data Visualization**

### **MRI Slice Visualization**
Interactive slice navigation using `ipywidgets` for both T1w and T2w images:
```python
import ipywidgets as widgets
from IPython.display import display

slice_slider = widgets.IntSlider(value=0, min=0, max=100, step=1, description="Slice:")
display(slice_slider)
```

### **Gene Expression Profiling**
Plot heatmaps and expression distributions to visualize gene expression variations across brain regions.

---

## **4. Machine Learning Applications**
- **Predictive Modeling:** Predict gene expression from anatomical features.
- **Clustering and Classification:** Group genes with similar expression profiles.
- **Differential Expression Analysis:** Identify genes with significant expression differences.
- **Spatial Mapping:** Integrate MRI data to predict regional gene expression patterns.

---

## **5. Example Notebooks**
Explore the following Jupyter Notebooks for practical applications:
- **Desikan-Killiany Data Exploration.ipynb:** Visualize and analyze donor brain structure data.
- **RNA-Seq Data Analysis.ipynb:** Explore gene expression data and perform normalization.
- **MRI Slice Visualization.ipynb:** View interactive MRI slices of the brain.

---

## **Data Structure**

The project directory is structured as follows:
```
ahba-data-analysis/
├── data/
├── notebooks/
│   ├── desikan-killiany-exploration.ipynb
│   ├── rna-seq-analysis.ipynb
│   └── mri-visualization.ipynb
├── scripts/
├── README.md
└── requirements.txt
```

---

## **References**
- **Allen Human Brain Atlas (AHBA)**: [Human Brain Map](https://human.brain-map.org/)
- **Abagen Library**: [Documentation](https://abagen.readthedocs.io/)

---

## **Contributing**
Contributions are welcome! Please submit a pull request with improvements or fixes. 

---

## **License**
This project is licensed under the MIT License.

---

## **Contact**
For questions or feedback, feel free to open an issue or contact the maintainer.

