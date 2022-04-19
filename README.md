# School District Analysis
Analysis of student funding and students standardized tests scores to make decisions regarding school budgets and priorities.We are using Python and Jupyter Notebook along with The Pandas Library. 

## Overview of the school district analysis: 
### Background
After the complete analysis of the school district student data,the grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent of this academic integrity violation, they want to uphold the standards of state testing and have turned to us for help.After assessing the situation with the school superintendent and Maria, we decide the best approach is to:
Replace the ninth-grade math and reading scores from Thomas High School and Keep all other data associated with the ninth-grade students and Thomas High School intact.

Analysis is done in the Jupyter Notebook in the PyCitySchools_Challenge.ipynb file.

Objectives
The goals of this challenge are:
Filter DataFrames using logical operators.
Replace the incorrect values with NaN.
Explain how our PyCitySchools analysis changes after we handle the incorrect data.

- After creating a duplicate of PyCitySchools.ipynb and renaming it PyCitySchools_Challenge_testing.ipynb; we corrected the students names so there are no professional prefixes or suffixes.
Also, replaced the reading and math scores for ninth graders at Thomas High School with NaN
We used the pandas.DataFrame.loc to equate the math and reading scores of 9th graders from Thomas High School to np.nan.To use np.nan, we need to import Numpy.

#### Original District Summary DataFrame with the analysis in the module is as below:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Original%20Student%20Data.png)

After we replaced the reading and math scores for ninth graders at Thomas High School with NaN, DataFrame looks like as below:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Clean%20Student%20Data_NaN.png)

After merging the clean student data with the school dataset and checking the column order for all the DataFrames and number formatting same as what was covered in this module, we started analysis on it.
After replacing the reading and math scores,and recreating the district and school summary DataFrames we have to analyse by answering the questions for each step.


### How is the district summary affected?

- Before DATA Cleanup:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Initial%20District%20Summary.png)

Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing are:

79.0, 81.9, 75, 86, 65

- After DATA Cleanup:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/District%20Summary%20After%209th%20grade%20NaN.png)

Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing are:

78.9, 81.9, 74.8, 85.7, 64.9

#### Observation: Slight downward change in district averages

### How is the school summary affected?

- Before DATA Cleanup: 

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/original%20school%20listings%20by%20performance.png)

Thomas High School's % Overall Passing = 91, placing second
- After DATA Cleanup:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Top%20Schools%20after%20NaN.png)

 % Overall Passing = 65, placing eighth!

### Observation: Overall ranking order change due to THOMAS HS, which slipped from second to eighth position.

### How does replacing the ninth-grade scores affect the following:

For this we have to analyse How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?

- Before Cleanup:original math and reading scores were

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Math%20and%20Reading%20scores_original.png)

- After Cleanup:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Math%20and%20Reading%20scores%20after%20NaN.png)

### Observation: It shows 9th grade column as NaN and rest of the grade scores remains the same.

### Math and reading scores by grade
"Percentage passing" score is reduced as Total number of students (denominator) remains unchanged, but total passing value (numerator) is reduced by the number of removed 9th grade scores.(461)
Thomas HS 9th grade math & reading scores set to "NaN"
Totals for passing math & reading across grades are reduced as all of 9th grade scores are equivalent to failing
Average scores calculation not significantly affected by removal of 9th grade scores, seems due to count() function NOT including 9th grade scores = nan
We calcuated number of students with a math grade
- Before cleanup: Thomas High School       1635

- After cleanup: Thomas High School       1174

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/School%20Summary%20before%20academic%20integrity%20violation.png)

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/School%20Summary%20After%20NaN.png)

### Scores by school spending

Thomas HS is in the spending bucket "$630-644"

Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644" as follows

- Before: 

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Spending%20Ranges%20per%20student_original.png)

- After: 

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Scores%20by%20School%20Spending_NaN.png)

### Observation : Scores are not substancially affected.

### Scores by school size

Thomas HS is in the "Medium (1000-2000)" size bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)" as follows
- Before:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Performance%20by%20school%20size_original.png)

- After: 

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Scores%20by%20School%20Size_NaN.png)

### Observation : Scores are not substancially affected.

### Scores by school type

Thomas HS is in the "CHARTER" type bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER" as follows
- Before:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Performance%20by%20school%20type_original.png)

- After: 

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Scores%20by%20School%20Type_NaN.png)

### Observation : Scores are not substancially affected.

### Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
Overall ranking order change due to THOMAS HS, which slipped from second to eighth position. In case of Math and Reading scores, as 9th grade scores are NaN , analysis of the school records based on school spending, school size, and school type are not substancially affected.

