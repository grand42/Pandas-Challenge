# Pandas-Challenge City Schools

## Background

This project usings pandas and jupyter notebook to analyze the district-wide standardized test results.  Using two datasets in csv format including [students_complete.csv](PyCitySchools/Resources/students_complete.csv), which includes info on student scores, gender, and grade, and the [schools_complete.csv](PyCitySchools/Resources/schools_complete.csv).

## Analysis

#### Import Dependencies

	# Dependencies and Setup
	import pandas as pd

#### Load, Read, and Merge Data files

	# File to Load
	school_data_file = "Resources/schools_complete.csv"
	student_data_file = "Resources/students_complete.csv"

	# Read School and Student Data File and store into Pandas DataFrames
	school_df = pd.read_csv(school_data_file)
	student_df = pd.read_csv(student_data_file)

	# Combine the data into a single dataset
	school_data = pd.merge(student_df, school_df, how="left", on=["school_name", "school_name"])


### District Summary

* Create a summary table describing the following results

	* Total Schools
  	* Total Students
  	* Total Budget
  	* Average Math Score
  	* Average Reading Score
  	* % Passing Math (The percentage of students that passed math.)
  	* % Passing Reading (The percentage of students that passed reading.)
  	* % Overall Passing (The percentage of students that passed math and reading.)

![District_Summary](PyCitySchools/Summary_Tables/District_Summary.PNG)

###### School Summary

* Create a summary table describing the following results:

  	* School Name
  	* School Type
  	* Total Students
  	* Total School Budget
  	* Per Student Budget
  	* Average Math Score
  	* Average Reading Score
  	* % Passing Math (The percentage of students that passed math.)
  	* % Passing Reading (The percentage of students that passed reading.)
  	* % Overall Passing (The percentage of students that passed math and reading.)

###### Top 5 Best Performing Schools (By % Overall Passing)

![Top5](PyCitySchools/Summary_Tables/Top5_Schools.PNG)


###### Top 5 Worst Performing Schools (By % Overall Passing)

![Bottom5](PyCitySchools/Summary_Tables/TopWorstSchools.PNG)


###### Average Math and Reading Scores by each Grade per School

*  Average Math Scores

![AvgMath](PyCitySchools/Summary_Tables/Avg_Math_Scores.PNG)

*  Average Reading Scores

![AvgReading](PyCitySchools/Summary_Tables/Avg_Reading_Scores.PNG)

##### Scores by School Spending, School Size, and School Type

  * Average Math Score
  * Average Reading Score
  * % Passing Math (The percentage of students that passed math.)
  * % Passing Reading (The percentage of students that passed reading.)
  * % Overall Passing (The percentage of students that passed math and reading.)

![School_Spending](PyCitySchools/Summary_Tables/Scores_by_Spending.PNG)

![School_Size](PyCitySchools/Summary_Tables/Scores_by_Size.PNG)

![School_Type](PyCitySchools/Summary_Tables/School_Type.PNG)