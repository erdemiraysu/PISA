# PISA
This repo contains an exploratory data analysis I conducted on the 2012 PISA (programme for international student assessment) test scores.

## Dataset

The PISA 2012 represents assessments of academic skills of 485,490 15-year-old pupils, representing 28 million globally from 65 different countries. Rather than examining how well students have learned the school curriculum, PISA looks at how well prepared they are for life beyond school. The data set also contains a wealth of information on students’ demographic background as well as various student attitudes. 

The main dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisa2012.csv.zip), with feature documentation available in this file [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv).

The PISA 2012 Technical Report which describes the methodology underlying the PISA 2012 survey can be found .[here](https://www.oecd.org/pisa/pisaproducts/pisa2012technicalreport.htm), and the codebook with detailed variable documentation can be found .[here](https://www.oecd.org/pisa/pisaproducts/PISA12_stu_codebook.pdf). 

The repo includes:

1. Jupyter notebook file: All of the relationships explored are stored in 'exploration_template.ipynb'. The notebook file first explores every variable independently and then proceeds to the bivariate and multivariate explorations.
2. A smaller subset of the dataset stored in CSV: 'pisa_small.csv'
3. A slide deck presentation focusing on the main findings: 'slide_deck_template.slides'


## Summary of Findings

###  Bivariate Relationships

> EFFECT OF COUNTRY:
- **China** is the leader of outperforming students, followed by **Hong-Kong** and then **Singapore**. The worst performing students, on the other hand, are from **Peru**, **Quatar** and **Indonesia**. 
- Among the 5 mostly developed countries based on the The United Nations Development Report 2019 (1.Norway, 2.Switzerland, 3.Ireland, 4.Germany, 5.Hong Kong-China) **Hong Kong-China** has the highest scores.

> EFFECT OF WEALTH:
- There is a weak but significant correlation between wealth and  scores, which means wealthy counties are doing  better overall in academics. However the relationship is stronger for low wealth students compared with moderate and high wealth students - both of which are not much different from one another. Wealth plays a greater role in academic success for the low wealth families.
- An interesting but UNEXPECTED observation is that: **Quatar**, which is the wealthiest country, has one of the lowest overall scores. On the other hand, **Vietnam**, which is one the poorest countries, has above average overall scores! 
- As expected, OECD member countries  have overall higher scores for all three subjects than non-members.

> EFFECT OF GENDER:
- Females and males perform similarly in math and science, but male students seem to have more highest performing children in especially math (in addition to a very slight median). Females, on the othen hand, outperform the males in reading overall with a higher overall average. This was expected given that females are known to develop language skills earlier than their male peers in early times of childhood.

> EFFECT OF IMMIGRATION STATUS:
- Being a native versus being a second or first generation immigrant does not have a sizeable effect on average. However exceptionally high scores are more dominantly from natives, followed by second generation immigrants, and the first generation immigrants. As a student adapts to a country more (by being born to that country) then they might be more likely to achieve exceptionally high scores. 

> EFFECT OF PARENT EDUCATION LEVEL:
- As expected, as the education level of the parents increase, so does the success of the student. But the effect seems to level out once the parents reach the education level of "upper secondary", with some slight boost for the top education level. 

> EFFECT OF FAMILY STRUCTURE:
- Having a mother or father at home help to achieve higher scores, but specifically "not having amother at home" plays a more negative impact on scores compared with "not having a dad at home". 
- Having siblings does not help with academic success, and there might even be a slight positive effect of NOT having a brother at home on academic success - which is interesting.  
- Living with two parents helps with academic success. Living with one parent is also sufficienct to achieve a level of success that is close. However not living with any parents impacts success negatively.

> EFFECT OF NUMBER OF BOOKS OR COMPUTERS:
- As the number of books or the computers at home increases, so does the level of success. But the effect is stronger for the number of boooks between 0-200 and for the number of computers 0-1.  

> EFFECT OF PERSEVERANCE, SENSE OF BELONGING TO SCHOOL AND TRUANCY:
- As the perseverance of the student increase so does their success, but the relationship is weak. A similar positive correlation seem to exist for belong and scores but even at a much lower rate.
- Truancy seem to be negatively correlated with student scores: The more likely the student to skip a whole day of school, the lower the student's score. 

###  Multivariate Relationships

> EFFECT OF COUNTRY +  WEALTH:
- For Qatar, Norway and UAE - three of the richest countries" higher wealth does not necessarily mean higher scores. In countries Peru, Uruguay, Bulgaria, Slovak Republic and Chile, there is a stronger correlation between wealth and scores. 

> EFFECT OF COUNTRY +  GENDER:
- Overall the way wealth is related to scores in the same way for both genders, But, for example, in Slovak Republic the relationship between wealth and scores is slightly stronger for females than males. This means that wealth has a slightly stronger effect on girls' academic success than boys in this country. 

> EFFECT OF PARENT PRESENCE + WEALTH:
- A combination of high wealth and parent presence leads to highest scores. However, if the mother is NOT at home, the scores drop significantly even for the high wealth students - the size of the drop is not as pronounced under the absecne of the father. 

> EFFECT OF PARENT EDUCATION + WEALTH:
- As the education level of the mother or the father increases, the student is more likely to score incrementally better. But the gain from parent education is higher for students with moderate and high wealth. For students with low level of wealth, even highest parent education level is not sufficient enough to get them to the same level. A combination of moderate-high wealth and higher education results in the highest scores.

> EFFECT OF PARENT EDUCATION + GENDER:
- The gains from an increased level of education from the parents seem to be similar for male or female children overall, but there is a small amount of benefit for the females as the education level increases!

> EFFECT OF COUNTRY + GENDER:
- The countries in which females significantly outperform males are : Quatar, UAE, Jordan, and Thailand - all of which are lower achieveing countries. In other countries there is more gender equity in terms of scores. 

> EFFECT OF PARENT PRESENCE + PARENT EDUCATION:
- The presence of the mother and the father result in similarly higher scores as the education level increases, however absence of the mother from home seem to result in lower scores compared with absence of the father.

> EFFECT OF WEALTH, GENDER + PARENT PRESENCE AT HOME.
- There is increase in scores with increasing wealth overall. However the relationship is strongest when both mother and father are at home, and it is not there any more when the mother and father are NOT at home. More interestingly, female students scores' are slightly more strongly tied to wealth when the mother is "at home" irrespective of whether the father is at home or not. When the mother is not at home, both genders seem to have a similar amount of gain in scores in relation to wealth.

> EFFECT OF TRUANCY + PARENT EDUCATION:
- If the student does not miss any school days, as the mother education increases so does the scores of the child. Hovewer, for those children who miss more than  5 days at school then mother education does not help much for achieving greater scores. Probably other personality or character factors are playing a role here. 

> EFFECT OF PERSEVERANCE + GENDER:
- Perseverance seem to be playing a greater role in males, i.e. males seem to score incrementally higher as their perseverance score also gets higher more than females. 

> EFFECT OF NUMBER OF BOOKS/COMPUTERS + GENDER:
- As the number of books at home increases, the reading scores also increase for both gender, but when there are more than 500 books at home females tend to preserve their high scores while males experience a drop - interestingly. 
- As the number of computers at home increases, the reading scores also increase in a similar way for both genders, but the biggest boost in scores is achieved from  switching from no computer to 1 computer. 


## Key Insights for Presentation

For the presentation, I focus on the variables of **country**, **wealth**, **gender**, **parent education** and **parent presence at home** in relation to the overall **academic scores**. 

- First I display the distributions of math, science and reading scores using histograms, which portray normal distibutions. 
- Then, I create an average academic score for each child taking the average of math, science and reading score, called "Overall Score". 
- Then I plot Mean Overall Academic Scores across Countries using barplots which display countries in the order of their average student score, this way we can have a clear comparison of the countries' average scores to one another. 
- And then I draw the same plot by listing the countries based on their average wealth. This way we are able to pinpoint the rich and poor countries that have (contrasting) low and high scores respectively. 
- And then I bring out the realtionship between wealth and scores using a scatterplot and a bar graph. I create a new variable called wealth range by grouping wealth scores into 3 different bins as low, moderate and high wealth using min, 25%, 75% and max of the distribution, and I use this newly created categporical variable for the bar plot. 
- I move on the to see if there are gender differences in math science and reading scores. Using boxplots allows us to see the distribution of the scores, exceptionally high or low performing student scores in addition to the averages.  
- Using lineplots I investigate how student scores change in relation to higher parent education levels, and at three different levels of wealth. 
- Again, using lineplots I investigate how student scores change in relation to higher parent education levels, when the mother or the father are at home or not. 
- And lastly I also investigate how wealth is related to scores for females and males, when the mother and or the father are at home or not. For this complex investigation of 4 variables I use faceted scatterplots. 


## References used

- https://datatofish.com/correlation-matrix-pandas/
- https://www.kite.com/python/answers/how-to-plot-a-linear-regression-line-on-a-scatter-plot-in-python
- https://worldpopulationreview.com/country-rankings/developed-countries
- https://stackoverflow.com/questions/42579908/use-corr-to-get-the-correlation-between-two-columns
- https://stackoverflow.com/questions/52741236/how-to-calculate-p-values-for-pairwise-correlation-of-columns-in-pandas/52741393#52741393
- https://seaborn.pydata.org/generated/seaborn.FacetGrid.html
- https://seaborn.pydata.org/generated/seaborn.lmplot.html
