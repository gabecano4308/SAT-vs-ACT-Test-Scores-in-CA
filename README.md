# Why California Should Focus on the ACT Over the SAT in 2020-21

### Overview
For this project, I assume the role of a data scientist hired by the California Department of Education to help determine whether to focus more of its yearly budget towards SAT or ACT promotion.

With this mission in mind, the project compares, synthesizes, and analyzes information from the California 2018-19 SAT and ACT datasets. The two original datasets are provided by the California Department of Education and can be found on its [website](https://www.cde.ca.gov/ds/sp/ai/). The analysis determines if placing more emphasis on participation in one test over the other could make improved overall test score averages more likely for high school seniors in California.

### Problem Statement
>Every year, high schools in California allot considerable resources to improve the standardized test scores of their students [(source)](https://www.theatlantic.com/education/archive/2015/06/should-the-sat-be-part-of-school/395417/), since those scores play a significant role in college admission and curriculum development [(source)](https://global.act.org/content/global/en/products-and-services/the-act-non-us/scores/how-schools-use-the-act.html). This project analyzes participation rates and benchmark achievement averages for the SAT and ACT from schools across California to recommend whether the state should invest more funding on SAT or ACT programs.

### Background
The SAT and ACT are standardized tests that colleges in the United States request for their admissions processes. Colleges holistically factor in applicants' test scores along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)), while the ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)).

Certain colleges and universities, including UC schools, are taking away the SAT/ACT requirements for their applications due in part to the belief that the tests unfairly discriminate against students of lower socio-economic status[(source)](https://www.insidehighered.com/admissions/article/2020/11/02/appeals-court-upholds-ruling-barring-use-sat-and-act-u-california). However, there are still various colleges in the United States that require or at least recommend inclusion of SAT or ACT scores in a student's application [(source)](https://www.insidehighered.com/admissions/article/2020/11/02/appeals-court-upholds-ruling-barring-use-sat-and-act-u-california).

### Methodology
* The two datasets provided by the California Department of Education were cleaned and merged into one larger dataset containing both ACT and SAT data for schools across California.
* Statistical summaries were calculated and compared between data points relating to average test scores and participation rates across California.
* Primary findings were visualized using a variety of graphs and charts, in order to better communicate insights with a non-technical audience.

### Datasets

##### Provided Datasets
* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutact19.asp))
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutsat19.asp))

##### Dataset Created During Project
* [`ca_sat_act_19.csv`](./data/ca_sat_act_19.csv): contains cleaned information merged from the two originally provided datasets, sourced above. Data Dictionary is listed below.

### Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**school**|*object*|ca_sat|CA school name|
|**district**|*object*|ca_sat|CA district name|
|**county**|*object*|ca_sat|CA county name|
|**snr_enroll**|*float*|ca_sat|Senior enrollment size|
|**sat_snr_testers**|*float*|ca_sat|Number of senior SAT testers|
|**sat_num_erw_bm**|*float*|ca_sat|Number of seniors meeting the Evidence-Based Reading & Writing (ERW) SAT benchmark|
|**sat_pct_erw_bm**|*float*|ca_sat|Percent of seniors meeting the Evidence-Based Reading & Writing (ERW) SAT benchmark|
|**sat_num_math_bm**|*float*|ca_sat|Number of seniors meeting the Math SAT benchmark|
|**sat_pct_math_bm**|*float*|ca_sat|Percent of seniors meeting the Math SAT benchmark|
|**sat_num_both_bm**|*float*|ca_sat|Number of seniors meeting both the ERW and Math SAT benchmarks|
|**sat_pct_both_bm**|*float*|ca_sat|Percent of seniors meeting both the ERW and Math SAT benchmarks|
|**sat_pct_participation**|*float*|ca_act|CA SAT participation for senior grade|
|**act_snr_testers**|*float*|ca_act|Number of senior ACT testers|
|**act_avg_read_scr**|*float*|ca_act|Average senior ACT Reading test score|
|**act_avg_eng_scr**|*float*|ca_act|Average senior ACT English test score|
|**act_avg_math_scr**|*float*|ca_act|Average senior ACT Math test score|
|**act_avg_sci_scr**|*float*|ca_act|Average senior ACT Science test score|
|**num_act_benchmark**|*float*|ca_act|Number of senior testers whose ACT composite scores are at least 21 points|
|**pct_act_benchmark**|*float*|ca_act|Percent of senior testers whose ACT composite scores are at least 21 points|
|**act_pct_participation**|*float*|ca_act|CA ACT participation for senior grade|

### Conclusion from Analysis  
#### Key Takeaways:
* ACT participation is much lower than that of the SAT in CA, which shows there's ample room for growth for ACT participation numbers
* CA seniors in 2018-19 performed slightly better on the ACT than on the SAT overall in terms of the percent who reached a benchmark score.
* Students struggled more with SAT Math than with ACT Math when compared proportionately to those tests’ other sections

#### Recommendation:
The California Department of Education should invest more of its resources on increasing ACT testing in schools across the state. This change will likely raise overall benchmark achievement rates for its seniors.
