# Data Science Portfolio

## Portfolio projects

## Portfolio 1
In this portfolio, Cycling and weather data were analysed. 

1. I combined 2 datasets "Cheetah" and "Strava" and removed rides with no measured power
2. Plot some required key variables: time, distance, average speed, average power, TSS to see their distributions:
   * Moving time is bimodally distributed
   * Distance is right-skewed
   * Average Speed seems to be normally distributed
   * Average Power is normally distributed
   * TSS is right-skewed, it also has some outliers
3. In this requirement, I tested the correlation of every required variable and explored some relationships: 
   * Distance and moving time
   * Distance and elevation gain
   * Distance and Training Stress Score (TSS)
   * TSS and moving time
   * moving time and Elavation gain
   * Average Speed and Average heart rate
   * Average Speed and power
   * Elevation Gain and TSS
   * Normalised power (NP) and Power
   * NP and Average Speed
   * Average Heart rate and Power   
All of them are positive linear associations due to their high possitive correlation (from 0.67 to 0.94)
4. I explored the differences among the three categories: Race, Workout and Ride
   * Using scatter plots with different colours for each category, I explored that Ride has the highest number of rides and a wide range in moving time and distance, comparing to other 2 categories. While Ride can go up to more than 200 in time and 100 in distance, Race and Workout have significantly much less moving time and shorter distance. 
   * Using box plots to visualise moving time, I explored that Ride has the most rides, biggest range and highest median moving time; while Race has the less rides, smallest range and lowest median moving time, followed by Workout with a mild difference. Only Race has some outliers, which are pretty far from the box.   
5. In this requirement, I explored relationship between rides and weather by combining the rides dataset with weather dataset in 2018 and 2019. There was no observed relationship between distance and temperature, and between average speed and temperature.
  
Challenge: 
   * By summarizing the likes of each catergory, I found that Ride is the most popular due to its highest number of likes
   * I tested correlation between Kudos and other key variables. Distance, moving time and TSS are 3 variables that have moderately positive correlation with Kudos. That means it can be understood that the more distance, time and TSS are, the more likes we seem to get. 
   
   
## Portfolio 2

In this Portfolio, I was asked to reproduce some work on predicting the energy usage of a house based on Internet of Things (IoT) measurements of temperature and humidity and weather observations. 

**Linear Model**
After droping some unnecessary variable and converse all into numerial values, I fit training and test data into a Linear Regression model. Root mean square error (RMSE) is 93.21 and R2 is 0.16. The result showed very high RMSE and low R2, which means this model is not very good for the dataset. 

**Linegraphs(Time-series plots)**

   * The first line graph shows energy consumption of Appliances from January to May 2016. In the beginning of February and April, there were days that energy was not used much, while at the middle of January, appliances were used up to more than 1000Wh.
   * The second graph looked closer at the first week of January. It can be seen that there were days that electricity was consumed up to 800 Wh and up.

**Distribution of Appliances (Histagram and boxplot)**
   
   * The common amount of electricity vary from around 5 to 200Wh, with the most common one is 50-60Wh
   
**Pairplots**
   * The graph shows relationship between the energy consumption of appliances with: lights, T1, RH1, T2, RH2, T3, RH3. It can be seen that there is a positive correlation between the energy consumption of appliances and lights (0.2).
   * Besides, there is a significant positive correlation between T1 and T2 (0.84), T1 and T3 (0.89), RH1 and RH2 (0.8), RH1 and RH3 (0.84)

**Heatmap**
   * An hourly heat map was created for four consecutive weeks of data to identify any time trends.
   * Energy starts to be used at around 6am. The energy consumption decreases from around 9pm. There is no clear pattern in terms of day of the week.
 
**RFECV**
   * 35 predictors (inclusing Visibility) were used to select the best features. Comparing to the original paper, the order of best feature was different and RMSE of my work is around 7 higher. While lights', 'T1', 'RH_1', 'T2', 'RH_2' is my top 5 best feature, the paper' top 5 is NSM, light, Press, RH5 and T3.
   
## Portfolio 3
The required goal of this portfolio is to build predictive models for the genre of a book into one of the five target genres based on a summary. The five genres are: "Children's literature", 'Science Fiction', 'Novel', 'Fantasy', 'Mystery'. Since the value are all text, I performed feature extraction to produce feature vectors for the predictive models. I fit 2 predictive models and this is their accuracy score:
   * Logistic Regression: 0.66
   * Random Forest Classifier: 0.63
   * Multinomial Naive Bayes: 0.43
**Conclusion**: It can be seen that Logistic Regression model is the most suitable model to predict book genre in this case.
