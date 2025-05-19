# Data-Modelling-Project

### **1. Introduction:**

This project involves setting up a PostgreSQL database to store and manage wealth account data. It includes data cleaning, data insertion, and database management using Python, Pandas, and psycopg2.

### **2. Problem Statement:**

The objective of this project is to create a structured database for managing wealth account data from various datasets, ensuring data consistency, and facilitating future data analysis. It addresses the problem of unstructured financial data by integrating and storing it in a relational database format for easier querying and manipulation.

### **3. Technologies Used:**

* **Python:** Data processing and database interaction.
* **Pandas:** Data cleaning and preprocessing.
* **PostgreSQL:** Database management and structured data storage.
* **psycopg2:** Database connection and data insertion.
* **CSV Files:** Data source format.

### **4. Project Structure:**

* `Wealth-AccountData.csv`: Data related to accounts and their financial indicators.
* `Wealth-AccountsCountry.csv`: Data related to countries, income groups, and regions.
* `Wealth-AccountSeries.csv`: Data related to financial series and indicators.
* `main.py`: Main project file containing the data processing and database insertion logic.

### **5. Data Sources:**

* Wealth-AccountData.csv: Contains financial data for different countries and indicators across years.
* Wealth-AccountsCountry.csv: Contains country details including income group, region, and lending category.
* Wealth-AccountSeries.csv: Contains information about financial indicators, their definitions, and data sources.

### **6. Process:**

1. **Data Import:** Load CSV files using Pandas.
2. **Data Cleaning:**

   * Replace missing values (`..`) with NULL values.
   * Select relevant columns for each dataset.
3. **Database Design:** Create tables for account data, country data, and series data, with appropriate data types and primary keys.
4. **Data Insertion:** Insert cleaned data into the respective tables using parameterized SQL queries.
5. **Error Handling:** Implement `try-except` blocks to handle connection errors, data type mismatches, and other exceptions.

### **7. Challenges and Solutions:**

* **Data Inconsistencies:** The data contained missing values represented by `..`. This was resolved by replacing these with NULL values before insertion.
* **Data Type Conversion:** Some columns expected numeric values but contained strings (`..`). Data conversion and error handling were implemented to manage this.
* **Primary Key Conflicts:** In the `accountscountry` table, potential primary key conflicts were handled using `ON CONFLICT DO NOTHING` in the SQL query.
* **Database Connection Issues:** Ensured stable connection and committed transactions after data insertion to prevent data loss.

### **8. Database Design:**

* **Database Name:** dataengineer
* **Tables:**

  * `accountscountry`

    * Columns: Code, Long_Name, Income_Group, Region, Lending_category
  * `accountsdata`

    * Columns: country_code, country_name, series_code, year_1995, year_1996
  * `accountseries`

    * Columns: Code, indicator_name, long_definition, source, topic

### **9. How to Run the Project:**

* Install dependencies: `pip install psycopg2 pandas`
* Create the database: `python main.py`
* Check data insertion by querying the PostgreSQL database.

### **10. Conclusion and Learnings:**

This project provided hands-on experience in data engineering, database management, and data processing using Python. It reinforced the importance of data validation, conflict handling, and structured database design.
""")
