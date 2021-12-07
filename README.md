# SAT Analysis 
##### Thomaz Moon
---

## Problem Statement
---
As part of a group hired by the admissions team for multiple Universities to find out whether the SAT is actually fair to all students,
I have been specifically tasked to find if there is correlation between wealth and test scores. The worry the Universities have comes from
recieving a lot of complaints about students who believe that they are qualified to attend the Universities, and the main difference between
those accepted and them is the SAT score. While my team will has multiple angles to attack this problem from, I will have to report to my
supervisors my findings about **wealth and score** as well as suggestions for any findings that stick out and can or need to be changed.


## Executive Summary
---
This project will explore a total of 5 datasets starting with the *2017 and 2018* data which contains a list of states as well as their participation rate, evidence-based reading and writing, math and total over all score. *Capita_wealth_by_state* which contains the rank of a state based on real per capita personal income, poverty rate on a 3 year average, spending by state and person as well as a state revenue per capita. *Schools scores and more* is a very big datasets with over 60 columns that we will dive deeper into. The information goes from 2005 to 2015 along with the States. Last we have the *Income dist* which simply contains the percentage of each annual household income for the population of the US.  

Exploratory analysis done in this project showed a very strong positive correlation between wealth and the total SAT score. One main possibility is that the more rich someone is, the more likely they are to have parents who are more adjusted to what is needed in order to be successful as well as having the resources to pursue it. Examples would be having their children attend an after school program solely to prepare them for the SAT test, or having them focus only on their studies instead of having to get a job to also help support the family.  

