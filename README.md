# Ex-09 Data Visualization.

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE:

## DEVELOPED BY : PAVITHRA R

## REG NO : 212222230106
 ```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()
```
## Which day of the week has the highest total bill amount?
```
sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")
```
## What is the average tip amount given by smokers and non-smokers?
```
sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")
```
## How does the tip percentage vary based on the size of the dining party?
```
sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")
```
## Which gender tends to leave higher tips?
```
sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")
```
## Is there any relationship between the total bill amount and the day of the week?
```
plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()
```
## How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?
```
sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")
```
## Which dining party size group tends to have the highest average total bill amount?
```
sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")
```
## What is the distribution of tip amounts for each day of the week?
```
sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")
```
## How does the tip amount vary based on the type of service (lunch vs. dinner)?
```
sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")
```
## Is there any correlation between the total bill amount and the tip amount?
```
sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
heatmap
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```

# OUTPUT:
## Initial Dataset:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/679e1029-799a-4039-9254-f0554aad0d18)


## tips.head():
![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/a1c1f8e3-5371-4440-a3f6-3580fb48659f)


## tips.info():

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/ff924e0c-16e6-4b3b-8fb9-e45e30ea039b)


## Bar Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/77a7c595-d890-4fde-8180-f73c33662d51)


![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/5fd803e3-d5fe-45cc-be19-1c4b504c71d0)

## Box Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/169412cf-3ba5-4aed-ace7-06a3c4192f16)

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/b241040e-3bf6-4484-9cc6-58c25532f261)

## Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/9e1b8f3b-c95f-4f90-bdf0-18a39b5f355e)

## Violin Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/dd8131af-beb7-4782-b295-8fce0bf1d78e)

## Bar Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/494a1304-b36e-4c9e-8635-e8b866fac498)

## Box Plot:

![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/3aff214d-a7c1-4737-bd1e-ab6c92dc60d4)


## Violin Plot:
![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/5eaaecaf-ad1f-42e1-96e3-3c83ce780ad4)

## Scatter Plot:
![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/cfc13659-3df3-4be0-a2a4-968a0c484c5b)

## Heatmap:
![image](https://github.com/Pavithraramasaamy/ODD2023-Datascience-Ex-09/assets/118596964/33390603-f3cf-4eba-ab14-ed0ad26673dc)


## RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file




