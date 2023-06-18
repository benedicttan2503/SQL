# SQL 

#Description
This SQL code retrieves data from the bigquery-public-data.world_bank_intl_education.international_education table. It calculates rates of change and population ratios for specific indicators and years, focusing on the richest and poorest countries according to GDP per Capita. The code uses subqueries and joins to obtain the desired results.

#Code Explanation
The SQL code consists of a single main query that includes three subqueries. Here's an overview of each part:

Main Query: The main query selects various columns and performs calculations on the retrieved data.

First Subquery (complete): This subquery retrieves data grouped by country and indicator, creating new columns for every decade. It uses conditional aggregation to get the values for each year. The subquery also filters the data to focus on specific countries and indicators.

Second Subquery (pop): This subquery retrieves population data for the first and last grade of primary education in 2010. It selects the maximum values for the corresponding indicators and filters the data based on specific countries and indicators.

Third Subquery (enroll): This subquery retrieves enrolment data for the first and last grade of primary education in 2010. It selects the maximum values for the corresponding indicators and filters the data based on specific countries and indicators.

Joins: The main query joins the subqueries on the country name to combine the retrieved data. It uses left joins to ensure all rows from the first subquery are included, even if there are no matches in the second and third subqueries.

#Usage
To use this SQL code:

Make sure you have access to the bigquery-public-data.world_bank_intl_education.international_education table in BigQuery.
Copy the SQL code and execute it in your preferred SQL environment or tool that supports BigQuery syntax.
Review the query results to obtain the calculated rates of change and population ratios for the selected indicators and years.

#Customization
To customize the SQL code for your specific needs:

Adjust the country names and indicator filters in the subqueries' WHERE clauses to focus on your desired countries and indicators.
Modify the selected years and indicators in the main query to retrieve different data or perform additional calculations.
Adapt the column aliases in the main query to match your desired output.
Please note that the SQL code assumes the existence of the specified table and column names. Ensure that the table and column names are accurate and accessible in your environment.
