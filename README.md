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
- Data exploration
- Feature engineering:
      - Feature selection : choosing the set of features to include in the model. 
      - Data transformation: sometimes we transform variable before include them in the model
      - Text Data Processing: Tokenize, vectorize, and preprocess text data to make it suitable for machine learning models.
      - Time-Series Feature Engineering: create lag features, rolling statistics, or other time-related features for time-series data.
- Data transformation :
    - Feature Scaling: convert the scale of numeric data so they are comparable
        - Normalization
        - Standard scaling : converts features to standard normal variables (by subtracting the mean and dividing the standard error)
        - Log scaling or Log transformation
        - Polynomial transformation
    - Feature encoding : converting categorical variables to numeric variables
    - Feature extraction : use techniques like Principal Component Analysis (PCA) or Singular Value Decomposition (SVD) to reduce dimensionality and extract essential features.
    - Binning or Discretization : group continuous variables into bins or discrete intervals to simplify complex relationships.
    - Creating Interaction Terms : combining existing features to capture interactions between them.

# Feature Engineering
 
 Feature engineering refers to the process of raw data manipulation such as addition, deletion, combination, mutation etc. It encompasses the process of creating new features or modifying existing ones to improve the performance of a machine learning model.

 In addition, feature engineering in Machine Learning involves extracting useful features from the given input data to better learn the target using our choosen machine learning model. It involves transforming data to forms that better relate to the underlying target to be learned. 
 At the end, only the most significant features, that have linear relation with the target, are given to the model and the remaining features are discarded.
 
In order to achieve an effective feature engineering, it is important to understand deeply the business problem and the given data via perforing exploratory data analysis and data cleaning.

##  Data Transformation 

Data transformation is indeed one subtask within the broader field of feature engineering in machine learning. It is a specific aspect of feature engineering that involves modifying the raw data to make it more suitable for the learning algorithm. 

Moreover, The data transformation step could be required either before some data cleaning tasks or between data cleaning and Exploratory Data Analysis (EDA). Data transformation before data cleaning, is the process of converting data from one format to another such as from JSON to CSV or data aggregation etc. After data cleaning, this process helps convert our cleaned data into useful information and more significant features. 

Data transformation can include various operations such as:

- Scaling and Standardization: adjusting the scale of features to a similar range or standardizing them to have a mean of 0 and a standard deviation of 1.
- Normalization: scaling features to a range between 0 and 1.
- Encoding Categorical Variables: converting categorical variables into numerical representations that can be used by machine learning algorithms.
- Logarithmic Transformations: applying logarithmic, square root, or other power transformations to handle skewed distributions.
- Binning or Discretization: arouping continuous data into bins or discrete intervals.
- Creating Interaction Terms: combining existing features to capture interactions between them.
- Feature Extraction: reducing dimensionality through techniques like Principal Component Analysis (PCA) or extracting meaningful features from raw data.
  
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
      - One-hot Encoding: converts variables that take multiple values into binary (0,1) variables one for each category. This creates several new variables.
      - Label Encoding
      - Ordinal Encoding: converting ordered categories to numerical values, assigning each categorical value to a number such as 0,1,2 etc. while respecting the order : for example LOW==> 0, Medium==>1, High==>2.
      - Helmert Encoding
      - Binary Encoding : convert variables to either 0 or 1 suitable for variables with two values such as YES/NO, True/FALSE
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
- Variable transformation and feature engineering are integral components of the machine learning pipeline.
- Transformed data is easier to understand and to analyze either by computer or human.
- Feature engineering involves creating new features, selecting relevant ones, and extracting meaningful information to improve a model's ability to capture patterns and relationships within the data.
- Effective variable transformation and feature engineering require a deep understanding of the data and domain knowledge.
