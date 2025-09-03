# coffee-leave-rusty-
This is a ML project on coffee  rust detection , whether the leaves is rusty or not , i contains , some lab images  

# Coffee Leaf Rust Detection Using Machine Learning

![Rusty Leaf Example](images/rusty_leaf_sample.jpg)
*Example of a rusty coffee leaf (Image 1)*

![Non-Rusty Leaf Example](images/non_rusty_leaf_sample.jpg)
*Example of a healthy coffee leaf (Image 2)*

## Project Description

This repository contains an end-to-end machine learning pipeline for detecting coffee leaf rust from images. Coffee leaf rust is a major disease affecting coffee crops worldwide, and early detection can help prevent significant yield losses.

### Dataset

- **Source:** [Kaggle: Coffee Rust Dataset](https://www.kaggle.com/datasets/jorgearoca/coffee-rust)
- **Contents:** The dataset includes around 7000 images of coffee leaves, both healthy (non-rusty) and affected (rusty).
- **Sample Images:**  
  - Image 1: Rusty leaf  
  - Image 2: Non-rusty leaf

### Approach

We experimented with multiple deep learning models and ensemble techniques to classify images as either "rusty" or "non-rusty." The models were trained and evaluated using the labeled dataset mentioned above.

#### Models Compared

- Convolutional Neural Network (CNN)
- Swin Transformer
- Averaging Ensemble
- Stacking Ensemble (Logistic Regression, SVM, Random Forest, LightGBM)

### Performance Comparison

The performance metrics for each model are summarized in `model_performance_comparison.csv`. The metrics include accuracy, precision, recall, and F1-score for both classes (rust and no rust).

| Model                      | Accuracy | F1-score (Rust) | F1-score (No Rust) |
|----------------------------|----------|-----------------|-------------------|
| CNN                        | 0.91     | 0.94            | 0.80              |
| Swin Transformer           | 0.82     | 0.88            | 0.62              |
| Averaging Ensemble         | 0.92     | 0.95            | 0.81              |
| Stacking Ensemble (LogReg) | 0.89     | 0.93            | 0.77              |
| Stacking Ensemble (SVM)    | 0.89     | 0.93            | 0.77              |
| Stacking Ensemble (RF)     | 1.00     | 1.00            | 1.00              |
| Stacking Ensemble (LGBM)   | 1.00     | 1.00            | 1.00              |

For more details, see the full CSV file: `model_performance_comparison.csv`.

### How To Use

1. Clone the repository.
2. Download the dataset from Kaggle and place it in the appropriate folder.
3. Run the training scripts to reproduce the results or retrain the models on updated data.

### Repository Structure

- `images/` - Sample images of rusty and non-rusty leaves
- `model_performance_comparison.csv` - Performance summary of all models
- `notebooks/` - Jupyter notebooks for training and evaluation
- `src/` - Source code for data processing, training, and inference

### Acknowledgements

- The dataset is provided by Jorge Aroca on Kaggle.
- Model architectures and ensemble methods inspired by recent advances in ML for plant disease detection.

---

Feel free to contribute or raise issues for improvements!
