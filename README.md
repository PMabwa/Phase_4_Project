# Phase_4_Project
![image](https://github.com/user-attachments/assets/74a57338-0a78-4c82-a892-d91bcefec033)
# **Business Understanding**
#### This project seeks to accurately gauge customer sentiment towards our brand based on their Twitter interactions. Additionally, stakeholders may use this to inform customer engagement strategies and improve product or service offerings.
## **Summary of the Project**

#### The project begins by exploring the sentiment dataset sourced from CrowdFlower via data.world (https://data.world/crowdflower/brands-and-product-emotions). The dataset undergoes an EDA process that involves handling null values through a for loop that is able to extract items to replace the null values in it. With a clean dataset, it is easier to determine that Ipad is the most mentioned product, neutral sentiments are more than both positve and negative ones and that the ipad device is rated highest in the sentiment distribution among products.

#### In order to undertake the modeling process, the tweet_text column referenced as tweets, undergoes a preprocessing phase (tokenization, vectorization & lemmantization) that distills the irrelevant articles that wouldn't be easily translated by the machine learning model. This also helps in identifying the most frequent phrases & words observed among the tweets. In this case, Apple Store is the most mentioned text across the texts with a frequency of 520. 

#### The Modelling Phase consists of a binary & multiclassifier comparison across diverse models. They include; Logistic Regression, XGBOOST, Support Vector and Random Forest Classifier. The results of the model perfomances demonstrate that these models perform best under binary (Accuracy Score ranging from 84-89%) than in multiclass classifier 67, even with best parameters applied. 

#### The recommendation for enhanced classification comprises of; 
#### 1) using aspect-based sentiment analysis to provide context.
#### 2) sample data from high impact users including relevant   influencers & tech communities 
#### 3) Enhance sentiment models to interpret more nuanced emotions beyond the regular (positive, negative & neutral)

### **Data Understanding**

#### This dataset is a list of sampled tweets about Apple and Google products with 9093 entries, within it there are three columns;

   #### 1) tweet_text - contains sampled tweets about the products.

   #### 2) emotion_in_tweet_is_directed_at - which product the tweet is about.
   
   #### 3) is_there_an_emotion_directed_at_a_brand_or_product - which sentiment the tweet is about. 

# **Import the necessary libraries**

#### These may be needed including Pandas, numpy, matplotlib and nltk.
# **Exploratory Data Analysis**

#### Explore the contents of the dataset to better understand it. Determining missing values, renaming columns, handling duplicate columns,and evaluate the disribution of products.

![image](https://github.com/user-attachments/assets/64c9b07a-d97a-403e-a4d9-8b29cdfe9745)

![image](https://github.com/user-attachments/assets/fc26b740-c404-44b8-b23a-496f3d0ce795)

#### The Pie Chart above displays that the percentage of neural sentiments is higher (60.3%), followed by positive (33.3%) then negative at (6.4%). With such a collection, there is likelihood of a class imbalance challenge when analyzing the sentiments. With the bar chart showcasing the top ten products with ipad getting the most mentions of about 2300.
![image](https://github.com/user-attachments/assets/8c4e38a8-4bd4-4ee6-9a97-83a46f3b7c54)

 #### The plot above demonstrates that the distribution of neutral sentiments across the product is high. This may be as a result of a class imbalance, whereby the number of neutral sentiments are more than those of either positive or negative. According to the plot, the ipad product has the highest positive sentiment of 900 whilst the highest negative sentiments are observed to affect the iphone product.  

 # **Modeling**

#### In this section, expose the cleaned and preprocessed dataset to diverse models for sentiment analysis. Evaluate how accurate the models perform in binary and multiclass. For a baseline model, use logistic regression
### **Conclusion**

#### Based on the EDA above, it is evident that the product with a high frequency of sentiments are from the Apple industry, with the Ipad product demonstrating a more positive reception among customers from the tweets sampled.

#### After testing diverse models for the best possible sentiment analysis, it is evident that in both simple(logistic regression) and Advanced models(XGBOOST, SVM & Random Forest Classifier), binary classification performs best with high accuracy prediction scores of between (84% - 89%) after tuning the models to their best parameters. The multiclass trials exhibit a stagnation of prediction accuracy score of 67%. The *challenge* faced across the models is the class imbalance where neutral sentiments are more than those positive and negative.

### **Recommendation**

#### 1) To get better insights, companies like Google and Apple may focus on high-impact users such as relevant product influencers and tech communities who can provide more valuable insights about their products. The high product engagement usually informs this of these target segments.

#### 2) Seek to interrogate the neutral comments further using aspect-based sentiment analysis to contextualize the comment. This may help identify valuable information/feedback about a product's performance or design.

#### 3) For the sentiment analysis model to perform better, introducing sentiment weighting might aid in distinguishing feedback from high-engagement users to reduce the influence of low-impact neutral responses influencing the overall insights.

#### 4) Lastly, Enhancing the sentiment classification models from the conventional(positive, negative and neutral) responses, where it can be able to interpret more nuanced emotions within the text.  


