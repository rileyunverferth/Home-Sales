# Home Sales Queries
## Module 22 Challenge (SparkSQL)

### Synopsis
We're looking at data from home sales to determine ket metrics. This is a big data set and in order to read it and perform queries we are using SparkSQL. With SparkSQL we will also be able to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.
</br>
</br>
A DataFrame was created to house the dataset, a temporary table of the DataFrame was created, and then the temporary table was given the following queries:
- What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
- What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
- What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
- What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

### Shortening Run Times
After this another method was tried to see if it was possible to make the same queries in a shorter run time.
</br>
</br>
In order to first see the run time of the first method, the temporary table was cached, and the last query was performed, while calculating the run time.
Next, a partition of the home sales dataset by the "date_built" field is created, and the formatted parquet data is read. A temporary table of the parquet data is created, the same query is run on the parquet temporary table, and the run time is computed. After determining the run time is shorter when run through the parquet temporary table, the temporary table is uncached.
