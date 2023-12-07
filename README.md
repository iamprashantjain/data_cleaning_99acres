# data_cleaning_99acres

This code performs extensive data cleaning on a dataset extracted from 99acres, a real estate platform. Here's a breakdown of the cleaning operations performed:

Reading the Data: The code starts by reading a CSV file ('flats.csv') using Pandas, loading it into a DataFrame (df).

Data Exploration:

Adjusting Pandas display options (pd.set_option) to show all rows and columns for better visibility.
Displaying a random sample of 5 rows from the dataset (df.sample(5)).
Checking the shape of the dataset (df.shape) and obtaining information about data types and missing values (df.info()).
Data Cleaning Steps:

Handling duplicates (df.duplicated().sum()).
Identifying missing values and dealing with them (df.isnull().sum()).
Dropping unnecessary columns (df.drop(columns=['link','property_id'], axis=1, inplace=True)).
Renaming columns ('area' to 'price_per_sqft').
Cleaning Specific Columns:

Cleaning the 'society' column by removing ratings info and converting to lowercase.
Handling 'price' column values containing "Price on Request" and standardizing price values in lakhs and crores.
Cleaning 'price_per_sqft' column by removing non-numeric characters.
Handling 'bedRoom', 'bathroom', and 'balcony' columns by removing unnecessary parts and converting to appropriate data types.
Managing missing values in the 'additionalRoom' column and converting text to lowercase.
Processing 'floorNum' column by extracting floor numbers and cleaning the text.
Handling missing values in the 'facing' column by replacing them with 'not available'.
Feature Engineering:

Creating new columns ('area' and 'property_type') based on existing columns.
Renaming columns for better clarity ('area' to 'total_area').
Converting text in 'property_type' column to lowercase.
Saving Cleaned Data:

Saving the cleaned DataFrame to a new CSV file ('flats_cleaned.csv').
Overall, this code demonstrates a comprehensive process of exploring, cleaning, handling missing values, and performing feature engineering on a real estate dataset obtained from 99acres, preparing it for further analysis or modeling tasks.
