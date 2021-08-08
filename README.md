# Amazon Fake Reviews Detection
## Codes and dataset developed for MSING055 final project
We collected multiple layers of Amazon product and review data to identify fake reviews. In this repo you will find two notebooks that contain Python code to do:
1. Cleaning data: the data we get from scraping aren't yet ready to be analyzed, so we did several data cleaning steps
2. Generate new attributes for analysis: two new attributes, sentiment_score and most_rev, were generated to do more in-depth analysis


## Project Summary
The purpose of this project is to identifiy the fake reviews and reviewers by performing a social network analysis in conjunction with anomaly detection with clustering techniques. Developed approach to identify fake reviewers, relative to previously proposed methods has high potential for automation and enables to significantly narrow down the field and dynamically track fake reviewers. 

The sections below will briefly explain the steps and results.

### Data Collection
We scraped data from Amazon's website by adopting snowball method. The process is summarized in the figure below.
![Alt text](https://lh6.googleusercontent.com/s1VfNvgrKoC3DCCqfGruf_5ln49LQBbqKuymrHEd9gc3Z9MoZhtnVX5zHePoAGjsOtOHbneOO3AMbQ=w1440-h731-rw)

Two additional attributes were generated through data aggregation and python module:
- most_rev: highest number of reviews made in a day. This help us to identify if user made a very high number of reviews in the same day. 
- review_sentiment: the sentiment score of the reviews, ranging from -1 (negative) to 1 (positive). This help us identify if the rating is inconsistent with the review sentiment. Textblob module was used to get sentiment score.

#### Overview of final dataset
Total rows: 7652
Columns:
- url: Scraped url
- review_bold: Title of the review
- ratings: star rating given by the review
- verified: 1 = reviewer is a verified buyer, 0 = if not
- date: date review was made
- by: name associated with profile 
- profile_id: ID number of profile 
- most_rev: maximum review made in a day by profile
- by_link: url to profile
- helpful: number of people who tagged review as ‘helpful’
- product: product name
- product_link: url to product page
- review_sentiment: sentiment score of the review







