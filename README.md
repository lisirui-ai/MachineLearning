# MachineLearning

基于 **scikit-learn** 的机器学习仓库，通过 Jupyter Notebook 系统讲解特征工程、分类、回归与聚类的原理与实战，每段代码均配有详细中文注释，适合入门学习与复习查阅。

## 仓库内容

| Notebook                             | 主题   | 主要内容                                                                                                |
| ------------------------------------ | ------ | ------------------------------------------------------------------------------------------------------- |
| `1.feature_engineering.ipynb`        | 特征工程 | DictVectorizer、CountVectorizer、TF-IDF、jieba 中文分词、MinMaxScaler、StandardScaler、VarianceThreshold、PCA |
| `2.classification_algorithm.ipynb`   | 分类算法 | KNN（Facebook 签到）、朴素贝叶斯（20 Newsgroups）、决策树（Titanic）、随机森林、Pipeline 与 GridSearchCV                   |
| `3.regression_algorithm.ipynb`       | 回归算法 | 线性回归（正规方程）、SGD 梯度下降、Lasso / Ridge 正则化、逻辑回归（乳腺癌）                                                   |
| `4.clustering.ipynb`                 | 聚类算法 | KMeans（make_blobs 模拟数据 + 客户消费行为案例）、肘部法（SSE）、轮廓系数（SC）评估、聚类结果可视化                                   |
| `5.ensemble_learning.ipynb`          | 集成学习 | 手动投票分类器、VotingClassifier（硬/软投票）、BaggingClassifier（OOB 袋外评估）、随机子空间与随机补丁、随机森林、Extra-Trees、AdaBoost、GBDT |


## 技术栈

- Python 3
- [scikit-learn](https://scikit-learn.org/) — 机器学习算法与工具
- [pandas](https://pandas.pydata.org/) / [NumPy](https://numpy.org/) — 数据处理与数值计算
- [matplotlib](https://matplotlib.org/) — 可视化
- [jieba](https://github.com/fxsjy/jieba) — 中文分词

## 快速开始

### 环境要求

- Python 3.10 及以上
- 建议使用虚拟环境隔离依赖

### 1. 获取代码

```bash
git clone https://github.com/lisirui-ai/MachineLearning.git
cd MachineLearning
```

### 2. 创建并激活虚拟环境（推荐）

```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
```

### 3. 安装依赖

```bash
pip install -r requirements.txt
```

`requirements.txt` 已锁定项目核心依赖（scikit-learn、pandas、numpy、matplotlib、jieba、joblib、seaborn），其余传递依赖会由 pip 自动安装。

### 4. 启动 Notebook

```bash
jupyter notebook
```

在浏览器中按顺序打开以下 Notebook 即可开始学习：

1. `1.feature_engineering.ipynb` — 特征工程
2. `2.classification_algorithm.ipynb` — 分类算法
3. `3.regression_algorithm.ipynb` — 回归算法
4. `4.clustering.ipynb` — 聚类算法
5. `5.ensemble_learning.ipynb` — 集成学习

## 数据集说明

部分示例依赖外部 CSV 文件，需提前从 Kaggle 下载并放置到 `data/` 对应子目录。

| 数据集 | 用于 Notebook | 下载地址 | 本地放置路径 |
| --- | --- | --- | --- |
| Facebook 签到位置预测 | `2.classification_algorithm.ipynb` | [Kaggle — Facebook V: Predicting Check Ins](https://www.kaggle.com/competitions/facebook-v-predicting-check-ins/data) | `data/FBlocation/train.csv` |
| 泰坦尼克号生还预测 | `2.classification_algorithm.ipynb` | [Kaggle — Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/data) | `data/titanic.txt` |
| 乳腺癌威斯康星数据集 | `3.regression_algorithm.ipynb` | [Kaggle — Breast Cancer Wisconsin (Diagnostic)](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) | `data/breast-cancer-wisconsin.csv` |
| 商场客户细分数据 | `4.clustering.ipynb` | [Kaggle — Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) | `data/customers.csv` |

> sklearn 自带数据集（Iris、20 Newsgroups、California Housing 等）首次运行时会自动下载并缓存至 `data/` 目录，无需手动操作。

## 项目结构

```
MachineLearning/
├── 1.feature_engineering.ipynb       # 特征工程
├── 2.classification_algorithm.ipynb  # 分类算法
├── 3.regression_algorithm.ipynb      # 回归算法
├── 4.clustering.ipynb                # 聚类算法
├── 5.ensemble_learning.ipynb         # 集成学习
├── data/                             # 数据集目录
│   ├── FBlocation/                   # Facebook 签到数据（需从 Kaggle 下载）
│   │   ├── train.csv
│   │   └── test.csv
│   ├── breast-cancer-wisconsin.csv   # 乳腺癌数据（需从 Kaggle 下载）
│   ├── customers.csv                 # 商场客户细分数据（需从 Kaggle 下载）
│   ├── titanic.txt                   # 泰坦尼克数据（需从 Kaggle 下载）
│   └── *.pkz                         # sklearn 自带数据集缓存（运行时自动生成）
├── linear_regression_model.pkl       # 线性回归模型（运行 Notebook 后生成）
├── sgd_regression_model.pkl          # SGD 回归模型（运行 Notebook 后生成）
├── scaler.pkl                        # 标准化器（运行 Notebook 后生成）
├── LICENSE
├── README.md
└── requirements.txt
```

## 许可证

本项目采用 [MIT License](LICENSE) 开源。
