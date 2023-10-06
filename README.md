# pandas-challenge
 Module 04 Challenge


## Description 
pandas-challenge solution, due 10/12/2023

1. Create a new repository for this project called _pandas-challenge_. Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, create a folder for this homework assignment and name it _PyCitySchools_.
4. Add your Jupyter notebook to this folder. This will be the main script to run for analysis.
5. Push these changes to GitHub or GitLab.

### Instructions 
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

Hint: Check out the sample solution called _PyCitySchools_starter.ipynb_ located in the .zip file to review the desired format for this assignment.

### District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.
Include the following:
* Total number of unique schools
* Total students
* Total budget
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

### School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.
Include the following:
* School name
* School type
* Total students
* Total school budget
* Per student budget
* Average math score
*  Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

### Highest-Performing Schools (by % Overall Passing)
Sort the schools by _% Overall Passing_ in descending order and display the top 5 rows.
Save the results in a DataFrame called "top_schools".

### Lowest-Performing Schools (by % Overall Passing)
Sort the schools by _% Overall Passing_ in ascending order and display the top 5 rows.
Save the results in a DataFrame called "bottom_schools".

### Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).
Use the code provided below to create four bins with reasonable cutoff values to group school spending.

``` python
spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
``` 
Use _pd.cut_ to categorize spending based on the bins.
Use the following code to then calculate mean scores per spending range.

``` python  
spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
```

Use the scores above to create a DataFrame called _spending_summary_.
Include the following metrics in the table:
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

### Scores by School Size
Use the following code to bin the _per_school_summary_.

``` python
size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
```

Use _pd.cut_ on the "Total Students" column of the _per_school_summary_ DataFrame.

Create a DataFrame called _size_summary_ that breaks down school performance based on school size (small, medium, or large).

Scores by School Type
Use the _per_school_summary_ DataFrame from the previous step to create a new DataFrame called _type_summary_.

This new DataFrame should show school performance based on the "School Type".

## Requirements 
District Summary (20 points)
School Summary (20 points)
Highest-Performing Schools by Percentage of Overall Passing (5 points)
Lowest-Performing Schools by Percentage of Overall Passing (5 points)
Math Scores by Grade (10 points)
Reading Scores by Grade (10 points)
Scores by School Spending (5 points)
Scores by School Size (5 points)
Scores by School Type (5 points)
Written Report (15 points)

## Credits 
N/A 