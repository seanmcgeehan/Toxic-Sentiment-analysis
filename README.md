# Sentiment Analysis
### 
##  



**Team Members**  
Name | Year
------------ | -------------
Sean McGeehan | 2022
Lucy Hu | 2023
James Baker| 2022

For this project we focused on classifying toxicity using syntax and semantic features. We trained several machine learning models ranging from simple Bag of Words models using tf-idf up to fine tuning a BERT base model.


**Motivation**  -
The introduction of widespread Internet access and the age of social media has allowed for much more communication, interaction, and information sharing than ever before. Users are able to engage with far-away family, friends, and even strangers from the comfort of their own home. While social media has no doubt brought greater convenience and connection into our lives, its potential negative consequences on mental health, social abilities, and more cannot be ignored. In fact, they are the subject of much concern today, as evidenced by numerous articles and studies published on the subject.

Unfortunately, social media can be abused as a platform for creating and sharing offensive and toxic content like hate speech. As a result, comment moderation has become increasingly important especially considering the far reaching impacts of social media. Studies conducted by the Pew Research Center suggest that at least 72% of the public uses some form of social media and the majority of users access these platforms on a daily basis. Even more distressing, many of the most prolific users are young adults or adolescents. Hate speech and other forms of offensive content can potentially inflict mental and physical harm on users, especially vulnerable groups.

Given the importance of this problem, we decided to explore toxicity classification for our project.


**Data and Definition**
Our dataset originates from the Jigsaw Unintended Bias in Toxicity Classification competition on Kaggle. It consists of 1.8 million comments which were gathered from various Wikipedia Talk pages and labeled by a panel of reviewers. A target toxicity label was generated by aggregating the ratings of all judges, where toxicity was defined by researchers as "anything rude, disrespectful or otherwise likely to make someone leave a discussion."

In order to generate features and discover corelations between common words and toxicity we dove deep into the data to attempt to find lists of words that might be useful for our models. We generated bar plots and word clouds to help visualize what would be useful.


![alt text](https://github.com/seanmcgeehan/Toxic-Sentiment-analysis/blob/main/word%20cloud.png?raw=true)

![alt text](https://github.com/seanmcgeehan/Toxic-Sentiment-analysis/blob/main/download.png?raw=true)








In bulding our classifers, we used five different modeling packages. Our most successful models include logistic regression on tf-idf and our fine-tuned roBERTa and BERT models, which is a bit of surprise considering that the former is a much simpler model. All performed similarly (with an AUC around 0.84 - 0.86), which serves as a lesson to not discount simple models. However, we believe that the BERT has more potential.

In the future, given more GPU resources, we hope to be able to fine-tune BERT with the full dataset. Additional avenues to explore in the future include analysis based on stemming to catch offensive words that share the same root, ensemble models, higher data fidelity, better data labeling, more feature engineering heuristics. Utilizing other pretrained models may also be a fruitful pursuit. The sentence structure such as separating the subject and predicate could provide useful context clues when predicting toxicity. Performing Named Entity Recognition could also add more signal to the model???s weights.


**Stack** -
Python
Pandas
Numpy
Sklearn
Matplotlib
NLTK
Seaborn
Spacy
BERT





