# Module-22-Challenge

In this exercise, the following four questions were answered using SparkSQL:

1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
2. What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
3. What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
4. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

For Question 4, the runtime was compared across three different query methods: the original temporary view (uncached), a cached temporary table, and a partitioned Parquet temporary table.

**Original Temporary View (uncached):** query runtime was around 0.5017 seconds.

**Cached Temporary Table:** query runtime was around 0.2870 seconds, demonstrating the performance benefits of caching in Spark.

**Partitioned Parquet Temporary Table:** query runtime was around 0.4847 seconds. Although the data was partitioned by the "date_built" field in Parquet format, this didn't significantly improve performance. This is likely because the query still needed to read through each partitions to retrieve the answer for question 4, which limited the benefits of partitioning.

## Resources

Resources that I referred to for completing this homework:

<https://chatgpt.com/>
