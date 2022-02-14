## Mid_term_Project
### Introduction
Flight delay has become a very important subject for air transportation all over the world because of the associated financial loses that the aviation industry is continuously going through.

According to data from the Bureau of Transportation Statistics (BTS) of the United Stated, over 20% of US flights were delayed during 2018, which resulted in a severe economic impact equivalent to circa 41 billion US$.

The reasons for these delays vary a lot going from air congestion to weather conditions, mechanical problems, difficulties while boarding passengers, and simply the airlines inability to handle the demand given its capacity.

In this project I will look at different ML algorithms including MLP Neural Networks to try to predict if a flight will be delayed or not before it is even announced on the departure boards. 
### Objective
The objective of this project is very clear as described in the introduction: "Design a Model that predicts flight delays of first week of january,2020".

### Data Preprocessing/Cleaning
The imbalanced data means that I will need to weight these two classes while training my models.

Other features were engineered mainly to perform the EDA. Among those, some of the most relevant were:

- Calculating the total number of flights and total numbers of delayed flights (from departure and arrivals separately) by airline
- Extracting the "weekday" from the date using the "datetime" function from Pandas. Using the same function, the "month" and "day of the month" were also extracted
- Calculating percentages of delayed departures and arrivals by airlines and by cities
- Extracting the top destinations with average delays and arrivals
- Calculating best weekday to travel in terms of delays (departures and arrivals)
- Impact of late departure on arrival time (with difference between both)
