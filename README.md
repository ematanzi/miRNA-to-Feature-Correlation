# miRNA-to-Feature-Correlation: A Strategy to Enhance Explainability in Alzheimer's Diagnosis
A methodology to improve model interpretability by linking microRNA (miRNA) expressions to predictive features in Alzheimer's classification models.

## 📁 Project Files

- 📄 Documentation: [`doc/MiRNA_to_Feature_Correlation[report].pdf`](doc/MiRNA_to_Feature_Correlation[report].pdf)
- 📊 Presentation: [`doc/MiRNA_to_Feature_Correlation[report].pdf`](doc/MiRNA_to_Feature_Correlation[report].pdf)
- 🧪 Main Notebook: [`explaining_classifications.ipynb`](explaining_classifications.ipynb)

## 📌 Overview

This project proposes a strategy to enhance the explainability of machine learning models used in the early diagnosis of Alzheimer's Disease (AD). It achieves this by tracing model predictions back to specific miRNA expression profiles through a two-step process:

1. **Sparse Mapping via Lasso Regression**  
   A sparse linear transformation is learned to link miRNA expressions to the 128-dimensional embedding space used by a classification model.

   * *P* describes, for each patient, genetic features extracted in the form of embeddings from miRNA analysis.
   * *X* describes, for each patient, the information related to miRNA together with personal information.
   * *Feature Importance* associates, to each feature in *P*, an importance score associated to the classification.

![first step](images\first_step.png)

2. **SHAP-Based Interpretation**  
   SHAP values are computed to identify the most influential features in each prediction, which are then translated into miRNA-level explanations.
   * Test set is extracted from *X*.
   * The weight matrix is computed in the first step.

![second step](images\second_step.png)

For more detalied information about the project, read the [documentation](doc\MiRNA_to_Feature_Correlation[report].pdf)