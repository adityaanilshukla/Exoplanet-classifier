# Exoplanet Classification Using Machine Learning

This project explores the classification of exoplanets using machine learning models, focusing on two algorithms: k-Nearest Neighbors (kNN) and a self-implemented Decision Tree. The goal is to determine which model more accurately classifies exoplanets into categories such as Gas Giants, Super Earths, Neptune-like, and Terrestrial planets.

## Overview

- **Notebook**: `exo-planet.ipynb`
- **Report**: Included in PDF format with detailed analysis and results
- **Models Used**:
  - k-Nearest Neighbors (kNN)
  - Decision Tree (from scratch)

## Objective

To compare and evaluate the performance of kNN and Decision Tree algorithms in classifying exoplanets using attributes from the NASA Exoplanet Archive.

## Dataset

- Sourced from the NASA Exoplanet Archive
- Features include mass, radius, distance, stellar magnitude, and more
- Classification Categories:
  - Gas Giants
  - Super Earths
  - Neptune-like
  - Terrestrial

## Methodology

1. **Preprocessing**
   - Dropped rows with missing data
   - Normalized distance and stellar magnitude
   - Log-transformed skewed numerical features
   - Used SMOTE to balance class distribution

2. **Model Implementation**
   - **kNN**:
     - Used `k=3`
     - High precision for Gas Giants but struggled with Terrestrial class
   - **Decision Tree**:
     - Self-implemented using Gini impurity
     - Max depth of 3 to prevent overfitting
     - Strong performance and interpretable feature importance

## Evaluation Metrics

- Precision, Recall, F1-Score
- Confusion Matrix
- ROC Curves
- AUC Scores

### Key Findings

| Model        | Strengths                                   | Weaknesses                                  |
|--------------|---------------------------------------------|----------------------------------------------|
| kNN          | High precision for Gas Giants               | Poor recall for underrepresented classes     |
| Decision Tree| Balanced performance, interpretable splits  | Possible overfitting due to high accuracy    |

- Most predictive features: `mass_multiplier` and `radius_multiplier`
- Decision Tree showed slightly better generalization and performance

## Conclusion

Both kNN and Decision Trees are viable for exoplanet classification. However, the Decision Tree model proved to be slightly more robust, offering a good balance of accuracy and interpretability — particularly valuable for understanding the physics behind planetary classification.

## References

- NASA Exoplanet Archive  
- scipy.stats.skew — SciPy Documentation  
- Jauregui, A. F. — How to program a decision tree in Python from scratch  
- Bujokas, E. — Decision Tree Algorithm in Python From Scratch - Towards Data Science

































