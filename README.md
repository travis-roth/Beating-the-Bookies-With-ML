# Beating-the-Bookies-With-ML
DEVELOPING A MODEL TO PREDICT WINNERS AND PROFIT ON FOOTBALL BETTING USING THE AMERICAN ODDS METHOD
Travis Roth, Iman Janoo, Drew Blik, Evelyn Ochoa

## Executive Summary

The sports betting industry is a rapidly growing and evolving sector with significant global growth, driven by factors such as increased accessibility through online platforms, the legalization of sports betting in various jurisdictions, and the rising popularity of sports. In 2022, the worldwide sports betting market reached USD 83.65 billion and is projected to grow at a compound annual growth rate (CAGR) of 10.3% from 2023 to 2030. One great business avenue in this sector is the technological innovations supporting sports betting. The industry has seen technological advancements, integrating data analytics, artificial intelligence, and machine learning to provide more accurate odds, better user experiences, and enhanced customer engagement.
	
Considering the potential business opportunities related to data analytics, we chose to explore how we can give football betters an edge in sports betting. Using three main datasets representing game scores, team information, and stadium information, we attempted to develop a model to predict who will win each game based on normal scoring and spread-adjusted scoring with an American odds method. Our ultimate goal was to see whether our model could improve the accuracy, yearly profit, and cumulative profit compared to the baseline, both with or without the spread-adjusted scoring. Our datasets offer a wealth of opportunities for in-depth data analysis, especially in the context of sports analytics and strategy. Hence, our goal is to determine whether a model can be built with existing data to accurately predict the winners of every game during an NFL season. 
	
The response variable is home_win, referring to whether the home team wins or loses the respective game. This is a binary variable, in which 1 represents a win, and 0 represents a loss. Within our code, we utilized random forests and logistic regression to make these predictions. Ultimately, our results revealed that using spread-adjusted scoring did not help our case or improve our model. However, the CART model without spread-adjusted scoring did yield slightly improved results in comparison to the baseline. 
	
Finally, to calculate profitability, we used the American odds neutral, which is -110,110 odds. American odds show how much a better must bet to make winnings of $100. In our case, to receive winnings of $100, a better must bet $110.


## Business Goal
Our goal is to help football betters get a better profit on their bet, based on the features in this dataset related to stadium, scoring, and weather-related information. We modeled our strategy using the American odds method, described in our executive summary.

## Data Mining Goal 
Response Variable: home_win 
Home_win refers to a binary outcome where 1 indicates the home team won, and 0 indicates the home team lost or tied. Ties are extremely rare in the NFL, there have been only 6 games tied since a rule change in 2017.

## Predictors and Goal: 
The features we use for predicting the home_win are extracted from our nfl_team, stadiums and spreadspokescores datasets which were merged together. The predictors included in our model are stored in the include_columns variable. Simply put, our data mining goal is to predict whether the home team will win. Notably, the baseline model predicts the home team will win in every game. Therefore, we assess whether our model improves the betting strategy from the baseline model based on accuracy, yearly profitability, and cumulative profitability to compare the model performance both with and without spread scores. 

## Key Findings: 
Stadium Variability: The analysis revealed a diverse range of stadium types with varying elevations including outdoor, indoor, and retractable venues. This highlights potential areas where altitude differences may impact game performance and outcomes. 
Weather Factors Impact: Certain weather conditions, such as extreme temperatures or precipitation, showcased correlations between fluctuations in home team performances, indicating potential predictive value. When analyzing weather data, we found that 1085 games were played in temperatures greater than or equal to 75 degrees with the highest temperature reaching 97 degrees. 
Geographical Influence: Stadium locations and their respective climatic conditions displayed regional variations which might influence team strategies and performance. 
Home Team Performance: The Pittsburgh Steelers demonstrated the highest number of wins, significantly outperforming other teams. In contrast, the Washington Football Team exhibited the lowest number of home wins among the analyzed teams. 

Understanding stadium types, elevation effects, and weather conditions provided valuable insights into the diverse factors influencing game outcomes. Incorporating these variables into predictive models holds promise in refining betting strategies and enhancing predictive accuracy.
Data Preparation 
Our data preparation can be explained in two parts. The first part will briefly cover how we constructed our training and testing set step by step. The second part will explain feature engineering techniques conducted by elaborating the features we used for prediction. 

## Next Steps
We believe our model could be improved in a few ways. Firstly, we could add more data about the team’s composition. For example, we could use the previous year’s data about individual players' performance to calculate a player rating, and then combine these ratings into a team rating. This could give the model a more accurate understanding of the team it is predicting other than its rolling win count. Another way to improve the model is to use real betting odds instead of the default -110. Given access to this data, we could use the historical odds to evaluate the profitability of bets versus the certainty of the outcome, choosing only the most certain bets to bet on. The NFL is extremely popular, and data collection is improving in accuracy and scope. In the future, machine learning will have an even greater impact in areas like sports betting. Although this project is a good first step at the problem, it is only that: the first step.

