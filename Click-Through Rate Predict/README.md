# 广告点击率预测（CTR Prediction）

通过用户、广告位、时间等特征，预测用户是否会点击广告。

本项目对比了 **决策树、随机森林、逻辑回归**，以及**加入特征工程后**的各模型表现，比较它们的准确率。

## 数据集

数据来自 Kaggle 竞赛：[Avazu CTR Prediction](https://www.kaggle.com/competitions/avazu-ctr-prediction/data)

下载后请将数据文件放在项目根目录的 `data/` 文件夹下，目录结构如下：

```text
data/
├── train.csv              # 训练集
├── test.csv               # 测试集
└── sampleSubmission.csv   # 提交样例
```

> 数据集体积较大，**未包含在本仓库中**，需要自行从 Kaggle 下载。

## 环境依赖

- Python 3.8+
- 主要依赖：

```bash
pip install -r requirements.txt
```

`requirements.txt` 内容参考：

```text
pandas
numpy
scikit-learn
imblearn
statsmodels
category_encoders
```

## 项目结构

```text
.
├── notebook.ipynb        # 主分析代码
├── README.md
├── requirements.txt
├── .gitignore
└── data/                 # 数据集（不提交到仓库）
```

## 方法

对同一份数据，分别训练并对比以下模型：

| 模型 | 是否含特征工程 |
|---|---|
| 逻辑回归 | 否 |
| 逻辑回归 | 是 |
| 决策树 | 否 |
| 决策树 | 是 |
| 随机森林 | 否 |
| 随机森林 | 是 |

特征工程主要包括：时间特征拆分、类别特征编码、点击率相关统计特征等。

## 运行方式

1. 按上文说明下载数据并放入 `data/` 目录。
2. 安装依赖：

```bash
pip install -r requirements.txt
```

3. 启动 Jupyter：

```bash
jupyter notebook
```

4. 打开 `notebook.ipynb`，从头运行即可。

## 结果

各模型在验证集上的准确率对比：

| 模型 | 准确率 |
|---|---|
| 逻辑回归 | 待填 |
| 逻辑回归 + 特征工程 | 待填 |
| 决策树 | 待填 |
| 决策树 + 特征工程 | 待填 |
| 随机森林 | 待填 |
| 随机森林 + 特征工程 | 待填 |

> 具体数值见 `notebook.ipynb` 输出。

## 说明

- 本项目为学习/练习用途，模型未做大规模调参。
- 数据集版权归 Kaggle 及原作者所有，本仓库仅包含代码。