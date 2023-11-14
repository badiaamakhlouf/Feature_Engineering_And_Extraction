As I mentioned before data cleaning and data transformation are two fundamental and essential steps for any data science project.
They are the two first tasks that must be accomplished by any data scientist when obtaining the raw data for first time.
Sometimes, we perform EDA (Exploratory data analysis) between data cleaning and data transformation tasks.

<div>
<img src="images/data_transformation.png "Data cleaning" width="500"/>
</div>

*Source : [zanovoy.com](https://www.zanovoy.com/blog-posts/data-transformation-the-benefits-of-taking-the-time-to-right-your-wrongs)*

## Summary 
- Import the required libraries
- Data reading
- Data transformation :
    - Normalization
    - Log scaling or Log transformation 
    - Standardisation
    - Mapping categorical variables to numeric variables : data encoding using multiple solutions

##  Data Transformation 

The data transformation step could be required either before some data cleaning tasks or between data cleaning and Exploratory Data Analysis (EDA). Data transformation before data cleaning, is the process of converting data from one format to another such as from JSON to CSV or data aggregation etc. After data cleaning, this process helps convert our cleaned data into useful information and more significant features. 

Some examples of data transformation are:

•	Aggregation: concatenate data from multiple sources and store them into a single format. 

•	Normalization: transform attributes to be on a similar scale e.g., from 0 to 1, which ameliorate model performance and training stability. 

•	Standardization: rescale data values so that its mean will be 0 and its standard deviation will be 1. The new data distribution fits standard normal distribution. 

•	Manipulation: data is transformed to render it more readable and organized. 

•	Attribute construction: adding one new attribute or more from existing ones.

•	Etc

During the data transformation part, I have accomplished the next steps: 

- Data transformation : means transforming features to be on a similar scale which improves the performance and training stability of the model. I have used :
  - Normalization : 
    - Min-Max feature scaling (Normalization) using `MinMaxScaler`
    - Maximum absolute scaling (Normalization) using `.abs().max()` 
    - Z-score method (Standardization Scaling) using `mean()` and `std()` or `StandardScaler`
    - Log scaling or Log transformation using `np.log()`
  
- Transforming categorical values to numeric variables : both nominal and ordinal data were considered. I have used :
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
 
## Conclusion
• Transformed data is easier to understand and to analyze either by computer or human.
