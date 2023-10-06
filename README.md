# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 4: A 'health' classifier for biscuits

### Problem Statement



---

### Data Used

Source: 
* [`NTUC Fairprice`](https://www.fairprice.com.sg/category/biscuits) : Data is scrapped from NTUC Fairprice website, under category of Biscuits.
- Biscuit Subcategory: Creamed and Filled, Crackers, Wafers, and Chocolate Cookies
* [`Anxious Attachment Subreddit`](https://www.reddit.com/r/AnxiousAttachment/): A subreddit for individuals with anxious attachment style to learn more about the style, share experiences and find support.
* [`Avoidant Attachment Subreddit`](https://www.reddit.com/r/AvoidantAttachment/): A subreddit about and for individuals with avoidant atatchment style.

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|**class**|*integer*|Class 0: Avoidant<br>Class 1: Anxious|
|**title**|*string*|Title of the subreddit post|

---

### Notebook description

* [`01_scrapping`](/code/01_scrapping.ipynb): Scrapping data from the respective subreddits using PRAW
* [`02_clean_eda_modelling`](/code/02_clean_eda_modelling.ipynb): Data preprocessing, exploring and visualizing the data and modeling. 

---

### Conclusion

- Our classifier model, Logistic Regression with Count Vectorizer, is able to classify individuals as either anxious or avoidant attachment style with 0.9 accuracy. 
- With this classifier model, we developed an easy-to-use self-help tool (https://attachment-style-classifier.streamlit.app/) to help couples identify their attachment styles. 
- Information and recommendations are provided based on the attachment style for couples to improve on communicating with each other. 

---

### Recommendations

#### Phase 1 - First release of the app on:
- MSF website
- MSF’s Telegram channel (i.e.,MSFCares)
#### Phase 2 - Improve accuracy of classifier model to ≥0.95 through:
- collecting more data from other similar subreddits
- exploring ways to tune the existing classifier model
- exploring the use of other classifier models (e.g., XGBoost) 
#### Phase 3 - Second release of the app with:
- expanded coverage of the other two attachment styles
