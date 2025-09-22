Data Cleaning — Netflix Titles (Task 1)

Author: Abhishek Patil   
Dataset: Netflix Movies and TV Shows (`netflix_titles.csv`)

A. Objective:
The goal of this task was to clean and preprocess a raw dataset by handling missing values, duplicates, inconsistent formats, and ensuring the dataset is ready for analysis.

B. Cleaning Steps Performed:
1. Column Names Standardization
   - Converted all column names to lowercase with underscores (snake_case).  

2. Duplicates
   - Checked and removed duplicate rows.  

3. Missing Values
   - `director`, `cast`, `country` → filled with `"Unknown"`.  
   - `rating` → filled with `"Unrated"`.  
   - `duration` → filled with `"Unknown"`.  
   - `date_added` → converted to datetime; rows with missing values dropped.  

4. Text Standardization
   - `type` → converted to lowercase (`movie`, `tv show`).  
   - `country` → converted to title case (e.g., `"united states"` → `"United States"`).  
   - Cleaned spacing and formatting in `listed_in`, `title`, and `description`.  

5. Date Handling
   - Converted `date_added` column into proper datetime format.  

6. Duration Handling
   - Extracted numeric duration into `duration_number`.  
   - Extracted unit (`min`, `season`) into `duration_unit`.  

7. Rating Normalization
   - Converted all ratings to uppercase.  
   - Standardized variants like `NR` or `Not Rated` → `Unrated`.  

C. Dataset Overview
- Original Shape: (8807, 12)  
- Final Shape: (fill in your final shape from Colab, e.g., (8797, 14))  
- New Columns Added: `duration_number`, `duration_unit`  


D. Outcome
A cleaned, well-structured dataset ready for further analysis and visualization.

