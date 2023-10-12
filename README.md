# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 4: A 'health' classifier for biscuits - The Snack-o-Meter

### Problem Statement

The National Health Population Survey highlighted various actions to improve Singaporean health. The focus of our project will be on eating healthier.

Several measures has been implemented to encourage healthy eating. This includes the Nutri-Grade labeling for beverages, which focuses on sugar and saturated fat, which has shifted consumption and led to reduction in sugar intake. More recently, Singapore has also shared that it is studying possible regulatory measures to reduce sodium content in food dishes. However, the nutritional values in snacks has not been widely discussed and this is the gap we are targeting to cover.

While all snacks should be considered, biscuit is used as the initial proof-of-concept due to its popularity. The objective of the project is to build a user-friendly tool that can inform if a biscuit is healthy or not, helping consumers make healthier choices.

---

### Data Used

[`NTUC Fairprice`](https://www.fairprice.com.sg/category/biscuits): Data is scrapped from NTUC Fairprice website, under category of Biscuits.
<br>Biscuit Subcategory: 
1) Creamed and Filled
2) Crackers
3) Wafers
4) Chocolate Cookies

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|**type**|*string*|Subcategory of Biscuit<br>cookie: chocolate cookie<br>cracker<br>cream: creamed & filled biscuit<br>wafers|
|**product**|*string*|Name of product|
|**per_serving_g**|*int64*|Size of serving per one gram (gram)|
|**total_fat_g_per_gram_of_serving**|*int64*|Total fats per gram of serving (gram)|
|**sugars_g_per_gram_of_serving**|*int64*|Sugars per gram of serving (gram)|
|**sodium_g_per_gram_of_serving**|*int64*|Sodium per gram of serving (gram)|
|**class**|*string*|Healthy<br>Unhealthy|
---

### Notebook description

* [`01_webscrapping`](/code/01_webscrapping.ipynb): Scrapping nutritional value data from NTUC Fairprice website
* [`02_Data cleaning`](/code/02_cleaning.ipynb): Cleaning of data
* [`03_EDA`](/code/03_eda.ipynb): Exploratory data analysis
* [`04_Modelling`](/code/04_modelling.ipynb): Modelling of the data

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
