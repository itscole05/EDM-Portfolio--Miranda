## Midterm Lab Task 2  Data Cleaning and Transformation Using Power Query
In this task, we were given a raw data with a file named Uncleaned_DS_jobs.csv dataset and tasked with performing data cleaning and transformation using Power Query Editor in Excel.
## STEP 1- Data Cleaning Process ##

- Load the raw file  
- Fit Column and row width and height
  
- TRIM extra spaces
  
- Remove NULL values
  
- Remove Duplicates

## STEP 2- Data Transformation ##

1. Salary Estimate Column:
   
- In Power Query, select the Salary Estimate column.
- Use Transform > Extract > Text Before Delimiter to remove any characters after the open parenthesis.
  
3. Create Min and Max Salary Columns:
   
- Use Add Column > Column from Examples to generate the Min Sal and Max Sal columns from the Salary Estimate column.

4. Salary Estimate Column:
   
- In Power Query, select the Salary Estimate column.
  
- Use Transform > Extract > Text Before Delimiter to remove any characters after the open parenthesis.
  
5. Create Min and Max Salary Columns:
   
- Use Add Column > Column from Examples to generate the Min Sal and Max Sal columns from the Salary Estimate column.
  
- Add Role Type Column.
  
- Go to Add Column > Custom Column and use the formula to categorize job titles into roles like Data Scientist, Data Analyst, Data Engineer, etc.
  
6. Split Location Column:
   
- Select the Location column and use Transform > Split Column by Delimiter (Comma) to split location into separate columns.
  
7. Location Correction:

- Create a custom column to correct location values, replacing certain locations (e.g., "New Jersey" to ", NJ", "California" to ", CA").
  
8. Handle Negative Values:
   
- Filter out negative values in Competitors and Industry columns.
  
9. Clean Company Name:
    
- Remove any unwanted text from the Company Name column using Transform > Replace Values or Remove Text.

## STEP 3 - Screenshots

Before Data Cleaning: (See screenshot of raw data before any transformations were made.)

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Uncleaned_data.jpg" align="center" height="350" width="600"/>



After Data Cleaning: (See screenshot of cleaned data post-transformation.)

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Uncleaned_data.jpg" align="center" height="350" width="600"/>



## STEP 4 - Final Output Queries
Here are the final queries after performing all necessary data transformations:

Sal By Role Type dup: A query with job titles categorized by role type.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Sal%20by%20role%20type%20dup.png" align="center" height="350" width="600"/>


Sal By Size ref: A query focusing on salary data by company size or another metric.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Sal%20by%20size%20ref.png" align="center" height="350" width="600"/>



Sal By State ref: A query analyzing salary data by state/location.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/sal%20by%20state%20ref.png" align="center" height="350" width="600"/>



Uncleaned DS Jobs: The original dataset before any transformations.

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Uncleaned%20DS%20Jobs.jpg" align="center" height="350" width="600"/>



## Physical Data Model ##


(Insert physical data model screenshot here)

<img src="https://github.com/itscole05/EDM-Portfolio--Miranda/blob/main/Midterm%20Lab%20Task%202/images2/Physical%20Model.jpg" align="center" height="350" width="600"/>