There have also been multiple cases of wealthier parents bribing SAT and college officials to *correct* mistakes on the SAT, give their kids more times on sections, have some of the answers, or simply have people take the test for them,. One recent example of this would be [William Rick Singer](https://en.wikipedia.org/wiki/2019_college_admissions_bribery_scandal) who made over $25 million dollars by accepting bribes. Needless to say, the less well of families can't afford to do these things and therefore will have a higher likely hood of doing worse than those that can.


## Sources
1. [2017 SAT dataset](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/ )
2. [2018 SAT dataset](https://reports.collegeboard.org/archive/sat-suite-program-results/2018/state-results )
3. [Capita Wealth dataset](https://apps.bea.gov/regional/downloadzip.cfm )
4. [School scores and more dataset](https://corgis-edu.github.io/corgis/csv/school_scores/)
5. [Income distribution dataset](https://www.statista.com/statistics/203183/percentage-distribution-of-household-income-in-the-us/)
> One thing to note about the **Capita Wealth** data is that while on the source page a specific year for the rank is not listed, the chamber of commerce has stated that it is from an average of 3 years 2017 - 2019.  


## Data Dictionary For Columns Used
---

| Column | Type| Dataset | Description |
|---|---|---|---|
|**State**| Str | All Datasets| State the Data corresponds to.|
|**Participation**| Int | 2017 & 2018 Dataset| The participation rate of all students by State who took the SAT.|
|**Total**|Int|2017 & 2018 Dataset| The total combined score of the Reading/Writing and Math.|
|**Rank**|Int| Capita Wealth Dataset| The rank of the state based on the Real Per Capita Personal Income.|
|**Real per capita personal income**| Int | Capita Wealth Dataset| The average of how much an individual makes in a year|
|**Year**| Int| School scores and more dataset| Year data is from.|
|**Family Income Less than 20k Test-takers**| Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math less than 20k**| Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Family Income Between 20-40k Test-takers**| Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math 20-40k**|Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Family Income Between 40-60k Test-takers**|Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math 40-60k**|Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Family Income Between 60-80k Test-takers**|Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math 60-80k**|Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Family Income Between 80-100k Test-takers**|Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math 80-100k**|Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Family Income More than 100k Test-takers**|Int| School scores and more dataset| Number of students taking the test that who's total family income is as stated.|
|**Total Reading and Math more than 100k**|Int| School scores and more dataset| Total combined score of reading and writing for wealth bracket.|
|**Total Reading and Math less than 20k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Total Reading and Math 20-40k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Total Reading and Math 40-60k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Total Reading and Math 60-80k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Total Reading and Math 80-100k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Total Reading and Math more than 100k**| Float| School scores and more dataset| Average score of all states within the wealth bracket listed|
|**Average of all**| float| School scores and more dataset| Total average of all wealth groups by year
|**Annual household income in U.S. dollars**| Str | Income distribution dataset | Description of separation of wealth |
|**Percentage of U.S. households**| Float | Income distribution dataset | Percent of US households that fall into the category on the left |


## Conclusions
---
Loading in the 2017 and 2018 datasets to start my search, I was a bit confused as to how some states managed to get a 100% participation rate. After looking online I found out that some states require all students to take the SAT. Although I can understand states wanting to have a higher SAT participation rate, the thing they should really care about is the actual scores because in a scatter plot of 'Total Scores' vs 'Participation', the only states that actually had a decent score, were the ones what had a low participation rate, and in fact the trend line showed that the higher the participation rate, the lower the total score would be. This is also probably due to the fact that people who decided to take the test in the low participation states most likely studied for it beforehand as well as prepared in material for this specific test unlike those who were part of 100% rate and didn't care about their scores.

Although this was a nice insight, this does not shed light onto what I was tasked. In order to see how wealth would affect test scores, I also used the 'Real Per Capita income dataset' and found something that went against my original hypothesis that the wealthier you are, the higher the chance of you getting a better score would on average. Plotting a 'Total SAT Score' vs 'Rank by Capital Wealth', I expected to see a downward trend (As rank 1 would be the richest state); however, I was surprised to see that overall, there was almost no discernable patter between State Wealth and Test Scores.  

Just to be sure that my hypothesis was incorrect I also used the School Scores and more Dataset that had a 11 years (2005 - 2015) worth of data on test scores, as well as scores based on where they compared to others by wealth. At first I expected to see a similar graph on 'Test Scores' vs 'Test taker wealth'; however, the graph instead was very different. For **all** 11 years, there was a positive correlation between wealth and score. Meaning the wealthier always did better than those less fortunate than them. The Score vs Rank by Capital wealth was most likely skewed because instead of looking at individual test takers and their wealth, we instead looked at their average wealth as a whole state where there is a whole range for each state. We also did not take into account the Participation rate when looking at the graph so states with higher participation would most likely get a worse score.  

The next thing I looked at was the participation rate between each wealth group. If there were fewer well off people taking the SAT, then their higher average score would make sense as there would be less chance of bad scores dropping the average. However, What the graph made prominent was the fact that for all years except 2008 and 2009 (presumably because of the Housing Market crash), The group that had the highest participation rate was the richest group, which in our case were people who made over 100k per year.  
As the picture is getting clearer that wealth is one of the biggest factors in the average SAT test scores, I also decided to look at the population percentage of each group, in order to see if the reason the that people who make over 100k annually is the biggest group in population, in which case, the previous graph would make sense. It turns out that they are in fact the highest population group, and proportionally, the population percentage by wealth in the U.S. is actually close to the test taker population by wealth.  

Overall this does not change the fact even though the wealthiest group almost always had the highest Test Taker population, they also ALWAYS scored the highest throughout the entire 2005 - 2015 year period (The entire length of time the SAT was out of 2400). What the data analysis shows is that wealth is in fact correlated to the test scores. Not only because of advantages such as the William Singer case above, but because of ability to acquire necessary materials and resources to study and prepare for the test.

### Recommendations
---
1. Get rid of the SAT as a whole
  * This option might be unrealistic at the moment because it will most likely just be replaced with another standardized test that will end up having similar issues, but one that can be worked towards by having Colleges and Universities  only look at the student's high school transcripts and extra curriculars with no additional testing.
2. Have an elective class in high school that will prepare the students specifically just for the SAT.
  * While this won't change the fact that the wealthier students will be able to get outside help, it will help those who are less fortunate at the very least have a better chance, as well as giving direction on how to study for it.
3. Make the test free for those who score below 1150 (example number).
  * Not only will this make college board more likely to push students and provide cheaper or even free materials in order to have a better pay in long run by having more people hit the target score, but those who are less fortunate can take the test multiple times getting a feel for it in a real test environment that they might not have been able to receive before.
  * Although College board might a company and focus on making money, the fact that many students and schools depend on a fair testing and are not getting it puts the blame back onto the College Board for not doing the job that they were tasked on doing, possibly ruining chances for students that would have gotten into their dream school otherwise.
