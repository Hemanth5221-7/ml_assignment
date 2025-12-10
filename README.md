
Random Forest — Effect of Feature Subsampling on Correlated Features
Overview

This repository accompanies a university Machine Learning coursework project investigating the role of feature subsampling in Random Forests. The study focuses on the max_features parameter and analyses how it influences tree diversity, inter-tree correlation, and generalisation performance in the presence of correlated and redundant input features.

The repository contains the complete implementation used to generate the experimental results and figures discussed in the accompanying written report (submitted separately as a PDF or webpage).

Project Objective

The objective of this project is to provide a focused and interpretative analysis of how max_features controls ensemble behaviour in Random Forests. Rather than comparing multiple models, the study isolates a single internal mechanism and examines:

Tree-to-tree prediction correlation

The bias–variance trade-off induced by feature subsampling

Performance under correlated feature conditions

Structural and class-wise prediction behaviour

Repository Structure

notebooks/
Contains the Jupyter notebook used to run all experiments, compute metrics, and generate plots.

figures/
Stores all figures produced by the experiments, including performance trends, inter-tree correlation plots, and confusion matrices.

report/
Contains the final written tutorial (PDF or webpage), including figures and references.

data/
No external data files are required. All datasets are generated programmatically using scikit-learn.

Dataset

Experiments are conducted on a synthetic multiclass classification dataset generated using scikit-learn. The dataset is specifically designed to include informative and redundant features, inducing strong feature correlations. This controlled setup enables clear interpretation of how feature subsampling impacts ensemble diversity and generalisation.

Experimental Design

All experiments use a Random Forest classifier with a fixed number of trees and consistent training settings. The max_features parameter is varied systematically while all other hyperparameters are held constant to ensure controlled comparison.

Evaluation metrics include:

Accuracy

Macro-averaged F1 score

Multiclass log loss

Average inter-tree prediction correlation

Reproducibility

All experiments are fully reproducible. The notebook can be executed from start to finish to regenerate every reported metric and figure. Random seeds are fixed, and no manual preprocessing steps are required.

Requirements

The project is implemented in Python and relies on standard scientific and machine learning libraries, including NumPy, Matplotlib, Seaborn, and scikit-learn. No specialised hardware or external datasets are required.

Usage

Review the written report in the report/ directory to understand the theoretical motivation and experimental findings.

Open the notebook in the notebooks/ directory and execute it sequentially to reproduce all results and figures.

Inspect the generated plots in the figures/ directory alongside the analysis presented in the report.

License

This project is released under an open-source license for educational and non-commercial use. Please refer to the LICENSE file for detailed terms.
