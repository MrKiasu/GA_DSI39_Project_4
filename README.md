# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 4: The Snack-o-Meter: A tool to inform public on consumption of biscuits​

### Problem Statement

The National Health Population Survey highlighted various actions to improve Singaporean health. The focus of our project will be on eating healthier.

Several measures have been implemented to promote healthy eating. This includes the Nutri-Grade labeling for beverages, which focuses on sugar and saturated fat, and has shifted consumption and led to reduction in sugar intake. More recently, Singapore has also shared that it is studying possible regulatory measures to reduce sodium content in food dishes. However, the nutritional values in snacks has not been widely discussed and this is the gap we are targeting to cover.

While all snacks should be considered, biscuit is used as the initial proof-of-concept due to its popularity. The objective of the project is to build a tool that can inform if a biscuit is healthy or not, helping consumers make healthier choices.

---

### Data Used

[`NTUC Fairprice`](https://www.fairprice.com.sg/category/biscuits): Data is scraped from NTUC Fairprice website, under category of Biscuits.
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

* [`01_webscraping`](/code/01_webscraping.ipynb): Scrape nutritional value data from NTUC Fairprice website
* [`02_cleaning`](/code/02_cleaning.ipynb): Cleaning of data
* [`03_EDA`](/code/03_eda.ipynb): Exploratory data analysis
* [`04_modelling`](/code/04_modelling.ipynb): Modelling of the data

---

### Conclusion

- Our decision tree model yields train and test accuracy greater than 0.9, and the train cross validation score also shows that the model is reliable to be deployed for classification.
- With this model, we developed an user-friendly tool (https://snack-o-meter.streamlit.app/) to help consumers identify if the biscuit of their choice is healthy or not, and recommend healthy alternatives.

---

### Recommendations

#### 1 - Increase Public Awareness
- Through marketing campaigns (offline and online campaigns)​
#### 2 - Expand the model to include other snack types​
- For example: Nuts and chips
#### 3 - Integrate tool into HPB’s existing Health 365 app 
- Intergration is beneficial as it makes Health 365 as “one stop app”​

---

### Cost-Benefit Analysis

  
