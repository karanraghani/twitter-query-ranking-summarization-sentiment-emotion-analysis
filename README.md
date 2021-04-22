# Twitter Query Ranking, Summarization, Sentiment and Emotion Analysis

The intent of this project is to create a system that can do an immediate analysis of any topic on Twitter. The analysis includes ranking the top tweets, summarizing them and doing sentiment and emotion analysis of these tweets based on the tweets.
This will help understand the general emotion of the populace. The system will give you the top tweets based on a score assigned to each tweet. These tweets can show the general response of people to a certain situation or topic.
The summarization task involves summarizing the top tweets to create a gist. This is done using a custom mathematical approach developed based on word graphs, bigrams, trigrams, frequency of occurence and tf-idf scores. The summarization is not state-of-the-art but it is a good start in capturing important phrases and making a summary.


### Data
The dataset used is the twitter data. We set up a developer account on Twitter to get access to the search apis. The data that is tweets are retrieved on a query basis. We have used a python library called “tweepy” to query twitter. The twitter search api reference was used to filter and reformulate our queries as per the needs [REF](https://www.earthdatascience.org/courses/use-data-open-source-python/intro-to-apis/twitter-data-in-python/) [REF](https://developer.twitter.com/en/docs/tweets/rules-and-filtering/overview/standard-operators). The user gives a keyword to query. Other parameters configured are date, filters, number of tweets and geocode. The date is hard coded as the current date. The filters are to avoid retrieving tweets which will not be helpful in our summarization and sentiment analysis task. The filters include filtering out retweets, filtering out images and any other type of media and filtering out tweets with urls. The number of tweets is the maximum number of tweets that the user wants to retreive. Geocode is the filter to search for queries near a specific latitude, longitude and in a specific radius. For example, we could set the geocode to the US's centre and set a 1500miles radius to cover all of the US. There is an additional filter of the size of tweets. We take in only those tweets whose actual text is more than 70 characters to get only those tweets that have good content. From the filtered-out tweets, we retrieve the username, location and the actual tweet text.

### System requirements
There are certain system requirements for the implentation to work.
  - python 3.6+
  - pip
  - Jupyter Notebook

### Libraries
Upgrade to the latest version of pip. Use the command given below.
```sh
$ pip install --upgrade pip
```
There are certain libraries required for the implementation.
The libraries required are:
- numpy
- pandas
- tweepy
- nltk
- spacy
- gensim
- matplotlib
- folium
- sklearn
- wordcloud
- textblob
- geopy

There is a requirements.txt file which contains all the necessary libraries mentioned. They can be installed using the below command:
```sh
$ pip install -r requirements.txt
```
The installation part of the project is complete. Yayy !!

### Execution
The project has a Jupyter Notebook (**twitter_project.ipynb**) which is used for the implementation of this project.

The Jupyter notebook has explainations as to what each cell does.
Run each cell and you can observe the output of the commands.
Some commands take longer to execute (they did on our PC atleast), because of the complex calculation and data retrieval being done, so please be patient with it.

### Challenges
One of the biggest challenges faced during implementation of any natural language methods on the tweets are their length. Which increased to 280 characters recently but is still very short to provide better information on how information is structured within the tweet. Other challenges include the use of informal language in tweets, which can be further bifurcated into use of texting abbreviations that can carry a lot of information and use of custom hashtags and emojis. There has been a lot of research work done in the recent past to address these problems on how to relate these short messages to create summaries and do sentiment analysis on.

### Results
The results of our experiments and approach are below:

Ranked tweets:
![Result1](screenshots/Capture3.PNG?raw=true)
Summarization using trigrams:
![Result2](screenshots/Capture6.PNG?raw=true)
Summarization using gensim library:
![Result3](screenshots/Capture7.PNG?raw=true)
Distribution of sentiment in tweets:
![Result4](screenshots/Capture14.PNG?raw=true)
Sentiment Analysis:
![Result5](screenshots/Capture15.PNG?raw=true)

Overall it was a fun project to work on which lead to immense learning!

**Note:** More detailed information/report can be found in the [Project Report.pdf](https://github.com/utsav-195/twitter-query-ranking-summarization-sentiment-and-emotion-analysis/blob/master/Project%20Report.pdf).
