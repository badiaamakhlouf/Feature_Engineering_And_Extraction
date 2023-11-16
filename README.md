Before preparing the data for training machine learning models phase, it is useful to perform a feature engineering process. 
It aims to manipulate, select and transform raw data into more significant features that can be used in supervised learning.
Faeture engineering helps increase model accuracy, leading to better performance and discovering the appropriate findings.

Data transformation is the main part in feature engineering process. In addition, data transformation next to data cleaning are
two fundamental and essential steps for any data science project. They are the two first tasks that must be accomplished by any data scientist
when obtaining the raw data for first time and before provide tarining data to the machine learning model.
Sometimes, we perform EDA (Exploratory data analysis) between data cleaning and feature engineering tasks
to further understand patterns, determine correlation and summarize the key insights.

<div>
<img src="images/data_transformation.png "Data cleaning" width="500"/>
</div>

*Source : [zanovoy.com](https://www.zanovoy.com/blog-posts/data-transformation-the-benefits-of-taking-the-time-to-right-your-wrongs)*

## Summary 
- Import the required libraries
- Data reading
- Feature engineering 
- Data transformation :
    - Normalization
    - Standardisation 
    - Log scaling or Log transformation 
    - Mapping categorical variables to numeric variables : data encoding using multiple solutions
- 

##  Data Transformation 

The data transformation step could be required either before some data cleaning tasks or between data cleaning and Exploratory Data Analysis (EDA). Data transformation before data cleaning, is the process of converting data from one format to another such as from JSON to CSV or data aggregation etc. After data cleaning, this process helps convert our cleaned data into useful information and more significant features. 

Data transformation is important because most of machine learning models are based on some assumptions such in case of linear regression models
we assume that variables (observations) have a linear relationship with the target. Therefore, we use data transformation to ensure the existence of this linear relationship. 
In addition, most of cases raw data is skewed either positively or negatively while in linear regression models we assume that residuals are normally distributed so data transformation ca resolve this problem.

*Note:residuals are estimates of experimental error obtained by subtracting the observed responses from the predicted responses.* 

Some examples of data transformation are:

•	Aggregation: concatenate data from multiple sources and store them into a single format. 

•	Normalization: transform attributes to be on a similar scale e.g., from 0 to 1, which ameliorate model performance and training stability. 

•	Standardization: rescale data values so that its mean will be 0 and its standard deviation will be 1. The new data distribution fits standard normal distribution. 

•	Manipulation: data is transformed to render it more readable and organized. 

•	Attribute construction: adding one new attribute or more from existing ones.

•	Scaling

• Etc.

During the data transformation part, I have accomplished the next steps: 

- Data transformation : means transforming features to be on a similar scale which improves the performance and training stability of the model. I have used :
  - Normalization : 
    - Min-Max feature scaling (Normalization) using `MinMaxScaler`
    - Maximum absolute scaling (Normalization) using `.abs().max()`
  - Standardisation
    - Z-score method (Standardization Scaling) using `mean()` and `std()` or `StandardScaler` 
  - Log transformation
    - Log scaling or Log transformation using `np.log()` 
  - Feature encoding : transforming categorical values to numeric variables : both nominal and ordinal data were considered. I have used :
    - Python’s Category Encoder Library :
      - One-hot Encoding
      - Label Encoding
      - Ordinal Encoding
      - Helmert Encoding
      - Binary Encoding
      - Frequency Encoding
      - Mean Encoding
      - Weight of Evidence Encoding
      - Probability Ratio Encoding
      - Hashing Encoding
      - Backward Difference Encoding
      - Leave One Out Encoding
      - James-Stein Encoding
      - M-estimator Encoding
      - Thermometer Encoder
    - Dummy Variable Encoding using `pd.get_dummies()`
    - Using Scikit-learn such as `OneHotEncoder`
    - Ordinal Encoding such as `cat.codes` of pandas
    - How to choose the best Encoding Method
     
 # Feature Engineering
 
 Feature engineering refers to the process of raw data manipulation such as addition, deletion, combination, mutation etc. 

 In addition, feature engineering in Machine Learning involves extracting useful features from the given input data to better learn the target using our choosen machine learning model. It involves transforming data to forms that better relate to the underlying target to be learned. 
 At the end, only the most significant features, that have linear relation with the target, are given to the model and the remaining features are discarded.
 
In order to achieve an effective feature engineering, it is important to understand deeply the business problem and the given data via perforing exploratory data analysis and data cleaning.
 
## Conclusion
• Transformed data is easier to understand and to analyze either by computer or human.
