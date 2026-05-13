# GEPred: Prediction of Gene Expression Levels from Protein Sequence

Welcome to the official documentation for **GEPred**, a computational method developed to predict the expression levels of genes based on the amino acid and dipeptide composition of their encoded proteins. While traditional microarray analysis focuses on mRNA levels, GEPred provides a novel approach to understanding the relationship between a protein's primary sequence and the abundance of its corresponding gene's expression.

**Web Server:** [http://www.imtech.res.in/raghava/gepred/](http://www.imtech.res.in/raghava/gepred/)

---

## Citation

Raghava, G. P. S., & Han, J. H. (2005). 
**Correlation and prediction of gene expression level from amino acid and dipeptide composition of its protein.** *BMC Bioinformatics*, 6, 59. 
[https://doi.org/10.1186/1471-2105-6-59](https://doi.org/10.1186/1471-2105-6-59)

---

## About the Platform

GEPred was developed based on the observation that the amino acid composition of proteins is significantly correlated with the expression levels of their respective genes. The tool was built and validated using expression data from two well-studied model organisms:
* **Saccharomyces cerevisiae** (Yeast)
* **Caenorhabditis elegans** (Worm)

By utilizing Support Vector Machines (SVM), GEPred can classify genes into different expression categories (e.g., highly expressed vs. lowly expressed) with high reliability.

### Key Features
* **SVM-Light Implementation**: Developed using the SVM-light package for robust pattern recognition.
* **Compositional Analysis**: Uses amino acid and dipeptide ($i+1$) composition as input features.
* **Species-Specific Models**: Provides optimized models for both yeast and worm datasets.
* **Regression & Classification**: Capable of predicting actual expression values as well as categorical classification.

---

## Technical Overview

The performance of GEPred was evaluated through rigorous cross-validation on large-scale microarray and SAGE (Serial Analysis of Gene Expression) datasets.

| Feature / Model | Correlation (R) | Accuracy (%) |
| :--- | :--- | :--- |
| **Amino Acid Composition** | ~0.40 - 0.45 | ~70% |
| **Dipeptide Composition** | ~0.42 - 0.48 | ~72% |

### Key Findings
* Certain amino acids (e.g., Alanine, Glycine, Valine) show a strong positive correlation with high expression levels.
* Cysteine and several aromatic residues often show a negative correlation with high expression levels.

---

## Model Functionality

* **Expression Level Prediction**: Users can submit one or more protein sequences to estimate the likely expression level of the corresponding gene.
* **Feature Extraction**: The server automatically calculates the percentage composition of 20 amino acids and 400 dipeptides for each sequence.
* **Comparative Analysis**: Allows for the study of how different sequence features influence the stability and abundance of proteins in a cell.

---

## Applications

* **Functional Genomics**: Identifying highly expressed genes in newly sequenced genomes where experimental expression data is unavailable.
* **Proteomics**: Understanding the sequence-level determinants of protein abundance and translation efficiency.
* **Metabolic Engineering**: Designing synthetic genes with sequence features optimized for high expression in host organisms.

---

## Contact & Authors

**Prof. Gajendra P. S. Raghava**
Bioinformatics Centre, Institute of Microbial Technology, Chandigarh, India.
**Email**: raghava@imtech.res.in

---

## License

This project is an open-access resource and is available for research and academic use provided the original work is properly cited.
