Before preparing the data for training machine learning models phase, it is useful to perform a feature engineering process. 
It aims to manipulate, select and transform raw data into more significant features that can be used in supervised learning.
Feature engineering helps increase model accuracy, leading to better performance and discovering the appropriate findings.

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
# Feature Engineering
 
 Feature engineering refers to the process of raw data manipulation such as addition, deletion, combination, mutation etc. 

 In addition, feature engineering in Machine Learning involves extracting useful features from the given input data to better learn the target using our choosen machine learning model. It involves transforming data to forms that better relate to the underlying target to be learned. 
 At the end, only the most significant features, that have linear relation with the target, are given to the model and the remaining features are discarded.
 
In order to achieve an effective feature engineering, it is important to understand deeply the business problem and the given data via perforing exploratory data analysis and data cleaning.

##  Data Transformation 

data transformation is indeed one subtask within the broader field of feature engineering in machine learning. Feature engineering encompasses the process of creating new features or modifying existing ones to improve the performance of a machine learning model. Data transformation is a specific aspect of feature engineering that involves modifying the raw data to make it more suitable for the learning algorithm.


Data transformation is the main subtask within the broader field of feature engineering in machine learning. In addition, data transformation next to data cleaning are
two fundamental and essential steps for any data science project. They are the two first tasks that must be accomplished by any data scientist
when obtaining the raw data for first time and before provide tarining data to the machine learning model.
Sometimes, we perform EDA (Exploratory data analysis) between data cleaning and feature engineering tasks
to further understand patterns, determine correlation and summarize the key insights.

Moreover, The data transformation step could be required either before some data cleaning tasks or between data cleaning and Exploratory Data Analysis (EDA). Data transformation before data cleaning, is the process of converting data from one format to another such as from JSON to CSV or data aggregation etc. After data cleaning, this process helps convert our cleaned data into useful information and more significant features. 

Data transformation can include various operations such as:

- Scaling and Standardization: Adjusting the scale of features to a similar range or standardizing them to have a mean of 0 and a standard deviation of 1.
- Normalization: Scaling features to a range between 0 and 1.
- Encoding Categorical Variables: Converting categorical variables into numerical representations that can be used by machine learning algorithms.
- Logarithmic or Power Transformations: Applying logarithmic, square root, or other power transformations to handle skewed distributions.
- Binning or Discretization: Grouping continuous data into bins or discrete intervals.
- Creating Interaction Terms: Combining existing features to capture interactions between them.
- Feature Extraction: Reducing dimensionality through techniques like Principal Component Analysis (PCA) or extracting meaningful features from raw data.
- Text Processing: Converting text data into a format suitable for machine learning models, such as using techniques like tokenization or vectorization.
  
Effective data transformation can have a significant impact on the performance of machine learning models by improving their ability to extract patterns and relationships from the data. It is an essential step in the overall feature engineering process, which aims to enhance the representational power of the features used by the model.


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
 
## Conclusion
• Transformed data is easier to understand and to analyze either by computer or human.
