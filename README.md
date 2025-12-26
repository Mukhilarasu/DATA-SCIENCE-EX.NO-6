# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1032" height="178" alt="image" src="https://github.com/user-attachments/assets/63e11a2f-811e-42da-9e3a-083968e1d997" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="659" height="533" alt="image" src="https://github.com/user-attachments/assets/0f009548-64b5-407b-9ec9-78d4a7e381d6" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="664" height="536" alt="image" src="https://github.com/user-attachments/assets/f1caf2bf-4ffa-4359-bce6-83befd15da2a" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="846" height="579" alt="image" src="https://github.com/user-attachments/assets/3770a4bd-6363-4f50-91ff-3b0649bf1835" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="703" height="549" alt="image" src="https://github.com/user-attachments/assets/00c4f09a-71e6-471c-8b0b-0a3e3bbaf65c" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="706" height="551" alt="image" src="https://github.com/user-attachments/assets/2313af2c-0667-45df-b2f4-091bbfdc3082" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="571" height="432" alt="328475479-a5f69477-e68b-4892-b3cd-965610b7faef" src="https://github.com/user-attachments/assets/28b06382-a094-4296-8d78-826c95f9194a" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="684" height="550" alt="image" src="https://github.com/user-attachments/assets/46bfcb83-0771-4f14-8fdf-ab05d9bc2618" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="571" height="453" alt="image" src="https://github.com/user-attachments/assets/2efcf3fe-8596-4dfe-9942-60bb279fb902" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="723" height="551" alt="image" src="https://github.com/user-attachments/assets/43e09ded-8626-44e0-8e56-8da0a11f8be9" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="730" height="614" alt="image" src="https://github.com/user-attachments/assets/69956a4f-2f2e-4457-a5ab-811e19c0a1e8" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
