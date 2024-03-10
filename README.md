# ATP-Analysis-Project

In this project, we are interested in learning some factors for winning a ATP (Grand Slam Level) game, such as players’ ages, seed, height, handedness (right-handed or left-handed), etc. In particular, we are going to look into the players’ age factor. Some potential questions we would like to study are: “At what age is a tennis player at his peak/prime?”, “What is the average prime time for a tennis player?”, “Any correlations between players’ age and win rate?”. We gathered our dataset which contains details (49 columns) about all ATP matches played  (188,161 observations) since 1968, from Kaggle.com (https://www.kaggle.com/datasets/sijovm/atpdata ). 
 
In the data cleaning process, because match statistics are not available until 1991 and we are interested in only Grand Slam level matches, we decided to filter out matches that are not “G” level and pre-2000.
 
In our preliminary analysis, we first used the “describe” command to learn basic information of the dataset, such as mean, max, min, count. By capturing columns that we are interested in, we learned a few interesting information: ATP Grand Slam are averaging 26.5 years old with height around 186 centimeters and winner usually have a higher ranking/seed. However, we do not observe any significant age difference between winners and losers.
  
In order to obtain a better understanding of the relationship between age and winning, we chose concatenate the winner and loser data into a new dataframe. In this new dataframe, we included “Age” and dummy variable “win_or_lose” to indicate winner and loser. This allowed us to perform a simple linear regression and correlation matrix. 
From our result, we learned that the two variables have low correlation coefficient and our simple linear regression model is not accurate due to the low R-square value and high p-value of the independent variable (meaning it is not statistically significant).

 
	Next step, we categorized our data into 8 different groups and tried to compare win rate between groups. In the table and plot shown below, we can observe that the win rate of age group “under 18” (30.7%) and “22-26” (51.3%) are the lowest and highest respectively. Secondly, the overall win rate from 18 to 38 is relatively stable, stayed around 50% and start dropping after 38 years old.
	In conclusion, we could not conclude that players’ age is statistically significant of winning a match in Grand Slam level. Furthermore, we observed that professional tennis players do not have a particular “prime period”. Instead, they have a relatively long and stable career with a steady win rate overall.
