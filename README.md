# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Does Poverty Affect Standardized Test Performance?

### Overview

This project covers:
- Basic statistics and probability
- Many Python programming concepts
- Programmatically interacting with files and directories
- Visualizations
- EDA
- Working with Jupyter notebooks for development and reporting

---

### Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

School funding in California comes from federal, state, and local sources. As California relies heavily on income taxes for funding, there is a large funding gap between wealthy and impoverished school districts. Due to systematic racism and neighborhood segregation within California, high-poverty school districts serve primarily Black and Latinx students ([*source*](https://edpolicyinca.org/publications/californias-education-funding-crisis-explained-12-charts)). School districts with high poverty rates may have worse performance rates on standardized testing, which further exacerbates the uneven playing field between wealthy, primarily white students and low-income students of color with regards to college admissions. ([*source*](https://www.nytimes.com/2020/05/23/us/SAT-ACT-abolish-debate-california.html))

The state of California would like to use the 2019 ACT and SAT scores to analyze if there is a relationship between poor performance on the SATs and ACTs and poverty rates in order to recommend programs and allocate more resources to school districts with the greatest needs.

---

### Problem Statement

Many universities are no longer using standardized testing scores in admission decisions, stating that the tests put low income students at a disadvantage. The aim of this project is to see if there is a relationship between student performance on the ACTs and SATs and poverty rates across school districts in California in order to allocate greater funding to school districts in need and make standardized testing more equitable.

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**county_code**|*string*|ACT 2019 CA/ SAT 2019 CA|The unique ID of the County that the School District belongs to.|
|**district_code**|*string*|ACT 2019 CA/ SAT 2019 CA|The unique ID of the California School District.|
|**district_name**|*string*|ACT 2019 CA/ SAT 2019 CA|The name of the California School District.|
|**county_name**|*string*|ACT 2019 CA/ SAT 2019 CA|The name of the County that the School District belongs to.|
|**enrolled_seniors**|*integer*|ACT 2019 CA/SAT 2019 CA|The number of 12th grade students enrolled in the School District in 2018-2019 school year, averaged from SAT and ACT records.|
|**sat_tested_seniors**|*integer*|SAT 2019 CA|The number of 12th grade students in the School District that took the SATs in 2018-2019.|
|**sat_num_above_benchmark**|*integer*|SAT 2019 CA|The number of 12th grade students in the School District that have a combined Maths and ERW score above the mean benchmark set by the College Board for the SATs in 2018-2019.|
|**sat_pct_above_benchmark**|*float*|SAT 2019 CA|The percentage of 12th grade students in the School District that have a combined score above the mean benchmark set by the College Board for the SATs in 2018-2019.|
|**act_tested_seniors**|*integer*|ACT 2019 CA|The number of 12th grade students in the School District that took the ACTs in 2018-2019.|
|**act_num_above_benchmark**|*integer*|ACT 2019 CA|The number of 12th grade students in the School District that have a combined score above the mean benchmark set by the College Board for the ACTs in 2018-2019.|
|**act_pct_above_benchmark**|*float*|ACT 2019 CA|The percentage of 12th grade students in the School District that have a combined score above the mean benchmark set by the College Board for the ACTs in 2018-2019.|
|**population_total**|*integer*|SAIPE 2019 Census|The estimated number of people in the School District in 2019.|
|**population_5_to_17**|*integer*|SAIPE 2019 Census|The estimated number of children between 5 to 17 years old in the School District in 2019.|
|**population_5_to_17_poverty**|*integer*|SAIPE 2019 Census|The estimated number of children between 5 to 17 years old living in poverty in the School District in 2019.|
|**sat_participation_pct**|*float*|SAT 2019 CA|The percentage of 12th graders in the School District who took the SATs out of the total number of 12th graders enrolled in the School District in 2018-2019.|
|**act_participation_pct**|*float*|ACT 2019 CA|The percentage of 12th graders in the School District who took the ACTs out of the total number of 12th graders enrolled in the School District in 2018-2019.|
|**5_to_17_poverty_pct**|*float*|SAIPE 2019 Census|The estimated percentage of children between 5 to 17 living in poverty out of the total number of children between 5 to 17 in the School District in 2019.|

---

### Summary of Analysis

Based on my analysis, there is a strong negative correlation between the percentage of children in a school district that are between 5 to 17 years old and living in poverty, and the percentage of seniors in a school district scoring above the benchmark for both SATs and ACTs. As the percentage of children living in poverty increases, the percentage of seniors that score above the benchmark for both the SATs and ACTs decreases. This implies a relationship between wealth and performance on standardized testing.

The percentage of seniors that score above the benchmark for the SATs and ACTs seems almost perfectly correlated. This is unsurprising, as they are both standardized tests in very similar subjects, so high performers for one test would likely score well on the other as well.

It is also worth noting that the mean number of seniors that take the SATs is almost double the mean number of seniors that take the ACTs (A mean of 500 seniors take the SATs per school district, compared to a mean of 244 seniors take the ACTs per school district). Even so, a higher percentage of students score above the benchmark for the ACTs than the SATs. While the mean percentage of students that score above the benchmark for the ACTs is 57% across California school districts, the mean percentage for the SATs is only 49%.

---

### Conclusion and Recommendations

Based on the analysis, there is a very strong correlation between the percentage of students that score above the benchmark set by the Collegeboard for both the SATs and ACTs, and the number of children between the age of 5 to 17 years old living in poverty.

There are many reasons why school districts with higher levels of poverty may perform worse on standardized tests. This includes reasons such as:
> 1. Wealthier students will have access to private tutors and external standardized test preparation courses
> 2. Wealthier students can afford to retake the test several times
> 3. Wealthier students will have access to Advanced Placement (AP) courses and are enrolled in schools with greater funding that will provide better educational support to students

More background on these reasons can be found [here](https://www.cnbc.com/amp/2019/10/03/rich-students-get-better-sat-scores-heres-why.html).

As the SATs are more popular than the ACTs, and students typically perform worse on the SATs, I would recommend allocating resources towards programs with an emphasis on improving SAT test scores.

I would recommend increasing funding to the following six school districts in California:
>- Cutler-Orosi Joint Unified
>- Coachella Valley Unified
>- Wasco Union High
>- Lynwood Unified
>- Lawndale Elementary
>- Inglewood Unified

My recommendations to the six school districts above are based on the following criteria:
> 1. The number of students that took the ACTs and SATs in these districts are above the 25th percentile, therefore we are providing funding to school districts where we can impact a sufficient number of test takers
> 2. The percentage of students that took the ACTs and SATs in these districts are above the 25th percentile, therefore we are providing funding to school districts where we can impact scores for a high percentage of the students in the district
> 3. The school districts chosen are all in the lowest 20 performing districts for both the SATs and ACTs
> 4. The school districts chosen are in the top 20 districts with the highest percentage of children living in poverty
