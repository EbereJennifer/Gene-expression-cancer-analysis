#### RNA-seq Gene Expression Variability Analysis Across Cancer Types

##### Project Overview
This project explores RNA-seq gene expression data across multiple cancer types to identify highly variable genes and investigate differences in expression patterns between cancer classes. The analysis focuses on understanding how gene expression varies across five cancer types and identifying genes that may show cancer-type-specific activity.
- Cancer types included in the study:
  - BRCA (Breast Cancer)
  - KIRC (Kidney Renal Clear Cell Carcinoma)
  - LUAD (Lung Adenocarcinoma)
  - PRAD (Prostate Adenocarcinoma)
  - COAD (Colon Adenocarcinoma)

- The workflow includes:
  - dataset preparation
  - cleaning
  - merging
  - exploratory analysis
  - variance-based gene selection and
  - visualization using heatmaps and clustering.

##### Dataset Description
The analysis uses two datasets:

1. RNA-seq Dataset:
Contains gene expression measurements of 20,530 genes (features)
801 patient samples (observations)

- Each row represents one sample and each column represents one gene(see data).

2. Label Dataset:
Contains sample/class identifiers
- Includes cancer-type classification for each sample

##### Project Workflow

Step 1: Data Loading
The RNA-seq dataset and label dataset are loaded using pandas and prepared for merging.

Step 2: Data Cleaning
- Renamed unnamed identifier columns
- Ensured consistent formatting
- Verified dataset dimensions
- Removed unnecessary columns where required
  
Step 3: Dataset Merging
The gene expression dataset and class labels were merged using the shared sample identifier column.

Step 4: Feature and Label Separation
- Features (X): gene expression values
- Labels (y): cancer-type classification
- This structure enables downstream statistical analysis.

Step 5: Exploratory Data Analysis
Performed initial exploration of class distribution:







Count plots
Pie chart visualization
Key outcome: These plots help understand dataset balance across cancer categories.

Step 6: Gene Variability Analysis
Variance was used as the primary metric to identify highly variable genes across samples.

Process:
- Compute variance for each gene
- Sort genes by variance
- Select top 10 most variable genes






These genes are strong candidates for distinguishing cancer-specific expression behavior.

Step 7: Differential Expression Analysis
Mean expression levels of top variable genes were computed across cancer classes to observe class-specific expression patterns.
Key outcome: Identification of genes with distinct expression signatures across cancer types.

Step 8: Heatmap Visualization
Heatmaps were generated to visualize:
- Expression differences across cancer types
- Relative gene activity patterns







This helps identify relationships between genes and cancer categories.

Step 9: Cluster Map Visualization
Cluster maps were used to:
- Group genes with similar expression profiles
- Reveal hidden structure in expression patterns






  
- Clustering supports biological interpretation and pattern discovery.

- Technologies Used for this analysis:
  - Python
  - Google Colab
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
  
##### Key Results
- Identified top high-variance genes across samples
- Observed cancer-type-specific expression patterns
- Visualized expression differences using heatmaps
- Clustered genes with similar expression behavior

These findings highlight genes that may serve as potential biomarkers for distinguishing cancer types.

##### Future Improvements
Possible extensions of this project:
Apply dimensionality reduction (PCA / t-SNE)
Perform classification using machine learning models
Conduct pathway enrichment analysis

Author
Ebere Jennifer Agbarakwe
MSc. Biomedical Sciences, BSc. Microbiology
Currently WBS GRUPPE student(Data Science with Python Cert.)
