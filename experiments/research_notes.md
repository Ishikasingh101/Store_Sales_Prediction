### Q1. How can we use `transactions.csv` if we don’t have it in the test set?

The `transactions.csv` file shows how many people visited each store on past dates.  
But we don’t have this data for future dates in the test set, so we can’t use it directly.

---

# What we can do:

- We can look at past patterns in the transactions data.
- For example, how many people usually visit each store on a Monday, Tuesday, etc.
- Then we can add this average number of visitors to the test set.

---

# Why it might help:

Even if we don’t know the exact number of visitors in the future,  
we can give the model a good guess based on the past.  
This helps the model understand how busy a store might be on a certain day and make better predictions.


-----------------------------------------------------------------------------------------------------------------------------------------------


###  What We Can Do by Combining Datasets :


#  1. Sales by Store Type or Cluster
- Merge `train.csv` with `stores.csv`
- See which store types or clusters perform better.

#  2. Sales vs. Transactions
- Merge `train.csv` with `transactions.csv`
- Understand if higher footfall results in higher sales.

#  3. Promotions
- Study the impact of `onpromotion` on sales.
- Group by promotional status and compare average sales.

#  4. Holiday Impact
- Merge `train.csv` with `holidays_events.csv`
- See how holidays affect sales differently.



-----------------------------------------------------------------------------------------------------------------------------------------------


### Trend, Seasonality & Anomaly Analysis :

We can explore trends, seasonality, and anomalies in the store sales data.  
This will help us understand how sales behave over time and what factors might affect them.

---

# 1. Trend Analysis

We can check if sales or customer visits are increasing or decreasing over time.

- We'll use `train.csv` for sales and `transactions.csv` for customer footfall.
- We can plot line graphs over time for each store or overall.
- We can also use 7-day or 30-day rolling averages to smooth the data and highlight long-term trends.

---

# 2. Seasonality

We want to find repeating patterns in sales, such as:

- Higher sales on weekends or specific weekdays.
- Higher sales during certain months (like holiday season).
- We'll use `holidays_events.csv` to see how national or local holidays affect sales.

---

# 3. Anomaly Detection

We will look for unusual spikes or drops in sales that don’t fit the normal pattern.

- We'll identify outliers using methods like z-score or IQR.
- We’ll then check if those spikes relate to holidays, promotions, or external events like oil prices.

---

