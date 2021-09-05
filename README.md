# School_District_Analysis

## Overview

### Purpose
> The school board has notified Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. She has asked you to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once you’ve replaced the math and reading scores, Maria would like you to repeat the school district analysis that you did in this module and write up a report to describe how these changes affected the overall analysis.

The purpose of this analysis was to familiarize us with using Jupyter Notebook and Pandas, which is a very powerful Python data analysis library. We learned how to clean data, by finding missing values, and learning to replace/drop them. Additionally, we also replaced partially incorrect data values that had student names with  unneeded prefixes and suffixes. Other key learning points were creating and merging dataframes, learning to format individual columns to be more visually pleasing to the eye, and also splitting dataframes by groupby() and bins, categorizing and grouping by bins, and finally creating new dataframes from this manipulated data.

## Results
### District Summary
  - Minor changes overall, slight decreases for most of the values. District summary dataframes from before and after replacement of Thomas High School's ninth graders are below. (Before replacement on top, after replacement on bottom).

    - Total students slightly decreased from 39,170 to 38,709
    - Average math score decreased from 79.0 to 78.9.
    - Average reading score stayed the same, 81.9 throughout. 
    - Percentage passing math decreased from 75.0% to 74.8% 
    - Percentage passing reading decreased from 85.8% to 85.7%. 
    - Overall passing percentage decreased from 65.2% to 64.9%.

![District Summary Before](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/district_summary_before.png)
![District Summary After](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/district_summary_after.png)
***
### School Summary
- Minor changes overall in all the values. Thomas High School summary dataframes before and after replacement of the ninth graders are below. (Before on top, after on bottom). 
  
  - Average math score decreased from 83.41 to 83.35. 
  - Average reading score increased from 83.84 to 83.89. 
  - Percentage passing math decreased from 93.27% to 93.18%. 
  - Percentage passing reading decreased from 97.30% to 97.01%. 
  - Overall passing percentage decreased from 90.94% to 90.63%. 

![Thomas High School Summary Before](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/thomas_before.png)
![Thomas High School Summary After](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/thomas_after.png)
***
### Thomas High School performance
  - After the replacement of the ninth graders' scores, although Thomas High School's performance has slight changes, it still remained the #2 ranked school overall. Thomas High School stayed behind Caberera High School and ahead of Griffin High School. 
  - Top High School summary dataframes before and after replacement of Thomas High School ninth graders are below. (Before on top, after on bottom). 

![Top School Summary Before](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/top_performing_schools_before.png)
![Top School Summary After](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/top_performing_schools_after.png)

### Effect of replacing ninth grade scores
#### Math and reading scores by grade: 
  - Nothing in particular changed besides the 9th grade column under Thomas High School for both math and reading scores having NaN instead of a value. 
  - Example of math scores after replacement below.

![Math Scores After](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/math_scores_after.png)
***
#### Scores by school spending
  - Despite technically not counting the ninth-grade students' results, Thomas High School remains in bin $630-644. If the new student count excluding the ninth graders had actually been used, then Thomas High School would have been in an undefinable bin outside of the split. However, the ninth graders were still students during this time and more was not spent on 10th-12th graders as a result, the bin does not change. 
  - Due to this and the fact that we were rounding the final result, not that much actually changed. There were slight increases and decreases of scores in spending range $585-$629 and $630-644. 
![Spending Passing Before](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/spending_passing_before.png)
![Spending Passing After](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/spending_passing_after.png)
***
#### Scores by school size
  - Due to rounding the final result, there was no difference between before and after removing Thomas High School's ninth graders.

![Size Passing](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/size_passing.png)
***
#### Scores by school type
  - There was no difference between before and after removing Thomas High School's ninth graders because school type is not affected by this.

![Type Passing](https://github.com/li-emily/School_District_Analysis/blob/main/Resources/Images/type_passing.png)
## Final summary
After the reading and math scores for the ninth graders at Thomas High School were replaced with NaNs due to potential academic dishonesty, Thomas High School had drastic drops in their overall scores. This was due to the fact that the school was still counting the number of ninth graders in the the overall student count despite their lack of grade. If we had continued to calculate school performance based on this, it would have skewed the results. Thus, we decided to remove the ninth graders' scores from consideration, and from calculations involving Thomas High School and the overall district.

As a result, we were able to see that school district had slight decreases in almost every category. Thomas High School had similar minor decreases across all categories (but a slight increase in average reading score). However, even after removing the ninth graders, Thomas High School remained as number two school for the district. This shows that Thomas High School has strong students in every grade, performing well across the board.

We did not remove Thomas High School's ninth graders from the school's overall student count, as it would have influenced scores by school spending by moving Thomas High School into an unidentifable bin as mentioned.  While the student count did not change, this also had no effect on scores by school size, as the school itself would have stayed in the Medium bin. The number of students at Thomas High School even with removal would have stayed between 1000 - 2000 students. Thus, there was no great need to do unnecessary changes. Finally, the school type of Thomas High School obviously remains the same regardless of any student activity.
