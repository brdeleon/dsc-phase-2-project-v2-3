# King County, WA Property Business Plan

Authors: Brenda De Leon, Kelly Mullaney, Kevin Rivera
<br/>
August 2022
<br/>
![King County, WA](https://kingcounty.gov/~/media/depts/boundary-review-board/images/bellevue-at-night-banner.ashx?la=en)


### Business Problem

Our stakeholders are real estate agents looking to win more business. We propose that by providing home renovation advice, real estate agents are able to differintiate themselves and establish extertise. Additonally, by increasing the sale value of the home, the real estate agent increases their commission. Finally, if your client has a great experience and you maximize the sale value, they are more likely to refer you business. We believe our recommendations will be particularly attractive for the real estate agent's clients who are home owners, home flippers, and for corporate relocation programs that are not interested in a full renovation.

### The Data

To make our recommendations, we used the King County House Sales dataset from Kaggle. The dataset contains King County, WA house sales data from May 2014 to May 2015. King County, WA is in the pacific northwest and is the state of Washington's most populous county according to the 2020 USA Census. The dataset contains categorical and numerical data for 21,597 home sales across 70 zip codes. Our final recommendations were made from the features we analyzed to be the most relevant to solve our stakeholder's business problem. 

### Methodology

To understand the King County House Sales dataset, we began with an exploratory data analysis. We cleaned the data which included dealing with null values, transforming data types, and creating data visualizations. To avoid issues with multicollinearity we explored the correalations amongst the features through heatmaps and statistical measures. We dropped those features that were redundant in order to abide by the assumption of independence in linear regression. Additionally, we dropped those features which we found irrelevant to solving our business problem, such as 'view' and 'waterfront' as we were focused on more practical renovations a real estate agent would be able to pitch to their clients. 
<br/>
We selected 'price' as the target/dependent feature to identify which of the remaining features were creating the most impact on 'price'. To identify which independent features were the most impactful to 'price', we created different linear regression models to get more accurate insights. Linear modeling allowed us to quickly measure how strong the relationship is between the selected independent features and the target feature. Our first model included a few features we had confirmed as impactful through our earlier visualizations. We scaled those features to address the outliers. To refine the model we computed the natural logarithm of our target feature, we then added and kept features we found to be relevant. We based our final recommendations on the highest performing model. 

### Results

Our final model included 'price' as the target variable with 'sqft_living', 'sqft_lot', 'grade', 'condition_code', 'yr_built', and 'bedrooms' as the 6 most impactful features. The final model's R-Squared or coefficient of determination presented that these 6 features explained 62% of the variance in 'price' value. With this information, a real estate agent could provide targetted and effective renovation recommendations that would increase the value of the selling home, and in return will place them ahead of their real estate agent competitors. Specifically our recommendations are: 1. For those clients who are not able to add square footage due to lack of space, we recommend lower scale renovations such as new wood flooring. We identified the highest return of investements renovations to include, projects like painting, insulation, and kitchen/bath improvements. We believe these projects would increase the 'grade' of the house. Our next recommendation: 2. For those clients have the lot space to add square footage, we recommend adding to the home either by extending the home, or more simply by adding a detached addition. A boxabl addition can add almost $100,000 to the value of the home, the home owner could see almost $30,000 back from from this investment. Additionally, we can connect you to services such as financing options to provide further support for those clients who do not have the immediate financial resources to make the recommended renovations.  

### Next Steps

Moving forward, we will perform the same steps but instead, we will to create a new feature: 'price_per_squarefoot'. We will calculate 'price_per_squarefoot' by dividing 'price' by 'sqft_living' for each home. We believe that by targeting 'price_per_squarefoot' instead of 'price' we will be able to provide a more accurate and higher performing model for our stakeholder. We are also interested in exploring the impact of filtering by zip code, and factoring in market conditions, inflation, and degradation of home over time.

