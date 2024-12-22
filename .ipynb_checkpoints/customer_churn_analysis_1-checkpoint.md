# **Customer Churn Analysis Using Python**


## **Introduction**


### *i) Context*
Customer churn, or the rate at which customers discontinue a company's subscription services, is a key concern for companies in the subscription-based industry. Understanding why customers churn and identifying associated patterns are crucial for companies striving to enhance customer retention and profitability. This report presents a comprehensive customer churn analysis conducted using Python, leveraging data science tools and techniques to reveal insights into churn behaviour.

### *ii) Objective*
The goal of this project is to interpret patterns that contribute to higher customer churn rates and come up with recommendations to help reduce this phenomenon from occurring.


## **Data Description**
The dataset has 64,374 records of customer information containing the following columns:

| Column                 | Description                                                                |
| :-----                 | -----:                                                                     |
| Customer ID            | Unique identifier for each customer                                        |
| Age                    | Age of the customer                                                        |
| Gender                 | Gender of the customer                                                     |
| Tenure                 | Duration of the customer's subscription, relative to their contract length |
| Usage Frequency        | Monthly usage frequency                                                    |
| Support Calls          | Number of support calls made by the customer                               |
| Payment Delay          | Number of delayed payments                                                 |
| Subscription Type      | Subscription plan (Basic, Premium, Standard)                               |
| Contract Length        | Contract Type (Monthly, Quarterly, Yearly)                                 |
| Total Spend            | Total amount spent by the user                                             |
| Last Interaction       | Months since last interaction                                              |
| Churn                  | Churn status(1 = Churned, 0 = Retained)                                    |

By exploring these variables, we aim to uncover patterns and identify potential indicators of churn.


## **Data Cleaning and Processing**
We began our analysis by importing essential Python libraries, including pandas for data manipulation, numpy for numerical computations, and matplotlib and seaborn for data visualization. After importing the necessary libraries, we loaded the dataset, which was provided as a zip file, and extracted the data for further analysis.
To understand the structure and contents of the dataset, we performed an initial exploratory check. This included:
- Reviewing the dataset's overall characteristics, such as the number of rows and columns.
- Examining column names and their data types to ensure compatibility with our planned analysis.
- Displaying the first five and last five records to get a snapshot of the data.

Next, we moved on to data cleaning and processing to ensure the dataset was ready for analysis:
1. Missing Values: We inspected the dataset for missing values across all columns and confirmed none were present.
2. Duplicates: We checked for duplicate records, ensuring no redundant data entries existed.
3. Descriptive Statistics: We ran summary statistics to identify any irregularities in the data, such as unexpected outliers, inconsistencies, or anomalies.


## **Exploratory Data Analysis**

### *i) Univariate Analysis*
- **Usage Frequency Distribution:**  The usage frequency of customers is normally distributed, as evidenced by approximately equal mean and median values shown by the box plot.
- **Gender Distribution:** The company has more female customers compared to male ones. Female customers comprise 53.4% of the total customers, and male customers consist of 46.4% of the total customers.
- **Distribution of Tenure:** The histogram representing the distribution of tenure is right-skewed, meaning that a lot of customers are new, or churn is higher among newer customers.
- **Distribution of customers by age:** The majority of customers are aged between 50 and 59 years old.
- **Churn Distribution:**  The number of active customers(33881) is slightly more than that of churned customers(30493). This is a major cause for concern.
- **Distribution of Subscription Types:** Most customers subscribe to the Standard Package. There are notably slight differences in the packages customers subscribe to(Standard-21502, Basic-21451, Premium-21421).


### *ii) Multivariate Analysis*
- **Subscription Type vs Churn:** We discovered that most of the customers subscribed to the Premium package, whereas the basic package was the least subscribed to.
- **Contract Length vs Churn:**  The resulting analysis shows that customers who subscribed on a monthly basis churned the most(11421). Conversely, the majority of the retained customers subscribed on a quarterly basis(11657).
- **Age Group vs Churn:** The customer base mainly consists of individuals within the age range of 50 and 59 years. There are very few customers aged between 18 and 19 years, assuming that an individual must be of legal age to subscribe to the various packages on offer.
- **Gender vs Churn:** Female customers churned the most compared to male customers.
- **Correlation Matrix:** From the matrix, it is observed that payment delay has the highest correlation to churn(0.56). Last interaction has the least correlation to churn(-0.00).


## Feature Engineering
We improved our dataset by creating new features to make the information easier to analyze and uncover useful patterns:
1. Standardizing Subscription Duration:
   - We introduced a new column called **Adjusted Tenure** to ensure all customer subscription durations were measured in the same unit—months.
   - This standardization ensured consistency in the analysis, making it easier to compare subscription lengths across customers and derive actionable insights.
2. Churn-related features:
   - We added two new variables, **churn_data** and **contract_churn**, to facilitate visualization and analysis:
     1. **churn_data:** Designed to help analyze the relationship between Subscription Types and Churn, enabling us to create bar charts for visual exploration
     2. **contract_churn:**  Created to examine how Contract Length correlates with Churn, providing a deeper understanding of contract-related trends.
3. Age Group Binning:
   - We grouped customers into age categories instead of using individual ages.
This allowed us to identify patterns in how customers of different age groups behave, such as which groups are more likely to leave or stay.


## **Key Insights**
- The majority of the customers subscribing to the company’s various packages are aged between 50 and 59 years.
- Female customers churned the most from the company’s services, with a higher percentage discontinuing their subscriptions compared to those that were retained.
- Customers who had a higher number of delayed payments had the highest probability of churning from the company’s services.- 
Customers with a high number of support calls were more likely to churn.- 
More customers subscribed on a quarterly basis than on a yearly basis- .
The percentage of customers who have churned(47.4%) is almost similar to the percentage of customers that have been retained(52.6%), which is a huge cause for concer

## **Recommendations**
- Tailor-make services across the various packages to suit the needs and preferences of female customers.
- Increase the benefits across all the subscription packages to lure new customers and raise their chances of retaining the current ones.
- Act swiftly on support calls made by customers to ensure that the same problems are not repeated in the future.
- Offer discounts on yearly and quarterly payment plans to entice customers to subscribe to those payment terms and thus increase their chances of continuing to subscribe to the services offered in the long run.
- Segment the customers based on age groups and thus tailor their services to suit the needs and preferences of individuals across all age groups.
n.

   
