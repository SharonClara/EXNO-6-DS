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

<img width="1383" height="354" alt="596542896-707b9ee4-0646-47ab-8221-8bed547880f8" src="https://github.com/user-attachments/assets/c45f6bc9-7456-49aa-95ff-08eea20df14c" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="1375" height="706" alt="596543112-309dc599-2527-4566-9957-e1195d25d763" src="https://github.com/user-attachments/assets/498abba3-1f07-49df-b53b-a59e0f27c168" />

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

<img width="1375" height="763" alt="596543283-07a56010-3ccd-46f6-b609-9ba03d76de9d" src="https://github.com/user-attachments/assets/ee4c58a3-71dc-4113-96cf-3dd08574625f" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="1382" height="735" alt="596543475-afe86c54-c711-4f0c-a1b7-4ad02ee04102" src="https://github.com/user-attachments/assets/622d732e-96f8-44b6-a9b0-58fbbbb4c4f4" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()


```


<img width="1386" height="697" alt="596543645-8260f23a-9a43-4c76-9cc6-3a686e465816" src="https://github.com/user-attachments/assets/fbf0898b-5064-461b-81fd-bc3a0012cf5d" />


```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

<img width="1391" height="690" alt="596543855-1c727c22-05b4-4a1c-8b04-4b18919ab851" src="https://github.com/user-attachments/assets/ab8a2257-6ead-4e1b-b0bd-c06bc433f9ff" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="1397" height="649" alt="596544048-9db135fe-cf48-4eaf-8baf-033f412aa97b" src="https://github.com/user-attachments/assets/6c56bff6-1036-4be7-82bf-ae4dbc352f1c" />

```

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")


```


<img width="1389" height="698" alt="596544284-473e36a7-9194-4a7b-adf2-a0881992b205" src="https://github.com/user-attachments/assets/4114cdad-3a35-41ce-8156-2479355c707a" />


```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="1380" height="671" alt="596544533-46b0a54b-3d77-4ec9-9483-bed7ac28ea13" src="https://github.com/user-attachments/assets/fc2afdd6-c06f-4d06-be53-cf39bf7c8ce4" />


```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```

<img width="1356" height="639" alt="596545373-4224fb95-7160-459e-99fa-adc63657cb88" src="https://github.com/user-attachments/assets/a19daf45-4d12-4fe7-8d02-f1489a60ee76" />


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```


<img width="1389" height="757" alt="596545600-9babf32e-2020-4494-997a-0afd0299dfc5" src="https://github.com/user-attachments/assets/158ff3e4-5f7d-4a39-a271-70fb0e132775" />

# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
