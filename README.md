# Sentiment-Analysis-of-COVID-19-Tweets
A twitter sentiment analysis model to understand the people’s sentiment towards the epidemic and on the government decision to extend the lockdown.


## Files And Directories

```Project_Reddit_Flair.ipynb``` contains the notebook to view the analysis of  COVID19 tweets.

```requirements.txt``` lists all the dependencies required to run the project.

A **video demonstration** has also been done [here](https://drive.google.com/file/d/1iXuqDvdG2XCg2vRr2ujyEzlhgUbf07d-/view) to explain our proposed solution. 


## Working
The given kaggle notebook shows that we just need to add the dataset file from [this](https://www.kaggle.com/smid80/coronavirus-covid19-tweets-late-april/activity), run the notebook and then visualize the sentiments of the people in this epidemic.


## Dependencies

```requirements.txt``` contains the list of all the dependencies.


## Approach

This project would primarily explore a twitter sentiment analysis model to understand the people’s sentiment towards the epidemic and on the government decision to extend the lockdown. It uses the coronavirus related Tweets dataset dataset “Coronavirus (covid19) Tweets - late April” which contains the Tweets of users who have applied the following hashtags:#coronavirus, #coronavirusoutbreak, #coronavirusPandemic, #covid19, #covid_19, #epitwitter, #ihavecorona, #StayHomeStaySafe, #TestTraceIsolate. This dataset contains 20 files crawled from the Internet. 

The main idea of this project is to find out the general trendings of the coronavirus related Tweets and classify the Tweets based on the text. The contents have been listed below:
1. Data cleaning, data imputation, 
2. Data visualization using barplots, box plots, pieplots, correlation heatmap, 
3. Information extraction (tf-idf method), and
4. Mini Batch K-means Algorithm.

First of all, we import all the required modules and libraries, and then extract all the useful information leaving behind some files like “Countries” which just are just vain. Then we cleaned and pre-processed the datasets using Pandas dataframe. Here we dropped the columns that have too many missing values and useless columns, concatenated all the information to one dataframe, dropped duplicate columns, and filled the missing values with its mode value.

After cleaning the data, we did EDA, like calculating number of tweets on each day, plotting the barplot, boxplot, and Correlation Heatmap. We also created Wordcloud Visuals to get the insight of the most precious terms in the dataset, which undoubtedly showed “COVID19”, “coronavirus”, “pandemic” were the most frequent words. We had just shown the pie plots for reference to get the distribution analysis of two boolean features. We counted the top 10 sources and top 10 languages where we saw that English is dominating one, so we only used english text for the analyzing purposes. 

Subsequently, for the purpose of Text analysis, we used text features from the tweets of the people and then did clustering for the sake to understand their sentiment towards the epidemic and on the government decision to extend the lockdown. First and foremost, we extracted the tweets we want to use, and then considering the stopwords of the english language, we first transformed our given text data to numeric arrays using tf-idf technique to further retrieve the beneficial information. After this, we used the Mini-Batch K-means algorithm to form several clusters of the data to use it further for visualization purposes using PCA and t-SNE. 


## Conclusion

We observed the extracted key words from the clusters composed and concluded that in fact, this epidemic has badly affected the people, including the government's idea to extend the lockdown. Hence, this project concludes that while the majority of the people throughout the world are taking a positive and hopeful approach, there are instances of fear, sadness and disgust that exhibit still in the world.


## Future Work

Further we are hoping to extract the hashtags from people’s tweets and then design a model using some ML algorithms, like Naive-Bayes, Linear Support Vector Machine, Logistic Regression, Random Forest, and Multi-Layer Perceptron Classifier, where we would be able to detect and classify the tweet as what the overall the message is, that it wants to convey. We would also like to analyze Tweets in other languages as well considering what country that tweet belongs to. Last but not the least, we could also use the web frameworks to analyze how clusters of tweets, that have particular traits, would affect the society. 

