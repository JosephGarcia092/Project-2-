# Project-2-
# Housing Price Sentiment
___

# Project Goal 
Create an investment tool that will allow the user to predict the trends of real estate by analyzing the increase in housing prices as it relates to the mortgage rates. The tool will analyze historical mortgage rates and look for confluence and divergence between the housing prices and mortgage rates. Using the 30yr and 15yr mortgage rates as an indicator can we predict the future outlook of the housing market. The sentiment will be gauged by using NLP to see if there is a correlation with sentiment on twitter and our predictor. We can use this tool to assess the correlations and judge if it is the right time to look for houses.

## **Our Challenge**
- The Case-Shiller Home Price Index is delivered on a monthly basis. Although our data originates in 1987, 12 data points a year is not a lot. We decided to use both forward fill the monthly data to be “delivered” daily so we have more data points. Also to use the non biased data sets to get the real picture. 
- Using the Non biased data give the Group a more _REAL_ outlook on what is going on in the housing market The Case-Shiller Home Price Index only provided us with about _680 Data Points_. This was considered **low** to us. Using the Foward Fill method to fill in data in bwtween the months we get our **Real** data

# Group Questions
___
1. Is there a correlation with mortgage rates and housing prices?
2. What states index is lower than the US National benchmark?
3. What states index is Higher then the US National benchmark?
4. Do we foresee a slowdown or a correction in the future?
5. What is the overall sentiment of the housing market right now?
___

## Data Cleaning Process 
___
- we gathered data through an API using _Pandas DataReader_ with the data from **FRED** or _Federal Reserve Econommic Data_. This is where we find the *Case-Shiller* monthly index. At this point we decided to use the _ffill()_ method to see if the increse in data points were needed for an outcome. 
- cleaned the Data by the normal process (ie. dropping na, removing null, column manipulation, etc.) then splitting up the data for testing and training.

## Data Analysis
__
- We took the cleaned data and split data to get started for **Natural Language Processing** 
  - NLP we used a few different methods here **WordCloud, Vader Sentiment Intensity Analyzer, PorterStemmer/ Lemmatizer**
- After we took a look at the sentiments on _NLP_ we started our **Machine Learning**
   - **ML** we used Naive Bayes and Logistic Regression 
   - Naive bayes (https://machinelearningmastery.com/naive-bayes-for-machine-learning/) for a better understanding of now _Naive Bayes_ works.
- Another method of **ML** is _Logistic Regression_ (https://www.ibm.com/topics/logistic-regression#:~:text=Logistic%20regression%20estimates%20the%20probability,bounded%20between%200%20and%201.)
