\# Maximizing Revenue for Taxi Cab Drivers through Payment Type Analysis



\## Problem Statement

In the fast-paced taxi booking sector, maximizing revenue is essential for

drivers. This project examines whether the payment method (card vs cash)

affects the fare amount, and whether customers can be nudged toward a payment

method that earns drivers more, without hurting the customer experience.



\## Objective

Run an A/B-style hypothesis test to find out if there is a significant

difference in average fare between customers who pay by card and customers

who pay by cash.



\## Dataset

NYC Yellow Taxi trip data, January 2020 (\~630K trips).



Columns used: `passenger\_count`, `trip\_distance`, `payment\_type`,

`fare\_amount`, and trip duration (calculated from pickup and dropoff times).



\## Approach

1\. \*\*Data cleaning:\*\* kept card and cash payments only, removed trips with 0

&#x20;  or more than 5 passengers, and removed negative values and outliers

2\. \*\*Exploratory data analysis:\*\* histograms, pie chart, and stacked bar plot

3\. \*\*Regression analysis:\*\* relationship between trip duration and fare amount

4\. \*\*Normality check:\*\* QQ plots of fare amount for each payment type

5\. \*\*Hypothesis testing:\*\* Welch's two-sample t-test on fare amount by

&#x20;  payment type



\*\*Hypotheses\*\*

\- Null (H0): There is no difference in average fare between card and cash

&#x20; customers.

\- Alternative (H1): There is a difference in average fare between card and

&#x20; cash customers.



\## Key Findings



| Payment Type | Average Fare Amount |

|--------------|---------------------|

| Card         | $10.24              |

| Cash         | $9.92               |



\- Card customers pay about \*\*$0.31 more per trip\*\* on average than cash

&#x20; customers, roughly 3.1% higher.

\- The t-test gave a \*\*t-statistic of 20.53\*\* and a \*\*p-value below 0.001\*\*,

&#x20; so the null hypothesis is rejected at the 5% significance level.

\- There is a statistically significant difference in average fare between

&#x20; card and cash customers.

\- Trip duration is a statistically significant predictor of fare amount

&#x20; (regression analysis).



\## Business Insight

Encouraging card payments can increase average revenue per trip for drivers.

The difference per trip is small, but across thousands of trips it adds up.



\## Recommendations

\- Encourage customers to pay by card through incentives or discounts.

\- Make card payment seamless and secure to improve convenience and adoption.



\## Limitations

\- The result shows an association, not proof that card payment causes higher

&#x20; fares. Card customers may simply take longer or farther trips.

\- With a dataset this large, even small differences become statistically

&#x20; significant, so the practical size of the gap ($0.31) matters as much as

&#x20; the p-value.

\- The data covers only January 2020.



\## Tools Used

Python, Pandas, Matplotlib, Seaborn, SciPy, Statsmodels



\## Project Structure

```

taxi-revenue-payment-analysis/

├── Maximizing\_Revenue\_for\_Taxi\_Cab\_Drivers\_Project.ipynb

├── taxi\_data\_2020.csv

├── README.md

└── presentation/

&#x20;   └── Maximizing\_Revenue\_for\_Taxi\_Cab\_Drivers\_through\_Payment\_Type\_Analysis.pptx

```



\## How to Run

1\. Download or clone this repository.

2\. Install the libraries: `pip install pandas matplotlib seaborn scipy statsmodels`

3\. Open the notebook in Jupyter Notebook or JupyterLab.

4\. Run all cells. The notebook and `taxi\_data\_2020.csv` must stay in the same

&#x20;  folder.

