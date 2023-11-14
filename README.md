as I mentioned before data cleaning and data transformation are two fundamental and essential steps for any data science project.
They are the two first tasks that must be accomplished by any data scientist when obtaining the raw data for first time. 

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

- Data Normalization : means transforming features to be on a similar scale which improves the performance and training stability of the model. I have used :
    - Min-Max feature scaling (Normalization)
    - Maximum absolute scaling (Normalization)
    - Z-score method (Standardization Scaling)
    - Log scaling or Log transformation
  
- Transforming categorical values to numeric variables : both nominal and ordinal data were considered. I have used :
    - Python’s Category Encoder Library
    - Dummy Variable Encoding
    - Using Scikit-learn
    - Ordinal Encoding
    - How to choose the best Encoding Method # Feature Engineering and Variable Transformation
## Conclusion
• Transformed data is easier to understand and to analyze either by computer or human.
