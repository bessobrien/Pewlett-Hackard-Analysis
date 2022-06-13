# Pewlett Hackard Analysis

## Overview

Use SQL and Postgres to determine the numer of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. This work is to help the manager prepare for upcoming retirement wave in the workforce.

## Resources

PostgreSQL 11

PGAdmin 6.8

VS Code 1.68.0

## Results

First step in our analysis was to write and execute a Retirement Titles table for the employees who are born between January 1, 1952 and December 31, 1955. We exported that table into csv found here: [Retirement Titles](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/retirement_titles.csv)

We then wrote and executed a query to create a Unique Titles table that contained the employee number, first and last name, and most recent title. Final table was exported to csv. [Unique Titles](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/unique_titles.csv)

And finally, we wrote and executed a query to create a Retiring Titles table that contained the number of titles filled by employees who are retiring. This table was also exported to csv. [Number of Retiring Titles](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/retiring_titles.csv)

The second part of our analysis was to determine the employees that were eligible for the Mentorship program. We wrote and executed a query to create a Mentorship Elibibility table for current employees who were born between January 1, 1965 and December 31, 1965. This was also exported to csv. [Employees Eligible for Mentorship](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/membership_eligibility.csv)

After going through the two major analysis and using SQL to write and execute queries, we determined four points:
1. The number of employees retiring is 90,398 employees.
2. The number of employees eligible for mentorship is 1,549 employees.
3. The top two titles that will need mentorship are Senior Engineer and Senior Staff.
4. Our original pool of retirees that we reviewed covered 3 birth years, whereas our employees reviewed for mentorship only covered one birth year.

## Summary

In conclusion, the number of employees retiring is 90,398, and we have only 1,549 employees ready for mentorship. We will need to fill 90,398 roles. There are enough qualified, retirement-ready employees to mentor, but not nearly enough to be mentored and start to fill in as the workforce starts to retire.

One solution to consider is to expand the birth dates of the employees that are eligible for mentorship. We can do this with a query that expands our search. 

![expand_mentorship.png](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/expand_mentorship.png)

Another solution would be to only compare one year of retirement candidates to one year of possible mentored employees (ie: those born in 1952 to mentor those born in 1965). We can do this by changing our first query to pull those only born in the year 1952, and the second query to pull only those born in 1965. 

![compare_one_year](https://github.com/bessobrien/Pewlett-Hackard-Analysis/blob/main/Data/one_year_comparison.png)
