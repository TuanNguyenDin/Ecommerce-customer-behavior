# Ecommerce-customer-behavior

## Goals of the Project

The project aims to analyze customer churn in an e-commerce platform by exploring various questions such as demographic influences, membership correlations, engagement metrics, transactional factors, and building predictive models to identify at-risk customers.

## Data Overview

### Source
The dataset is sourced from Kaggle, titled "E-commerce Customer Behavior Dataset" by user dhairyajeetsingh. It is loaded using the KaggleHub library in the notebook.

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

## Hypotheses Based on the Insights

- Do certain age groups, genders, countries, or cities have higher or lower churn rates?
- How do membership duration and login frequency correlate with customer churn? Are long-term members less likely to churn?
- Do metrics like average session duration, pages per session, cart abandonment rate, and wishlist items indicate a higher propensity to churn?
- Is there a relationship between email open rates, customer service calls, product reviews, and social media engagement scores with churn?
- How do total purchases, average order value, days since last purchase, discount usage, returns rate, payment method diversity, lifetime value, and credit balance influence churn?
- Does mobile app usage play a role in customer retention or churn?
- Can we build a predictive model to identify customers at high risk of churning based on their behavioral and demographic data?

## Recommendations Based on Analysis Results

- **Improve Churn Identification**: Enhance model recall by trying advanced models like RandomForest or Gradient Boosting, or addressing class imbalance.
- **Targeted Interventions**: Provide proactive support for customers with high service calls; send reminders for abandoned carts.
- **Boost Engagement**: Encourage longer sessions, more logins, and higher email engagement through personalized content.
- **Retention Strategies**: Focus on high-risk customers identified by the model with offers, discounts, or improved customer service.
- **Monitor Key Metrics**: Regularly track cart abandonment, service calls, and engagement scores to predict and prevent churn.
