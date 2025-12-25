# Ecommerce-customer-behavior

## Notebook Link

You can view and run the analysis notebook on Google Colab: [Open in Colab](https://colab.research.google.com/github/TuanNguyenDin/Ecommerce-customer-behavior/blob/main/ecommerce_churn.ipynb)

## Goals of the Project

The project aims to analyze customer churn in an e-commerce platform by exploring various questions such as demographic influences, membership correlations, engagement metrics, transactional factors, and building predictive models to identify at-risk customers.

## Data Overview

### Source
The dataset is sourced from Kaggle, titled "E-commerce Customer Behavior Dataset" by user dhairyajeetsingh. It is loaded using the KaggleHub library in the notebook.

#### Sample Data
Here is a sample of the first 5 rows from the dataset:

| Age | Gender | Country | City       | Membership_Years | Login_Frequency | Session_Duration_Avg | Pages_Per_Session | Cart_Abandonment_Rate | Wishlist_Items | Total_Purchases | Average_Order_Value | Days_Since_Last_Purchase | Discount_Usage_Rate | Returns_Rate | Email_Open_Rate | Customer_Service_Calls | Product_Reviews_Written | Social_Media_Engagement_Score | Mobile_App_Usage | Payment_Method_Diversity | Lifetime_Value | Credit_Balance | Churned | Signup_Quarter |
|-----|--------|---------|------------|------------------|-----------------|----------------------|-------------------|-----------------------|----------------|-----------------|----------------------|--------------------------|----------------------|--------------|-----------------|-----------------------|-------------------------|-----------------------------|------------------|--------------------------|----------------|---------------|---------|----------------|
| 43.0 | Male   | France  | Marseille | 2.9              | 14.0            | 27.4                 | 6.0               | 50.6                  | 3.0            | 9.0             | 94.72                | 34.0                     | 46.4                 | 2.0          | 17.9            | 9.0                   | 4.0                     | 16.3                        | 20.8             | 1.0                      | 953.33         | 2278.0        | 0       | Q1             |
| 36.0 | Male   | UK      | Manchester| 1.6              | 15.0            | 42.7                 | 10.3              | 37.7                  | 1.0            | 19.5            | 82.45                | 71.0                     | 57.96                | 9.2          | 42.8            | 7.0                   | 3.0                     |                             | 23.3             | 3.0                      | 1067.47        | 3028.0        | 0       | Q4             |
| 45.0 | Female | Canada  | Vancouver | 2.9              | 10.0            | 24.8                 | 1.6               | 70.9                  | 1.0            | 9.1             | 165.52               | 11.0                     | 12.24                | 11.5         | 0.0             | 4.0                   | 1.0                     |                             | 8.8              |                          | 1289.75        | 2317.0        | 0       | Q4             |
| 56.0 | Female | USA     | New York  | 2.6              | 10.0            | 38.4                 | 14.8              | 41.7                  | 9.0            | 15.0            | 147.33               | 47.0                     | 44.1                 | 5.4          | 41.4            | 2.0                   | 5.0                     | 85.9                        | 31.0             | 3.0                      | 2340.92        | 2674.0        | 0       | Q1             |
| 35.0 | Male   | India   | Delhi     | 3.1              | 29.0            | 51.4                 |                   | 19.1                  | 9.0            | 32.5            | 141.3                | 73.0                     | 25.2                 | 5.5          | 37.9            | 1.0                   | 11.0                    | 83.0                        | 50.4             | 4.0                      | 3041.29        | 5354.0        | 0       | Q4             |

### Description
The dataset contains various attributes related to customer interactions and characteristics within an e-commerce platform. The goal is to identify patterns, understand customer churn, and derive actionable insights.

### Dataset Columns

| Column Name | Description |
|-------------|-------------|
| Age | Customer's age |
| Gender | Customer's gender |
| Country | Customer's country |
| City | Customer's city |
| Membership_Years | Number of years as a member |
| Login_Frequency | Frequency of logins |
| Session_Duration_Avg | Average session duration |
| Pages_Per_Session | Average pages per session |
| Cart_Abandonment_Rate | Rate of cart abandonment |
| Wishlist_Items | Number of wishlist items |
| Total_Purchases | Total number of purchases |
| Average_Order_Value | Average value per order |
| Days_Since_Last_Purchase | Days since last purchase |
| Discount_Usage_Rate | Rate of discount usage |
| Returns_Rate | Rate of returns |
| Email_Open_Rate | Rate of email opens |
| Customer_Service_Calls | Number of customer service calls |
| Product_Reviews_Written | Number of product reviews written |
| Social_Media_Engagement_Score | Social media engagement score |
| Mobile_App_Usage | Mobile app usage |
| Payment_Method_Diversity | Diversity in payment methods |
| Lifetime_Value | Lifetime value of the customer |
| Credit_Balance | Credit balance |
| Churned | Binary indicator of churn (1 for churned, 0 otherwise) |
| Signup_Quarter | Quarter of signup |

## Data Storytelling

Imagine a bustling e-commerce platform where customers come and go. Our data tells a story of engagement and dissatisfaction. Customers who frequently log in, spend more time browsing pages, and open emails are the loyal ones—less likely to churn, forming the backbone of the business. On the flip side, those who abandon carts, call customer service often, or haven't purchased in days are signaling trouble, often leading to churn. Through this analysis, we uncover that retention isn't just about sales—it's about building meaningful interactions and addressing pain points early.

## Hypotheses Based on the Insights

- Do certain age groups, genders, countries, or cities have higher or lower churn rates?
- How do membership duration and login frequency correlate with customer churn? Are long-term members less likely to churn?
- Do metrics like average session duration, pages per session, cart abandonment rate, and wishlist items indicate a higher propensity to churn?
- Is there a relationship between email open rates, customer service calls, product reviews, and social media engagement scores with churn?
- How do total purchases, average order value, days since last purchase, discount usage, returns rate, payment method diversity, lifetime value, and credit balance influence churn?
- Does mobile app usage play a role in customer retention or churn?
- Can we build a predictive model to identify customers at high risk of churning based on their behavioral and demographic data?

## Analysis Plan

The analysis follows a structured approach to understand and predict customer churn:

1. **Data Collection and Preparation**:
   - Load the dataset from Kaggle using KaggleHub.
   - Handle missing values, encode categorical variables, and scale numerical features.
   - Split data into training and testing sets (80/20 ratio).

2. **Exploratory Data Analysis (EDA)**:
   - Visualize distributions of key variables using histograms and box plots.
   - Analyze churn distribution across demographic and behavioral features.
   - Identify patterns in engagement metrics and transactional data.

3. **Correlation Analysis**:
   - Compute correlations between features and churn status.
   - Generate heatmaps to highlight strong positive and negative correlations.
   - Summarize key factors influencing churn.

4. **Predictive Modeling**:
   - Build a Logistic Regression model to predict churn.
   - Evaluate model performance using accuracy, precision, recall, F1-score, and ROC AUC.
   - Analyze confusion matrix and feature importance.

5. **Insights and Recommendations**:
   - Derive key insights from correlations and model results.
   - Formulate hypotheses based on findings.
   - Provide actionable recommendations for improving customer retention.

## Tools and Technologies

- **Python**: Programming language used for analysis.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib**: Plotting and visualization.
- **Seaborn**: Statistical data visualization.
- **Statsmodels**: Statistical modeling.
- **KaggleHub**: Dataset downloading from Kaggle.
- **Scikit-learn**: Machine learning for predictive modeling.

## Key Insights Discovered

- **Strong Positive Correlations with Churn**: Customer_Service_Calls (0.29), Cart_Abandonment_Rate (0.28), Days_Since_Last_Purchase (0.15).
- **Strong Negative Correlations with Churn**: Pages_Per_Session (-0.22), Session_Duration_Avg (-0.22), Email_Open_Rate (-0.22), Mobile_App_Usage (-0.21), Login_Frequency (-0.20), Wishlist_Items (-0.19), Social_Media_Engagement_Score (-0.18), Product_Reviews_Written (-0.17), Total_Purchases (-0.16), Credit_Balance (-0.15).
- **Model Performance**: Logistic Regression achieved 77.56% accuracy, 67.88% precision, 42.42% recall, 52.21% F1-score, and 0.79 ROC AUC.
- Customers with higher engagement (more logins, longer sessions, higher email open rates) are less likely to churn.
- Dissatisfaction indicators like frequent service calls and high cart abandonment correlate with higher churn.

## Recommendations Based on Analysis Results

- **Improve Churn Identification**: Enhance model recall by trying advanced models like RandomForest or Gradient Boosting, or addressing class imbalance.
- **Targeted Interventions**: Provide proactive support for customers with high service calls; send reminders for abandoned carts.
- **Boost Engagement**: Encourage longer sessions, more logins, and higher email engagement through personalized content.
- **Retention Strategies**: Focus on high-risk customers identified by the model with offers, discounts, or improved customer service.
- **Monitor Key Metrics**: Regularly track cart abandonment, service calls, and engagement scores to predict and prevent churn.
