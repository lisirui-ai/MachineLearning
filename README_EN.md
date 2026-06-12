English | [中文](README.md)

# MachineLearning

A **scikit-learn**-based machine learning repository that systematically covers feature engineering, classification, regression, and clustering through Jupyter Notebooks. Every code cell is annotated in detail, making it ideal for beginners and for review.

## Repository Contents

| Notebook                             | Topic                 | Key Content                                                                                                                            |
| ------------------------------------ | --------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `1.feature_engineering.ipynb`        | Feature Engineering   | DictVectorizer, CountVectorizer, TF-IDF, jieba Chinese tokenization, MinMaxScaler, StandardScaler, VarianceThreshold, PCA              |
| `2.classification_algorithm.ipynb`   | Classification        | KNN (Facebook Check-ins), Naïve Bayes (20 Newsgroups), Decision Tree (Titanic), Random Forest, Pipeline & GridSearchCV                 |
| `3.regression_algorithm.ipynb`       | Regression            | Linear Regression (Normal Equation), SGD, Lasso / Ridge Regularization, Logistic Regression (Breast Cancer)                           |
| `4.clustering.ipynb`                 | Clustering            | KMeans (synthetic data + customer segmentation), Elbow Method (SSE), Silhouette Coefficient (SC), cluster visualization               |
| `5.ensemble_learning.ipynb`          | Ensemble Learning     | Manual Voting Classifier, VotingClassifier (hard/soft), BaggingClassifier (OOB), Random Subspace & Random Patches, Random Forest, Extra-Trees, AdaBoost, GBDT |

## Tech Stack

- Python 3
- [scikit-learn](https://scikit-learn.org/) — machine learning algorithms and utilities
- [pandas](https://pandas.pydata.org/) / [NumPy](https://numpy.org/) — data manipulation and numerical computing
- [matplotlib](https://matplotlib.org/) — visualization
- [jieba](https://github.com/fxsjy/jieba) — Chinese text tokenization

## Quick Start

### Prerequisites

- Python 3.10 or higher
- A virtual environment is recommended

### 1. Clone the Repository

```bash
git clone https://github.com/lisirui-ai/MachineLearning.git
cd MachineLearning
```

### 2. Create and Activate a Virtual Environment (Recommended)

```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

`requirements.txt` pins the core project dependencies (scikit-learn, pandas, numpy, matplotlib, jieba, joblib, seaborn). All transitive dependencies are resolved automatically by pip.

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks in order to follow the learning path:

1. `1.feature_engineering.ipynb` — Feature Engineering
2. `2.classification_algorithm.ipynb` — Classification Algorithms
3. `3.regression_algorithm.ipynb` — Regression Algorithms
4. `4.clustering.ipynb` — Clustering Algorithms
5. `5.ensemble_learning.ipynb` — Ensemble Learning

## Datasets

Some examples depend on external CSV files that must be downloaded from Kaggle and placed in the `data/` directory before running the corresponding notebook.

| Dataset                              | Used In                             | Download Link                                                                                                                          | Local Path                     |
| ------------------------------------ | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| Facebook V: Predicting Check Ins     | `2.classification_algorithm.ipynb`  | [Kaggle — Facebook V: Predicting Check Ins](https://www.kaggle.com/competitions/facebook-v-predicting-check-ins/data)                 | `data/FBlocation/train.csv`    |
| Titanic: Machine Learning from Disaster | `2.classification_algorithm.ipynb` | [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/data)                                 | `data/titanic.txt`             |
| Breast Cancer Wisconsin (Diagnostic) | `3.regression_algorithm.ipynb`      | [Kaggle — Breast Cancer Wisconsin (Diagnostic)](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)                   | `data/breast-cancer-wisconsin.csv` |
| Mall Customer Segmentation Data      | `4.clustering.ipynb`                | [Kaggle — Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)     | `data/customers.csv`           |

> Built-in sklearn datasets (Iris, 20 Newsgroups, California Housing, etc.) are downloaded and cached automatically to the `data/` directory on first run — no manual action required.

## Project Structure

```
MachineLearning/
├── 1.feature_engineering.ipynb       # Feature Engineering
├── 2.classification_algorithm.ipynb  # Classification Algorithms
├── 3.regression_algorithm.ipynb      # Regression Algorithms
├── 4.clustering.ipynb                # Clustering Algorithms
├── 5.ensemble_learning.ipynb         # Ensemble Learning
├── data/                             # Dataset directory
│   ├── FBlocation/                   # Facebook check-in data (download from Kaggle)
│   │   ├── train.csv
│   │   └── test.csv
│   ├── breast-cancer-wisconsin.csv   # Breast cancer data (download from Kaggle)
│   ├── customers.csv                 # Mall customer segmentation data (download from Kaggle)
│   ├── titanic.txt                   # Titanic data (download from Kaggle)
│   └── *.pkz                         # Cached sklearn datasets (auto-generated at runtime)
├── linear_regression_model.pkl       # Saved linear regression model (generated after running notebook)
├── sgd_regression_model.pkl          # Saved SGD regression model (generated after running notebook)
├── scaler.pkl                        # Saved scaler (generated after running notebook)
├── LICENSE
├── README.md
├── README_EN.md
└── requirements.txt
```

## License

This project is open-sourced under the [MIT License](LICENSE).
