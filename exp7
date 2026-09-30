import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import seaborn as sns

%matplotlib inline

tips = sns.load_dataset("tips")
tips.head()

sns.displot(tips.total_bill, kde=True, color="purple")
sns.displot(tips.total_bill, kde=False, color="purple")

sns.jointplot(x=tips.tip, y=tips.total_bill)
sns.jointplot(x=tips.tip, y=tips.total_bill, kind="reg")
sns.jointplot(x=tips.tip, y=tips.total_bill, kind="hex")

sns.pairplot(tips)
tips.time.value_counts()
sns.pairplot(tips, hue="time")
sns.pairplot(tips, hue="day")

sns.heatmap(tips.corr(numeric_only=True), annot=True)

sns.boxplot(tips.total_bill)
sns.boxplot(tips.tip)

sns.countplot(y="day", data=tips)
sns.countplot(y="sex", data=tips)
tips.sex.value_counts().plot(kind="pie")
plt.show()

tips.sex.value_counts().plot(kind="bar")
plt.show()
sns.countplot(
    y="day",
    data=tips[tips.time == "Dinner"],
    hue="day",
    palette="pastel",
    legend=False
)
plt.show()
