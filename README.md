## Mid_term_Project
### Introduction
Flight delay has become a very important subject for air transportation all over the world because of the associated financial loses that the aviation industry is continuously going through.

According to data from the Bureau of Transportation Statistics (BTS) of the United Stated, over 20% of US flights were delayed during 2018, which resulted in a severe economic impact equivalent to circa 41 billion US$.

The reasons for these delays vary a lot going from air congestion to weather conditions, mechanical problems, difficulties while boarding passengers, and simply the airlines inability to handle the demand given its capacity.

In this project I will look at different ML algorithms including MLP Neural Networks to try to predict if a flight will be delayed or not before it is even announced on the departure boards. 
### Objective
The objective of this project is very clear as described in the introduction: "Design a Model that predicts flight delays of first week of january,2020".

### Data Preprocessing/Cleaning
Other features were engineered mainly to perform the EDA. Among those, some of the most relevant were:

- Calculating the total number of flights and total numbers of delayed flights (from departure and arrivals separately) by airline
- Calculating percentages of delayed departures and arrivals by airlines and by cities
- Extracting the top destinations with average delays and arrivals
- Calculating best weekday to travel in terms of delays (departures and arrivals)
- Impact of late departure on arrival time (with difference between both) etc.

### EDA
On the EDA notebook, the few questions were addressesd, we tried to solve those questions and got the better understanding why the flights are getting delayed.

### Modelling
Now that the data has been cleaned and gone through a thorough EDA process done in two stages, its time to start with the modeling.
I am not sure which Machine Learning algorithm will be the best for this.

### Summary & Recommendations

- From the EDA done it seems as DA (Delta Airlines) and Alaska Airlines are two of the most reliable airlines in terms of arrivals on time, and in the case of DA, they are top 5 in number of flights per year, average delay (with the lowest), and number of destinations within the US. However it is important to remember that these conclusions are based on 2018-2019 year data analysis and this could well be a good year for those airlines and bad for others for any particular reason.

- It is quite hard to create a ML model for flight delay prediction before you even know that the flight is delayed on the departure board.Maybe an even more thorough feature analysis could rise these metrics to close to 90%, so it might be worth investing the time to do so.

- There are a series of variables (features) that were not included on this project due to a shortage of time and I believe after my research that they are key to predicting a flight delay accurately. Some of these are the weather, mechanical issues, and security issues. Then inside some of these there are sub-categories that also play a key role such as humidity, wind, precipitation, etc, and should be accounted for. All of this data is available but needs to be scraped from different websites and it will require quite a lot more work to add it to the existing dataset, but will certainly translate into more realistic and therefore more accurate predictions.
