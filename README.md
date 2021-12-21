# UT Austin Fundraising Analysis
In this project, I am asking the question: who is more likely to donate money to a cause? My hypothesis is that someone who meets a certain set of criteria (ie: age, income, and education level) is more likely to donate then someone who does not meet set criteria. 

I want to address, from a managment prespective, the most efective way to utilize resources with the goal of achieving a success rate of over 95% within an 8 hour period. My intension is to give managers a tool that they can use to focus their direct report's efforts and while maximizing time. 

## Overview of the Analysis Scope of the Project
I am demonstrating my knowledge of unsupervised machine learning algorithiums. I use Python and the Pandas Library to preprocess the data and K-Means algoritum along with Prinicpal Component Analysis (PCA) to reduce the data to three columns. This will be further explained in the results section of this document. Furthermore, I use a dataset from Kaggle that redacted names, emails, and phone numbers but still contained 14 columns with information ranging from age to education level to marital status and income.

## Resources
- Data Source: Kaggle: Finding Donors for CharityML https://www.kaggle.com/ahmed2892/finding-donors-for-charityml
- Software: Conda 4.11.0 running Jupyter Notebook
- Pandas Libraries: Numpy, MatPlotLib, hvplot, Scikit-learn

## Results
To begin to test my hypothesis, I must first extract and transform the data. There are many constraints and considerations that are taken into account before analizing the data to answer my questions. 

The following image shows how I load the data into Pandas and create a dataframe of the actual data.
![load.png](Resources/load.png)
![df.png](Resources/df.png)

- Data Preprocessing

I use an f-string print statement to check for null values because unsupervised machine learning (ML) models can not use null values in their algorithum. This is one of the constriants of unsupervised ML models. 
![nulls.png](Resources/nulls.png)

Unnecessary data, or data that doesn't add to the solution, is another consideration when preprocessing your data. This is subjective and must be taken seriously as the analyist might unintensionally introduce biases into the algorithum. 
![drop.png](Resources/drop.png)


![divide.png](Resources/divide.png)
![binary.png](Resources/binary.png)
![transform.png](Resources/transform.png)
![preprocessed.png](Resources/preprocessed.png)
- PCA
![elbow.png](Resources/elbow.png)
![pca.png](Resources/pca.png)
- Outcome
![scatter3d.png](Resources/scatter3d.png)
![table.png](Resources/table.png)
## Summary
