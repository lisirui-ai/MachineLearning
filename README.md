# MachineLearning

基于 **scikit-learn** 的机器学习仓库，通过 Jupyter Notebook 系统讲解特征工程、分类与回归算法的原理与实战，每段代码均配有详细中文注释，适合入门学习与复习查阅。

## 仓库内容


| Notebook                           | 主题   | 主要内容                                                                                               |
| ---------------------------------- | ---- | -------------------------------------------------------------------------------------------------- |
| `1、feature_engineering.ipynb`      | 特征工程 | DictVectorizer、CountVectorizer、TF-IDF、jieba 中文分词、MinMaxScaler、StandardScaler、VarianceThreshold、PCA |
| `2、classification_algorithm.ipynb` | 分类算法 | 数据集加载（Iris / 20 Newsgroups / California Housing）、KNN、朴素贝叶斯文本分类、决策树、随机森林、Pipeline 与 GridSearchCV    |
| `3、regression_algorithm.ipynb`     | 回归算法 | 线性回归（正规方程）、SGD 梯度下降、Lasso / Ridge 正则化、逻辑回归                                                         |


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

1. `1、feature_engineering.ipynb` — 特征工程
2. `2、classification_algorithm.ipynb` — 分类算法
3. `3、regression_algorithm.ipynb` — 回归算法

### 数据说明

- 部分 Notebook 首次运行时会自动下载数据集，是sklearn自带的，会缓存至 `./data` 目录
- 分类与回归 Notebook 中的 Facebook 签到、乳腺癌等示例需对应 CSV 文件，实际使用中灵活应变

## 项目结构

```
MachineLearning/
├── 1、feature_engineering.ipynb      # 特征工程
├── 2、classification_algorithm.ipynb  # 分类算法
├── 3、regression_algorithm.ipynb     # 回归算法
├── data/                              # 数据集缓存（运行时生成）
├── LICENSE
├── README.md
└── requirements.txt
```

## 许可证

本项目采用 [MIT License](LICENSE) 开源。