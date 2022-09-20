# PyCitySchools

## Overview of Analysis

In this project,we are assisting Maria,the chief data scientist for a city school district. Maria is responsible for analyzing information from a variety of sources and in a variety of formats. In this role, she is tasked with preparing all standardized test data for analysis, reporting, and presentation to provide insights about performance trends and patterns.
These insights are used to inform discussions and strategic decisions at the school and district level.We analyse the sudent funding and acedemic scores.

Requirements:

-- Jupyter Notebooks

-- Pandas libraries

-- Os libraries

## Results

As required,we performed various arithmatic and logical operations on the data provied in csv file to get the desired results.Following are the screenshots of some of the analysis work done on the data.




For detailed results and the code please refer to the jupyter notebook file below:
[Challange_book][]


## Analysis process

The whole analysis process is divided into 6 parts

### 1.Collect the Data

To collect the data,we complete the following steps:

Using the Pandas read_csv function and the os module, import the data from the new_full_student_data.csv file, and create a DataFrame called student_df.

Using the head function to confirm that Pandas properly imported the data.

### Deliverable 2: Prepare the Data

To prepare and clean your data for analysis, complete the following steps:

  * Check for and remove all rows with NaN, or missing, values in the student DataFrame.

  * Check for and remove all duplicate rows in the student DataFrame.

  * Use the str.replace function to remove the "th" from the grade levels in the grade column.

  * Check data types using the dtypes property.

  * Remove the "th" suffix from every value in the grade column using str and replace.

  * Change the grade colum to the int type and verify column types.

  * Use the head (and/or the tail) function to preview the DataFrame.
