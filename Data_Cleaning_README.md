# Mid_term_Project
## Introduction

Before I start doing this notebook I will define what a delayed flight will be as this will be the principle used to drop or not some of the columns/features that come with this dataset, or to engineer others.

- First of all, a delay flight will be a flight that arrives late at its destination
- If the flight has any delays from its departure, but still arrives to its destination on time, it will not be considered a delayed flight

Furthermore, I will also handle this as a binary classification problem, with a 0 for a arrival on time, and a 1 for delayed arrival.

This is certainly a rather large datasets, so I will look into detail on each feature, missing values, and anything that won't be of use for the project and that can be dropped.
rom the previous quick familiarization, I have the following information which will bee a guide to start woth the EDA

## Priorities:

- Define what I will consider a delayed flight.

- Drop any irrelevant column.

# Things to look at:

Parts of the US with the most delayed flights
Is the data properly balanced? most probably it won't be, so I will need to address that
will this be a binary classification or multiple classification problem?

## DELAY REASONS
On this section I will deal with 5 columns at the same time that are related:

- CARRIER_DELAY
- WEATHER_DELAY
- NAS_DELAY
- SECURITY_DELAY
- LATE_AIRCRAFT_DELAY

It seems as there are a lot of values missing and for some reason the number of each is the same. I'm not sure how trustworthy this is.
Not very promising these number. almost 81% of the data corresponds to missing values.
The decision is to drop these 4 columns except WEATHER_DELAY.

- There are quite some missing values in a few rows
- There are a total of 25,045 rows with missing values.
herefore I will just drop those rows which has missing values and keep on going with my analysis.

## Binary Classsification
As I mentioned at the beginning of this document, this is a binary classification, 
which means that I will run my models with the target being a column that I will engineer called ARR_DELAY. 
In this column there will be only two values (hence the name binary), 
a 0 for flights that arrive either earlier or on time, and a 1 for flights that are delayed.

WE will create a final dataframe for the modeling which will have the top 20 cities only. The reason to do it this way is to get reduced data.

At this point I don't think there is any other pre-processing that I want to do, so I will save this dataframe and start looking at the EDA on a separate notebook. 
However, as I mentioned above, there might be some other feature engineering done for the visualizations that I will do, 
or even some additional column dropping as there are a few that I cannot see affecting the modeling in any way.
create a new one called dfm which stands for "datafame for modeling"

Before this dataframe is saved I need to review the type of each columns and try to minimize the categoricals when possible.
The reason for this is because as we know a categorical variable is a variable whose values take on the value of labels and Machine learning algorithms and deep learning neural networks require that input and output variables are numbers.
This means that categorical data must be encoded to numbers before we can use it to fit and evaluate a model

## Collinearity Check
Now with this reduced and cleaned dataframe it is time to look at how these features correlate to each others,
and then I'll deal with the Categoricals.
The missing features are the categorical ones so I will deal with those directly in the Modeling notebook. Here what I am going to do is reduce the possibility if collinearity.
I set up a threshold at 75% on the correlation matrix and as you can see I got as output points at the following:

- ARR_DELAY with DEP_DELAY
- CRS_ELAPSED_TIME with DISTANCE
- ACTUAL_ELAPSED_TIME with CRS_ELAPSED_TIME
- DISTANCE with ACTUAL_ELAPSED_TIME
And there is a possible multicollinearity with relationship 2, 3, and 4
- Now we have new and reduced datframe with 1351282 rows and 20 columns.
