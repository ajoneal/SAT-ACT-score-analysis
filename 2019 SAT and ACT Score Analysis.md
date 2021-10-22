# 2019 Standardized Test Analysis for Recruiting High Performing Students


### Problem Statement

**Top colleges recruit high performing high school students and require higher test scores for those students to be able to get into their school. This project aims at helping those colleges find where they can recruit more high performing students based on standardized test scores across the country and allocate more marketing resources to those states.**

---

### Data

* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))

#### Additional Resources
*An article from the Washington Post states that colleges spend billions on marketing themselves to potential students.*(https://www.washingtonpost.com/local/education/colleges-marketing-student-recruitment/2021/09/30/b6ddd246-2166-11ec-8200-5e3fd4c49f5e_story.html)

---

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|*object*|ACT/SAT|State where the SAT/ACT data is compiled for|
|sat_participation_rate|*float*|SAT|Participation rate for the SAT test for the state(units to 2 decimal places between 0 and 1 where 0.07 means 7%)|
|read_and_write_score|*integer*|SAT|Average Evidence-Based Reading and Writing score for the state|
|math_score|*integer*|SAT|Average Math score for the state|
|total_sat_score|*integer*|SAT|Average Total SAT score for the state (combination EBRW and Math score)|
|act_participation_rate|*float*|ACT|Participation rate for the ACT test for the state(units to 2 decimal places between 0 and 1 where 0.07 means 7%)|
|composite_score|*float*|ACT|Average Total ACT score for the state|

---

### Cleaning and Analysis

#### Cleaning
**When reviewing the data, I noticed there were more that 50 entries for both SAT and ACT data sets.  I found and removed US territories from the SAT data and the national average from the ACT data.  I also checked to ensure that all state score averages fell within the range of the the respective standardized test (which they did).  There were no missing values in the data and I converted the participation rate data type for each test to allow for better analysis.  I ensured that the average Evidenced-Based Reading and Writing and average Math score for the SAT added up to the total average for the SAT score for each state.  There were a few states where the sum of the EBRW and Math score were 1 point higher or lower than the total average SAT score, but I assumed that was due to a rounding error and didn't feel there was a need to adjust the average total score.  The two data sets were then merged for further analysis.**

#### Analysis
* **SAT and ACT participation rates are negatively correlated. When SAT participation increased, ACT participation decreased. Certain states seem to focus on one test and not so much on the other.**
* **Out of the top 10 SAT-scoring states, 8 of those states are in the bottom 10 for SAT participation rate.**
* **Out of the top 10 ACT-scoring states, 7 of those states are in the bottom 10 for ACT participation rate.**
* **The top 10 scoring states in the SAT and ACT have average participation rates of 3.2% and 19.6% respectively. There seems to be a negative correlation between scores and participation rates. Therefore, in order to find the top scoring states for each test, we need to ensure a majority of the students are participating in that test.**
* **Massachusetts, New Jersey, and Vermont are all states that fall within the top 10 for average SAT scores with a minimum of 50% participation rate in the SAT test. They also fall in the top 10 for ACT scores regardless of participation. Although a majority of the students in these states tend to take the SAT test, the ones that take the ACT perform well also.**
* **Iowa, Kansas, Minnesota, Missouri, Nebraska, South Dakota, and Wisconsin are all states that fall within the top 10 for average ACT scores with a minimum of 50% participation rate in the ACT test. They also fall in the top 10 for SAT scores regardless of participation. Although a majority of the students in these states tend to take the ACT test, the ones that take the SAT perform well also.**

---

### Conclusions and Recommendations

**Based on the most recent data prior to the pandemic for SAT and ACT scores and participation by state in 2019, we can conclude a few things.  First, we can see a clear negative relationship between the participation rates of each test meaning that if a state has a high participation rate in one test, they tend to have a low participation rate in the other test.  This is likely because each state tends to focus students more on one test when preparing for college than the other.  Next, we also see a negative relationship between a given test's scores and the participation rate for that test for both the SAT and ACT.  This is likely because when states push more students to take a test (including those that do not want to take it), it will push down the average test score for the state.**

**When adding a participation filter to ensure that a majority of the students in the state were taking a given test, we discovered the top 10 scoring states based on participation and compared them with the top 10 scoring states overall for each test.  Although none of the top 10 scoring states based on participation for the SAT and ACT were in the top 10 scoring states overall for their respective tests, there were some top 10 scoring states based on participation for the SAT that were also in the top 10 scoring overall states for the ACT and vice-versa.  MA, NJ, and VT were states that fell in the top 10 SAT-scoring states based on participation and were also in the top 10 overall states for ACT scores as well (although that had low participation in the ACT test).  IA, KS, MN, MO, NE, SD and WI were states that fell in the top 10 ACT-scoring states based on participation that were also in the top 10 overall states for SAT scores as well (although they had low participation in the SAT test).  High performing, motivated students in these states may have decided to take both test to increase their chances of getting into target schools.**

**Based on the data, I would recommend colleges invest marketing resources to some or all of the following states if they are looking to recruit students who perform better on standardized tests:  Massachusetts, New Jersey, Vermont, Iowa, Kansas, Minnesota, Missouri, Nebraska, South Dakota, or Wisconsin**

---

### Presentation Link



---

