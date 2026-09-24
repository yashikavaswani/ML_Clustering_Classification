# Task 3: Classification & Clustering on Gene Expression Cancer RNA-Seq Data

Runs 5 classification algorithms and K-Means clustering on the Kaggle "gene
expression cancer RNA-Seq" dataset, comparing model accuracy and evaluating
how well unsupervised clustering recovers the true cancer type labels.

## Dataset

[Gene Expression Cancer RNA-Seq (Kaggle)](https://www.kaggle.com/datasets/waalbannyantudre/gene-expression-cancer-rna-seq-donated-on-682016)

Download and unzip into this folder as `data.csv` and `labels.csv`. 

- `data.csv` — gene expression matrix (samples x ~20,000 genes)
- `labels.csv` — cancer type label per sample (BRCA, KIRC, COAD, LUAD, PRAD)

## What's inside

`Task3_Classification_Clustering.ipynb`

1. Load data (falls back to a small synthetic dataset if the CSVs aren't found, so the notebook still runs end-to-end for a quick preview)
2. Preprocess: scale features, reduce dimensionality with PCA
3. Train/test split
4. Classification — one cell per model, each with accuracy, classification report, and a confusion matrix:
   - Logistic Regression
   - Support Vector Machine (SVM)
   - Naive Bayes
   - K-Nearest Neighbors (KNN)
   - Random Forest
5. Model accuracy comparison chart
6. K-Means clustering — elbow method, cluster fit, and evaluation against true labels (Adjusted Rand Index, Normalized Mutual Info, Silhouette Score)
7. Visualization of clusters vs. true labels (PCA 2D scatter)

## How to run

```bash
pip install -r requirements.txt
jupyter notebook Task3_Classification_Clustering.ipynb
```

Run all cells top to bottom. Outputs (plots, CSVs, metrics) are saved to
`task3_outputs/`.

## Requirements

See `requirements.txt`:
- numpy, pandas
- matplotlib, seaborn
- scikit-learn
- scipy
