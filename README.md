# UT Austin Fundraising Analysis
In this project, I am asking the question: who is more likely to donate money to a cause? My hypothesis is that someone who meets a certain set of criteria (ie: age, income, and education level) is more likely to donate then someone who does not meet set criteria. 

I want to address, from a managment prespective, the most effective way to utilize resources with the goal of achieving a success rate of over 95% within an 8 hour period. My intension is to give managers a tool that they can use to focus their direct report's efforts and while maximizing time. 

## Overview of the Analysis Scope of the Project
I am demonstrating my knowledge of unsupervised machine learning algorithiums. I use Python and the Pandas Library to preprocess the data and K-Means algoritum along with Prinicpal Component Analysis (PCA) to reduce the data to three columns. This will be further explained in the results section of this document. Furthermore, I use a dataset from Kaggle that redacted names, emails, and phone numbers but still contained 14 columns with information ranging from age to education level to marital status and income.

## Resources
- Data Source: Kaggle: Finding Donors for CharityML https://www.kaggle.com/ahmed2892/finding-donors-for-charityml
- Software: Conda 4.11.0 running Jupyter Notebook
- Pandas Libraries: Numpy, MatPlotLib, hvplot, Scikit-learn

## Results
To begin to test my hypothesis, I must first extract and transform the data. There are many constraints and considerations that are taken into account before analyzing the data to answer my questions. 

The following image shows how I load the data into Pandas and create a dataframe of the actual data.
![load.png](Resources/load.png)
![df.png](Resources/df.png)

- Data Preprocessing

To begin, I use an f-string print statement to check for null values because unsupervised machine learning (ML) models can not use null values in their algorithum. This is one of the constriants of unsupervised ML models. 
![nulls.png](Resources/nulls.png)

Unnecessary data, or data that doesn't add to the solution, is another consideration when preprocessing your data. This is subjective and must be taken seriously as the analyist might unintentionally introduce biases into the algorithum. 
![drop.png](Resources/drop.png)

To minimize the spread of numbers in capital gain's column, I divided the entire row by 100. This will put the values in the same range as the rest of the columns without lossing any data. Now, the entire dataset is between 1 and 40. 
![divide.png](Resources/divide.png)

I performed two different functions to numerically describe the remainding columns. The first was from the pandas library called "get_dummies". This essentially transforms binary data into ones and zeros and creates an extra column. Each column populates with a one and a zero based on the original input. The second function "Label Encoder" comes from the SciKit-Learn library. It transformes each value to a numeric representation of all the categories in that row. 
![binary.png](Resources/binary.png)
![transform.png](Resources/transform.png)

This is the final product as a dataframe ready for the next level of analysis. 
![preprocessed.png](Resources/preprocessed.png)

- PCA

To begin clustering, I utilized an elbow graph to show where increasing the number of clusters no longer caused differences in the results. In other words, I plotted clusters on the x-axis and inertia, which measures the amount of variation in the dataset, on the y-axis. I can now visually see where the point of diminishing return for clusering is reached. In this case, I feel that five clusers will sufice. 
![elbow.png](Resources/elbow.png)

PCA is a statistical technique to speed up machine learning algorithms when the number of input features (or dimensions) is too high. PCA reduces the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information in the original large set.
The big takeaway from eigenvectors and eigenvalues is that they show us the spread of the dataset and by how much.
The statistics, linear transformations, and eigenvalues and eigenvectors all illustrate how PCA works. 
I wanted to further identify clusters and experiment with other means of identifing clusters. So, I implemented Principal Component Analysis. This is a statistical technique to reduce the input features by transforming them into smaller chunks of information that still contains most of the original larger dataset. It employes eigenvectors and eigenvalues to show us the spread of the dataset and by how much. This is a much more complicated process rooted in linear algebra. However, the coding for this is much easier. 
![pca.png](Resources/pca.png)
- Outcome
![scatter3d.png](Resources/scatter3d.png)
![table.png](Resources/table.png)
## Summary

## Presentation
[Here](website) is a link to a presentation discussing this work. 