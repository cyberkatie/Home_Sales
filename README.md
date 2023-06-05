# Home_Sales
UPenn Data Bootcamp Module 22 Assignment

* Imported the necessary PySpark SQL functions for this assignment.
* Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.
* Created a temporary table called homeSales.
* Answered the following questions using SparkSQL:
  * What is the average price for a four-bedroom house sold for each year? Answer is rounded off to two decimal places.
  * What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Answer is rounded off to two decimal places.
  * What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Answer is rounded off to two decimal places.
  * What is the "view" rating for homes costing more than or equal to $350,000? Determined the run time for this query, and rounded off answer to two decimal places.
* Cached temporary table homeSales.
* Verified if temporary table is cached.
* Using the cached data, ran the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determined the runtime and compare it to uncached runtime.
  * The uncached runtime was found to be 2.02 seconds. The cached runtime was found to be 0.86 seconds, making this significantly faster than the uncached runtime.
* Partitioned by the "date_built" field on the formatted parquet home sales data.
* Created a temporary table for the parquet data.
* Ran the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determined the runtime and compared it to uncached runtime.
  * The cached runtime was 0.86 seconds, where the partitioned runtime was found to be 0.98 seconds. While it is still over a second shorter than the unmodified query, it is slightly slower than the cached runtime by 0.12 seconds, making the cached data the most efficient.
* Uncached the homeSales temporary table.
* Verified that the homeSales temporary table is uncached using PySpark.
