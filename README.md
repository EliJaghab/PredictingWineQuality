# Predicting Wine Quality

This R Notebook explores using machine learning models predict a good quality wine over a bad one.

For this data set, I it is most important to prioritize the precision score because we are considering the quality of wine. For this data, we would be more inclined to exclude data points from the accpetable range and be more selective of the wines picked to be in the "Good" range. Precision factors false positives, so in this case, having a high precision accounts for having a minimal amount of wines thought to be good, but actually are not. 

The correlation of the actual data and the prediction that I came up with is 62.9%

My best model is the first random forest model that I ran where I specify the positive class as 0. This model scores 89% in precision which means that there was a low number of wines ranked as good, but were actually not good (small amount of false positives). This model does well because there is more data about the wines that are bad.

First I read in the data, and used a threshold of 6 and above to determine if a wine is good or not. I then converted the quality of Wine column to 1s and 0s. I looked at the distribution of the data and saw that 78% of the wines were labeled as bad. 

I used random forest and decision tree modeling to determine the best model to fit this data set. After examining the scores from each of the models, I came to the conclusion that the random forest model is best fit for the model as it as a high precision score (89%). The factors that are most important in this model are alcohol, density, chlorides, volatile_acidity, and total_sulfur_dioxide (in descending order).

