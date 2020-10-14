# TCLMF
Clinical drug response prediction from preclinical cancer cell lines by logistic matrix factorization approach

TCLMF is a computational method to predict log IC50 for tumor samples. This method is used in cancer drug sensitivity prediction, which is a fundamental issue in precision medicine. This repository contains the implemented codes of TCLMF, the preprocessed data and the computed similarity matrices for cell lines and drugs.


Input files:
"GDSC_class_median.txt" : We used the median of the log (IC50) values for individual drugs as a threshold for the classification model. A cell line assigned to the sensitivity or class with label 0, if it's log (IC50) value is smaller than the median of cell lines for an individual drug and a cell line assigned to the resistance or class with label 1, otherwise.

"drug_similarity_23.txt": The similarity between drugs according to their chemical substructure fingerprints.
 
"similarity_EXP_980_1.txt": The similarity is based on the gene expression profile corresponding to cell lines or tumor samples. The Pearson correlation coefficient between the real-valued gene expression vectors is calculated. Since we have 979 cell lines and one tumor sample, the last row and last column correspond to the tumor sample similarity values across to 979 cell line samples.

"similarity_tissue_980_'name of tissue'.txt" : There are 15 different tissue type for a new tumor samples. Depending on the type of tumor tissue, you should consider one of these 15 files as program input. For example, if the tumor sample is a breast cancer tumor sample, you should use the "similarity_tissue_BRCA" file as an input file.

"Real_Ic50.txt": The log (IC50) values for cell lines and drugs.

