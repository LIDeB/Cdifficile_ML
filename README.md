# Ligand-Based Virtual Screening Pipeline for *Clostridioides difficile* Spore Germination Inhibitors

![Jupyter Notebook](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat&logo=Jupyter)

## Overview

This repository contains the complete computational pipeline used to build, validate, and apply ensemble linear regression models specifically designed for virtual screening campaigns to identify novel germination inhibitors for *Clostridioides difficile* spores. The workflow integrates data preprocessing, feature selection, and the generation of consensus predictive models to identify novel bioactive candidates.

---

## Description
The pipeline is structured to ensure reproducibility, allowing researchers to replicate the results or adapt the methodology to different chemical datasets. It covers the following sequential steps:

| Step | Description |
|------|-------------|
| 1  | Individual model generation (random subspace + forward stepwise) |
| 2  | Evaluation of individual models on external validation sets 
| 3  | Selection of non-redundant models for ensemble construction |
| 4  | Ensemble generation and AUC/AUPR evaluation |
| 5  | Interactive AUC-vs-number-of-models curves |
| 6  | Internal validations (Fisher y-randomization and Leave-Group-Out cross-validation) |
| 7  | Detailed evaluation of a chosen ensemble (ROC, PR curves) |
| 8  | Positive Predictive Value (PPV) surface as a function of prevalence (Ya) and sensitivity/specificity ratio (Se/Sp) |
| 9  | Prospective virtual screening on an external compound library |
| 10 | Applicability domain assessment |
| 11 | Integration of applicability domain results with screening scores |
| 12 | Candidate selection: drug-likeness filters, PAINS detection, Tanimoto similarity, and Murcko scaffold analysis |

---

## Dependencies

- Python >= 3.8
- `pandas`
- `numpy`
- `scikit-learn`
- `statsmodels`
- `plotly`
- `rdkit`
- `openpyxl`

---

## How to Use

Each step contains a clearly delimited **USER CONFIGURATION** block. Only the parameters inside those blocks need to be modified. Everything below each configuration block runs automatically.


## Reference:
Caram F,, Alberca L., Trejo F. M., Ruatta S., Faraoni M. B., Musso F., Pérez P. F., Talevi A., Bellera C. L. Ligand-Based Virtual Screening Approach to Identify Novel Germination Inhibitors for Clostridioides difficile Spores. Chem Med Chem 2026. (sent)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
