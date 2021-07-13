# SQL Pewlett Hackard Retirement Analysis
## Overview of the Analysis
Use SQL to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. Then, create a report that summarizes the analysis and helps to prepare for the “silver tsunami” as many current employees reach retirement age.

## Results
- retirement_titles.csv
  - Retrieve the employees who were born between 1952 and 1955 ordered by employee number
There is a bulleted list with four major points from the two analysis deliverables
- unique_titles.csv
  - Remove duplicate entries for some employees because they have switched titles over the years and keep only the most recent title of each employee.
- retiring_titles.csv
  - Retrieve the number of employees by their most recent job title who are about to retire.
- mentorship_eligibility.csv
  - Create a Mentorship Eligibility table that holds the employees who are eligible to participate in a mentorship program. 

## Summary
How many roles will need to be filled as the "silver tsunami" begins to make an impact?
  - According to the query used to generate the retiring_titles table, there are 90,398 employees of retirement age that will potentially need to have their roles filled. This number is broken down by job title in the table below.
<img width="250" alt="retiring_titles_table" src="https://user-images.githubusercontent.com/72039212/114719578-d8ec7980-9cfc-11eb-902b-1d0afe031685.png">

Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
- We can determine the number of qualified, retirement-ready employees in the departments running a COUNT query on the mentorship_eligibility table:
    - SELECT COUNT(me.emp_no)
    - FROM mentorship_eligibility as me
- There are 1,940 employees eligible to mentor. Pewlett Hackard needs each eligible employee to mentor 47 employees.
    
