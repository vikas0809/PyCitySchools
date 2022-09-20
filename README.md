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

      full_student_data = os.path.join('Resources/new_full_student_data.csv')
      student_df = pd.read_csv(full_student_data)

Using the head function to confirm that Pandas properly imported the data.
          
      student_df.head()
      
      
      
      
      

### Deliverable 2: Prepare the Data

To prepare and clean your data for analysis, complete the following steps:

  * Check for and remove all rows with NaN, or missing, values in the student DataFrame.

            # Check for null values
            student_df.isna().sum()
            
            # Drop rows with null values and verify removal
            c1_student_df=student_df.dropna(how = 'any')
            c1_student_df.isnull().sum()


  * Check for and remove all duplicate rows in the student DataFrame.

            # Check for duplicated rows
            c1_student_df.duplicated().sum()
            
            # Drop duplicated rows and verify removal
            c2_student_df = c1_student_df.drop_duplicates()
            c2_student_df.duplicated().sum()

            
            # Examine the grade column to understand why it is not an int
            c2_student_df['grade']
            
         
            
  * Check data types using the dtypes property.

            # Check data types
            c2_student_df.dtypes
            
  * Remove the "th" suffix from every value in the grade column using str and replace.
  
             # Remove the non-numeric characters and verify the contents of the column
            c2_student_df["grade"]=c2_student_df['grade'].str.replace("th","")
            c2_student_df['grade']
            
  * Change the grade colum to the int type and verify column types.

            c2_student_df['grade']=c2_student_df['grade'].astype(int)

  * Use the head (and/or the tail) function to preview the DataFrame.

            c2_student_df.tail(5)
 
 
 ### Summarize the Data
 
Describe the data using summary statistics on the data as a whole and on individual columns.

   * Generate the summary statistics for each DataFrame by using the describe function.

   * Display the mean math score using the mean function.

   * Store the minimum reading score as min_reading_score.
