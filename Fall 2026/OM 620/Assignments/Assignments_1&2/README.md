## Assignment 1

### Question 1 — DataFrame Formatting
As you load and inspect your transaction dataframe, you'll notice the column names don't follow a consistent convention. Make the necessary changes to ensure all column names follow the same convention as the metadata.

---

### Question 2 — Data Inspection
Inspect the numeric features of your dataframe with the `describe` function. Provide a summary of these features, and in case there are any oddities/anomalies in your dataframe, locate and correct them.

---

### Question 3 — NaN Values
Your transactional dataset includes many missing values. Find and address (in your dataframe) the missing values by column. 

---

### Question 4 — Extracting the Country Values
To apply broader breakdowns of your transactional dataset, it will be helpful to add a country column. Recall that the metadata indicates the country information is somewhat captured in the site column. 

Create a new `country` column by using the `manufacturing_site` information. To do so, you will need the helper function [`str.startswith()`](https://pydata.org), which is defined for a pandas `Series` object.
As the documentation states, `str.startswith()` tests if the start of each string element matches a given pattern.

---

### Question 5 — Helpful Dimensional Information
It's time to focus on the subset of this dataset we need. Since we ultimately want to calculate safety stock, focus on finished goods designated as **"make to stock."** Create a filtered subset of your transaction dataset and write appropriate code to answer the following questions *(for the filtered data)*:
* How many unique SKUs are we working with?
* How many unique Manufacturing Sites are we working with?
* How many Divisions are we working with?
* What are the top and bottom 10 transactions by order quantity?
* What are the top and bottom 10 transactions by total sales value? *(**Hint:** Sales is not a feature in this dataset, so we must calculate it using the existing features.)*

## Assignment 2

### Question 1 — Required Transformation
Create a transformed dataset to filter for appropriate SKUs that are also aggregated with the following statistics:
* Minimum of quantity
* Maximum of quantity
* Average of quantity
* Median of quantity
* Variance of quantity
* Standard deviation of quantity
* Average lead time

---

### Question 2 — Safety Stock Calculation
Use the transformed data from Question 1 to calculate three safety stock values for each SKU for the service level coefficients of **75%**, **90%**, and **95%**. 

---

### Question 3 — Safety Stock Distribution
Now that we have the safety stock values, write appropriate code to answer the following questions *(for this question, you may focus on the **95%** service level coefficient)*:
* Which SKU has the largest safety stock?
* Which SKU has the smallest safety stock?
* What is the average safety stock value across all SKUs?

