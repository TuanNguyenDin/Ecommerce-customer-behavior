# Ecommerce-customer-behavior

## Goals of the Project

The project aims to analyze customer churn in an e-commerce platform by exploring various questions such as:
- Do certain age groups, genders, countries, or cities have higher or lower churn rates?
- How do membership duration and login frequency correlate with customer churn? Are long-term members less likely to churn?
- Do metrics like average session duration, pages per session, cart abandonment rate, and wishlist items indicate a higher propensity to churn?
- Is there a relationship between email open rates, customer service calls, product reviews, and social media engagement scores with churn?
- How do total purchases, average order value, days since last purchase, discount usage, returns rate, payment method diversity, lifetime value, and credit balance influence churn?
- Does mobile app usage play a role in customer retention or churn?
- Can we build a predictive model to identify customers at high risk of churning based on their behavioral and demographic data?

Expected outcomes include identifying key churn drivers, customer segmentation, behavioral patterns, impact of customer service, and data-driven recommendations for improving retention.

## Data Sources Used

The dataset is sourced from Kaggle, titled "E-commerce Customer Behavior Dataset" by user dhairyajeetsingh. It is loaded using the KaggleHub library in the notebook.

## Data Overview

The dataset contains various attributes related to customer interactions and characteristics within an e-commerce platform. The goal is to identify patterns, understand customer churn, and derive actionable insights.

### Key Features (Columns Description):
- **Demographic Information:** Age, Gender, Country, City.
- **Membership Details:** Membership Years, Login Frequency.
- **Website Interaction:** Session Duration (Avg), Pages Per Session, Cart Abandonment Rate, Wishlist Items.
- **Engagement & Communication:** Email Open Rate, Customer Service Calls, Product Reviews Written, Social Media Engagement Score.
- **Transactional Information:** Total Purchases, Payment Method Diversity, Lifetime Value, Credit Balance.
- **Mobile App Usage:** Mobile App Usage.
- **Churn Status:** A binary indicator (`Churned`) representing whether a customer has churned.
- **Signup Details:** Signup Quarter.

The dataset provides a rich foundation for exploring customer segmentation, predicting churn, and optimizing marketing strategies.
