# Home_Sales
**In this project I use PySpark SQL to read in large data sets on home sales data. Data large enough to not be suitable for Python code.
The data contained the following columns:**
![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/a41f0be2-9c2a-4b2d-82e6-bd902fa00583)

**For this table we answer the following questions:**
![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/3f7935a9-a9f3-4fc9-8cb0-0948b512a2a5)

**How we optimize computing power for large data sets is through partioning the data, caching tables and using parquet files.**

**As you can see, the query below took .75 seconds to run. This is before partioning, caching and using parquet files:**
![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/8515ccd2-f727-4922-a93a-033b19f024a5)

**Here we cache the table and then test to confirm it is cached to memory:**
![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/6da6f1b8-f358-4525-b296-cbc422a834ae)


**We then parquet and partition the data into digestable pieces:**

![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/5bbf99a8-e7a0-4087-97d9-f63b0704708b)

**Once we utilize parquet files, cache the table and partition the data by the "date_built" column (for homes) we see huge improvement, cutting processing time in less than half:**

![image](https://github.com/eemahazion/pyspark-sql-home-sales/assets/124013416/132a62be-5452-4d34-887c-72311030b758)
