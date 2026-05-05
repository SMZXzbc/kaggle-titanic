# Kaggle Titanic - 生存预测

这是我的第一个 Kaggle 竞赛项目，使用机器学习预测泰坦尼克号乘客的生存情况。

## 成绩

| 版本 | 模型 | 准确率 |
|------|------|--------|
| v1 | 逻辑回归 + 基础特征 | 75.36% |
| v2 | 随机森林 + 特征工程 | **77.99%** |

## 特征工程

- 从 Name 中提取头衔（Title）：Mr, Mrs, Miss, Master, Rare
- 创建家庭人数（FamilySize = SibSp + Parch + 1）
- 是否独自一人（IsAlone）
- 按性别和船舱等级分组填充 Age 缺失值

## 技术栈

- Python 3.x
- Pandas / NumPy
- Scikit-learn（RandomForestClassifier）
- Jupyter Notebook

## 文件说明

- `titanic-baseline.ipynb`：完整代码（数据探索 → 特征工程 → 建模 → 预测）
- `submission_v2.csv`：最终提交文件
- `requirements.txt`：依赖库

## 运行方式

```bash
pip install -r requirements.txt
jupyter notebook
# 打开 titanic-baseline.ipynb 运行即可