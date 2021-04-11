# Marketing Analysis
Dataset was taken from [Kaggle](https://www.kaggle.com/jackdaoud/marketing-data).
This data set was provided to students for their final project in order to test their statistical analysis skills as part of a MSc. in Business Analytics.

This is data about retail shop clients and advertising campaigns it have conducted.

## Goal
Improve and strengthen skills in data analysis.
## Achievements
Completed all tasks provided by dataset creator, applied statistic methods to make conclusions on data. Have built dashboards in Tableau for the 4th section.

**Analyst report is presented here in md file**

**All data preparation, cleaning etc. are available in [jupyter notebook](https://nbviewer.jupyter.org/github/ahinski/marketing-analysis/blob/main/analysis.ipynb).**

## Tasks
You're a marketing analyst and you've been told by the Chief Marketing Officer that recent marketing campaigns have not been as effective as they were expected to be. You need to analyze the data set to understand this problem and propose data-driven solutions.

### Section 01: Exploratory Data Analysis
* Are there any null values or outliers? How will you wrangle/handle them?
* Are there any variables that warrant transformations?
* Are there any useful variables that you can engineer with the given data?
* Do you notice any patterns or anomalies in the data? Can you plot them?

### Section 02: Statistical Analysis
Please run statistical tests in the form of regressions to answer these questions & propose data-driven action recommendations to your CMO. Make sure to interpret your results with non-statistical jargon so your CMO can understand your findings.

* What factors are significantly related to the number of store purchases?
* Does US fare significantly better than the Rest of the World in terms of total purchases?
* Your supervisor insists that people who buy gold are more conservative. Therefore, people who spent an above average amount on gold in the last 2 years would have more in store purchases. Justify or refute this statement using an appropriate statistical test
* Fish has Omega 3 fatty acids which are good for the brain. Accordingly, do "Married PhD candidates" have a significant relation with amount spent on fish? What other factors are significantly related to amount spent on fish? (Hint: use your knowledge of interaction variables/effects)
* Is there a significant relationship between geographical regional and success of a campaign?

### Section 03: Data Visualization
Please plot and visualize the answers to the below questions.

* Which marketing campaign is most successful?
* What does the average customer look like for this company?
* Which products are performing best?
* Which channels are underperforming?

### Section 04: CMO Recommendations
* Bring together everything from Sections 01 to 03 and provide data-driven recommendations/suggestions to your CMO.

# Report
Exploratory analysis showed that there were some duplicated clients in data (they had same income, education and join date) but still they had different countries, so the last inputed information was used in following analysis. Missed and outlier values in income section were filled with mean for clients with similar characteristics.

**New users by month**
![image](https://user-images.githubusercontent.com/43516629/114301414-6e092b80-9acd-11eb-8463-54ebada65472.png)
The flow of new customers is stable through time

**About 600 clients have accepted at least one campaign offer**
![image](https://user-images.githubusercontent.com/43516629/114301482-ce986880-9acd-11eb-92c9-2a2006cfc729.png)

**But most of them haven't accepted any**
![image](https://user-images.githubusercontent.com/43516629/114301492-d952fd80-9acd-11eb-951a-2911c407196c.png)

#### What factors are significantly related to the number of store purchases?
The most significant factors are income and number of children.
**Catalog purchases by income**
![image](https://user-images.githubusercontent.com/43516629/114301597-3b136780-9ace-11eb-99c9-7a9f4ccd6965.png)

**Store purchases by income**
![image](https://user-images.githubusercontent.com/43516629/114301642-77df5e80-9ace-11eb-9d47-029e34f762ed.png)

Less signifcantly income factor affects purchases from web
**Web purchases by income**
![image](https://user-images.githubusercontent.com/43516629/114301646-7ada4f00-9ace-11eb-8b0b-8274c9783418.png)

Clients with more children make more deals with disctount
![image](https://user-images.githubusercontent.com/43516629/114301663-8fb6e280-9ace-11eb-88bd-b00c1e36d420.png)

#### Does US fare significantly better than the Rest of the World in terms of total purchases?
**Average number of purchases made by client from Rest of the World and US**
![image](https://user-images.githubusercontent.com/43516629/114301707-afe6a180-9ace-11eb-913a-5e0c137e2289.png)

There is no enough statistical significance to say that US fate better than other world.

#### Your supervisor insists that people who buy gold are more conservative. Therefore, people who spent an above average amount on gold in the last 2 years would have more in store purchases.

**Number of store purchase by amount of gold bought**
![image](https://user-images.githubusercontent.com/43516629/114301861-3307f780-9acf-11eb-879f-44f72aa565a7.png)

With confidence level of 95% people who buy gold make more store purchases.

#### Fish has Omega 3 fatty acids which are good for the brain. Accordingly, do "Married PhD candidates" have a significant relation with amount spent on fish? 
**Fish product bought for 2 client clusters**
![image](https://user-images.githubusercontent.com/43516629/114301985-baee0180-9acf-11eb-8d71-46db8969ba2a.png)

With confidence level of 95% despite our predictions married clients with PhD spend less money on fish products.

#### Is there a significant relationship between geographical regional and success of a campaign?

Percentage of clients accepted the offer by country
![newplot](https://user-images.githubusercontent.com/43516629/114302060-0dc7b900-9ad0-11eb-8688-a491f9e7aa8c.png)

Number of clients accepted the offer by country
![newplot (1)](https://user-images.githubusercontent.com/43516629/114302077-1b7d3e80-9ad0-11eb-8779-545e3d8e9d78.png)

Clients from Spain are the most active in terms of accepting campaign offers. Other countries (except Mexico, from where there are only 2 clients) are on the same level, around 10% rate.

The best campaign is the latest, it attracted the biggest amount of clients from every country.

The worst campaign was the second one. The acceptance rate is very low for every country including Spain. Also there were no clients from USA who accepted 2nd campaign offer.

# Dashboards

**All dashboards provide ability to segment clients by income, country, age, marital status, education.**

### Which marketing campaign is most successful?
There is no additional information about campaigns, what were the purposes, but taking in mind that acceptance rate was provided, we’ll make analysis based on this metric. 

[Tableau Dashboard](https://public.tableau.com/profile/denis.ahinski#!/vizhome/CampaignAnalysis_16180730148870/Dashboard1)

**The most successful campaign was the latest. Also it should be taken in mind that the 4h campaign attracted clients with the highest income**

### What does the average customer look like for this company?
**Average client:**

45 age with graduation, 52000 income, married with 1 child from Spain.
Made about 5 purchases and bought 43 products. 

[Tableau Dashboard](https://public.tableau.com/profile/denis.ahinski#!/vizhome/Book2_16180795494820/Dashboard1)

### Which products are performing best?
There is no information about prices, so we can operate only with amounts of products. From this point of view the best selling products is wine. Next best products are gold and meat.

[Tableau Dashboard](https://public.tableau.com/profile/denis.ahinski#!/vizhome/BestProducts_16180909493580/Dashboard1)

**The best perfoming product is wine. However for clients with low income meat and gold are the best.**

### Which channels are underperforming?

[Tableau Dashboard](https://public.tableau.com/profile/denis.ahinski#!/vizhome/BestChannels/Dashboard1)

**Deals (discounts) and catalog channels are the worst. At the same discounts are very among people with low income. The best channels are store and web. Stores are more popular among people 35+, but at lower age channels perform equally.**

# Recommendations
* #### Analyze campaigns insights. Especially this questions:
  * Why 5th campaign was so succesful, what differs this campaign from others? 
  * Why 2nd campaign was bad?
  * Why 2nd campaign was much worse with clients from Spain compare to other campaigns?

* #### Last campaigns showed positive correlation with income level and negative corr with number of children. So we should try to conduct campaign for people with low income and children. Also we know that people with lower income and more children usually make more discount deals

* #### Conduct more campaigns popularizing products with less sells.

* #### Advertise campaigns with different approaches for stores/websites. Also age and other client characteristics should be considered.
