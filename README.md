# Ex-04-Multivariate-Analysis

# AIM

To Perform Multivariate Analysis for the SuperStore DataSet.

# Algorithm

1.Import the datasets and required libraries to perform the analysis.

2.Print the information about a DataFrame including the index dtype, columns, and non-null values.

3. Group the data according to the categories and apply a function to the categories

4. Represent the category of data with rectangular bars with lengths and heights that is proportional to the values which they represent using Barplot function.

5.Set the label for X and Y axis and print the Graph.

6.Use Pandas df.corr() function to find the correlation among the columns in the Dataframe.

7.Plot rectangular data as a color-encoded matrix.

# Program

import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df=pd.read_csv('/content/SuperStore.csv')

df.head()

df.info()

states=df.loc[:,["State","Sales"]]

states=states.groupby(by=["State"]).sum().sort_values(by="Sales")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("STATES")

plt.ylabel=("Sales")

plt.show()

df.corr()

sns.heatmap(df.corr(),annot=True)

# OUTPUT

![image](https://user-images.githubusercontent.com/84709944/231124870-5d73b87e-a259-4a93-8be7-41301f64d2da.png)

![image](https://user-images.githubusercontent.com/84709944/231124930-258e93de-5ff6-4fd5-a09a-a464ed7a4728.png)

![image](https://user-images.githubusercontent.com/84709944/231124997-df712d4c-ef63-4cd6-856d-d8ef1d5269c8.png)

![image](https://user-images.githubusercontent.com/84709944/231125063-8d27d8f9-7525-40ce-8913-81e55848cb19.png)

![image](https://user-images.githubusercontent.com/84709944/231125208-c803722b-eef8-4cb1-90d9-fa325cf18c71.png)

# RESULT

Hence the Multivariate Analysis for the SuperStore Dataset is Executed Successfully.



