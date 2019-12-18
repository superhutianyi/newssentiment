# News Sentiment on Stock Market Prediction
Created and completed by Tianyi Hu

This is about news sentiment on stock market prediction.

### Research Question: 
How effective is the prediction of stock price fluctuations using textual worldwide news articles?

### **Main Data** : 
`DJIA_price.csv`includes daily stock prices from 2000 to 2016 of Dow Jones Industry Average (DJIA) obtained from Yahoo! Finance API. In this dataset, it consists of the Open, High, Low, Close, Adj Close values and trading volume in each day.

| Column             | Varible Explain                                              |
| ------------------ | ------------------------------------------------------------ |
| `Date`             | specific calendar day                                        | 
| `Open`             | open price of each date                                      |
| `High`             | highest price in one day                                     |
| `Low`              | lowest price in one day                                      |
| `Close`            | closing price of each date                                   |
| `Adj Close`        | adjusted closing price of each date                          |
| `Volume`           | total transaction amount                                     |

`News_Data.csv`includes historical worldwide news headlines written in English from 2000 to 2016 were obtained from Reddit World News Channel. Reddit is a social network platform, and its subreddit ‘worldnews’ includes published news of the whole world. Due to the large volume of the datasets, only the top 25 headlines are considered for a single date.

| Column             | Varible Explain                                              |
| ------------------ | ------------------------------------------------------------ |
| `Date`             | specific calendar day                                        | 
| `Top 1`            | 1st popular news headlines                                   |
| `Top 2`            | 2nd popular news headlines                                   |
| `...`              | ...                                                          |
| `Top 25`           | 25th popular news headlines                                  |

### Methodology:
(1) Sentiment Analysis: Text Preprocessing
-Convert into a lower case;
-Drop the noisy words;
-Remove numbers, white spaces, tabs, punctuation characters, stop words etc.; 
-Tokenize the text document into words
-Stemming or lemmatization process. 

(2)Sentiment Analysis: Polarity Detection Algorithm
VADER/LM dictionary

(3)TF-IDF Analysis
Using TF-IDF analysis allows us to figure out which word is characteristic for one text document within a collection of documents.

(4)Stock Prediction using Machine Learning Models
Naive Bayes/ Random Forest/ SVM

### Results:
![image](https://github.com/superhutianyi/newssentiment/raw/master/Figure/WordCloud.png)

To have a general idea of the headlines we collected, we used word clouds and word counts to construct the frequency analysis, where the size of a word is determined by how many times it appears in the headlines. 

![image](https://github.com/superhutianyi/newssentiment/raw/master/Figure/Comparison.png)

We could see from the above figure that the accuracy of prediction in 90%/10% train test split shows the best accuracy among those three split methods. The color change of black and white shows most difference. The difference between three machine learning models in 90%/10% split is not significant for us to see from the picture. 

### Limitation:
High fluctuations in prices

Limitation in time series algorithms

Limitation in stock selection

