# SQL 

# Description
This SQL code retrieves data from the bigquery-public-data.world_bank_intl_education.international_education table. It calculates rates of change and population ratios for specific indicators and years, focusing on the richest and poorest countries. To represent the wealthiest countries per GDP per capita by choosing five G7 nations. For the most impoverished ones, I chose five countries from this website: https://www.gfmag.com/global-data/economic-data/the-poorest-countries-in-the-world. 

#Note:
There is missing information due to countries not having data in the same decade or simply because the World Bank does not have enough information about the countries.

# Explanation
The SQL code consists of a single main query that includes three subqueries. Here's an overview of each part:

Main Query: The main query selects the appropriate columns and makes every decade found in the year column into its own column. It also performs the calculation for first_grade_population_ratio and last_grade_popualtion_ratio.

First Subquery (complete): This subquery retrieves data grouped by country and indicator, creating new columns for every decade. It uses conditional aggregation to get the values for each year. The subquery also filters the data to focus on specific countries and indicators.

Second Subquery (pop): This subquery retrieves population data for the first and last grade of primary education in 2010. 

Third Subquery (enroll): This subquery retrieves enrolment data for the first and last grade of primary education in 2010. 

Joins: The main query joins the subqueries on the country name to combine the retrieved data. It uses LEFT JOIN to ensure all rows from the first subquery are included, even if there are no matches in the second and third subqueries.
