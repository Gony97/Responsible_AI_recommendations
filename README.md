# Final Project in Responsible AI, Law, Ethics & Society: 

## Feedback Loop and Amplification in Recommendation Systems 

### Project concept:

Recommendation system governs big part of our digital and content consumptions in: social media, streaming services and Ecommerce. What are the long-term consequences of relying on the recommendation of a system over and over again, and at the same time, this system is being shaped by the users’ actions?

Given that recommendation systems in the industry aim to optimize and increase time spent on a given platform, many (in effect) will lead to recommendation systems that produce "echo chambers" and "filtered content" feeds that tailor to the user's specific preferences and point of views.  “Echo chambers”, built on algorithmic recommendation systems fine tuned to the users preferences, limit the content and the diversification of the information flow to which the user is exposed to, known as a “filter bubble”. While this may not be strictly inappropriate or problematic in some cases, in other contexts, such as news consumption, which highly contributes to shaping the users political standing and identity, this could lead to the propagation of harmful material that may elicit detrimental interactions and exposure to otherwise irrelevant material.


### Data Source:
The news article recommendation system would require two datasets: All the News and Articles Sharing and Reading from CI&T DeskDrop, which includes many news articles and their properties, and user's impression logs. 

https://www.kaggle.com/datasets/gspmoreira/articles-sharing-reading-from-cit-deskdrop

https://www.kaggle.com/datasets/snapcrack/all-the-news

https://www.kaggle.com/code/eunicemok/recommendation-engine-that-combats-polarization


### Methods:
Training Models to classify the political lean of news articles (left-wing/central/right-wing) by using "All The News" dataset and classifying each article's political view based on the publisher. The data given to the model is a vectorization of the article contants using TfidfVectorizer and using Passive Aggressive Classifier to classify the data. 

Using the trained model we can classify the political views of the articles in "Articles Sharing and Reading from CI&T DeskDrop" dataset and examine users interaction with news articles (view, like, comment, share) and the political views of these articles.

### Finding:
The majority of users tend to engage primarily with news articles that align with their particular viewpoint, while a significant number of users avoid interacting all together with articles that present different perspectives.

![graph1](https://github.com/Gony97/Responsible_AI_recommendations/assets/82442657/e0161325-dc08-46ed-96df-9d7f51347ac4)

In the heatmap above we can see that most users have a political view in which most of the news articles they interact with are from that point of view. It is incoraging to see that we do have users that have around equal amount of articles from different views, but we can see see echo chambers forming, wtih users who only interact with one type of political view.

![graph2](https://github.com/Gony97/Responsible_AI_recommendations/assets/82442657/a0456f84-b4c5-481a-9841-acf3dd383c03)

In this heatmap we examine users who liked articles, and compare the general political lean in their total articles compared to the political lean of the articles they liked. We can see, especially at the users who interact mostly with articles of the same political view, that they “like” more articles of the same political view that does they interact with.

![graph3](https://github.com/Gony97/Responsible_AI_recommendations/assets/82442657/08850c51-52c4-481c-82e4-c43ac279e105)

This behavior is even cleared when viewing the users who comment on articles.
