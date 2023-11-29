Welcome to this article on Feature Engineering and Variable Transformation!

In the realm of machine learning, the journey from raw data to a well-performing model involves a crucial phase known as feature engineering. This process is not just a preliminary step before training; it is an artful and strategic manipulation of data. The goal? To shape, select, and transform raw data into meaningful features that will empower supervised learning.

Feature engineering is the key to unlocking the full potential of your machine learning models. By crafting features that encapsulate relevant information and relationships within the data, we pave the way for enhanced model accuracy. The result? Improved overall performance and the ability to uncover nuanced insights that might otherwise remain hidden.

Throughout this article, we will delve into the intricacies of feature engineering and variable transformation. From the fundamentals of manipulating data to the art of selecting and creating features, you'll gain a comprehensive understanding of how to optimize your data for machine learning success.


Are you ready to unlock the true potential of your data? Let's get started!

<div>
<img src="images/data_transformation.png "Data cleaning" width="500"/>
</div>

*Source : [zanovoy.com](https://www.zanovoy.com/blog-posts/data-transformation-the-benefits-of-taking-the-time-to-right-your-wrongs)*

## Summary 
1- Import the required libraries

2- Data reading

3- Feature selection

4- Data transformation 

    4.1. - Feature Scaling
    
        4.1.1- Data Normalization 
            a. Min-Max feature scaling (Normalization
            b. Maximum absolute scaling (Normalization)
            
        4.1.2- Standard scaling
            a. Z-score method
            b. Data Standardisation using StandardScaler
        4.1.3- log scaling or Log transformation
        4.1.4- Polynomial transformation
        4.1.5- Robust Scaling
     4.2- Feature encoding : Encoding categorical values to numeric variables
        4.2.1. Solution 1: Using Python’s Category Encoder Library
        4.2.2- Solution 2: Dummy Variable Encoding
        4.2.3- Solution 3: Using Scikit-learn¶
        4.2.4- Solution 4 : Ordinal Encoding - Manual
     4.3- Feature extraction
        4.3.1- Principal Component Analysis (PCA)
     4.4- Binning or Discretization
     4.5- Creating Interaction Terms
    
  

## Feature Engineering
 
 Feature engineering refers to the process of raw data manipulation such as addition, deletion, combination, mutation etc. It encompasses the process of creating new features or modifying existing ones to improve the performance of a machine learning model.

 In addition, feature engineering in Machine Learning involves extracting useful features from the given input data to better learn the target using our choosen machine learning model. It involves transforming data to forms that better relate to the underlying target to be learned. 
 At the end, only the most significant features, that have linear relation with the target, are given to the model and the remaining features are discarded.

Feature engineering encompasses several crucial phases to enhance the performance and interpretability of machine learning models:

- Feature Selection: This involves the strategic process of choosing a subset of features to include in the model. By selecting the most relevant features, we aim to optimize model performance and reduce complexity.

- Data Transformation: In certain cases, it is essential to transform variables before incorporating them into the model. This transformation can involve scaling, normalization, or encoding categorical variables to ensure compatibility and improved model accuracy.

- Text Data Processing: For tasks involving text data, a critical step is to tokenize, vectorize, and preprocess the text. Tokenization breaks down text into meaningful units, vectorization converts text into numerical format, and preprocessing enhances the text's suitability for machine learning models.

- Time-Series Feature Engineering: When dealing with time-series data, additional considerations come into play. This phase involves creating lag features, calculating rolling statistics, or generating other time-related features. These enhancements provide the model with insights into temporal patterns, enabling more effective analysis and predictions in time-series scenarios.

Through these phases, feature engineering plays a pivotal role in shaping input data to empower machine learning models with the information needed to make accurate and meaningful predictions. In order to achieve an effective feature engineering, it is important to understand deeply the business problem and the given data via perforing exploratory data analysis and data cleaning.

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
