# The public attitude towards ChatGPT on Reddit
Our code consists of 3 parts:
1. Data Preprocessing & Wordcloud and Word frequency Display
2. Topic Modeling
3. Sentiment Analysis

# Data Collection
Apify (https://apify.com) is a platform for data collection for web scraping, data extraction, and automation. It offers tools and services that assist developers in extracting data from web pages, executing automated tasks, and building web crawlers. This study used Apify to collect data from Reddit (https://Reddit.com) by setting GPT3, GPT3.5, and GPT4 as keywords. These keywords aim to examine whether people's perceptions of ChatGPT have evolved over time, particularly since the ChatGPT update. Apify collected 11,730, 10,109, and 12,046 relevant entries for the respective keywords. This study performed random sampling to ensure sample uniformity, resulting in 10,000 entries preserved for each GPT version. The dataset consisted of 30,000 samples from June 2020 to August 15, 2023.

# Data Cleaning
In terms of data cleaning, for the textual data in the database, special characters, punctuation, links, and unnecessary words were removed from the comment texts. This study applied lowercase conversion (removing uppercase letters) and removed stopwords. The NLTK library provides the English stopword list. It consists of common English words with no semantic or informational value and is typically filtered out in natural language processing to enhance the efficiency and accuracy of text analysis. Stopwords play a crucial role in enhancing text feature quality and reducing the significance of text features. Considering a slight overlap in the data sources, this study also conducted duplicate text filtering. In the end, 23,773 entries were retained, forming the database Processed_GPT_total.json.

# Topic modeling
The topic modeling addresses the research question: What are the emerging topics related to ChatGPT? The LDA model could help determine the most suitable number of topics for classification. The topic modeling is performed with LDA, and the perplexity-topic number curve is plotted. Subsequently, the results for each number of topics are analyzed to identify the optimal number of topics based on the highest topic coherence

# Sentiment Analysis
The analyzed entries exceeded a total count of 23,773 entries. The two sentiment analysis models, Vader and Textblob, are assigned weights of 0.6 and 0.4 for sentiment classification. The sentiment analysis categorizes the emotional tone of the entries into three distinct parameters: positive, negative, and neutral. This study did histograms and emoji wordclouds of different emotions for analysis.

Based on the GPT-3.5 model, ChatGPT was launched by Open AI on November 30, 2022, gaining a growing user base. On March 15, 2023, OpenAI unveiled the new large-scale multimodal model, GPT-4, available for purchase. This study examines daily sentiment trends by comparing the quantity of positive and negative sentiment posts from January to August 2023 (N=23,773). It aims to ascertain whether version updates and evolution have influenced sentiment towards ChatGPT. 
