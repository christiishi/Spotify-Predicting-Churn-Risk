# Spotify User Segmentation & Churn Risk Analysis: From Free to Premium
This project analyzes Spotify user behavior to identify distinct listener segments and assess churn and conversion risk at the cluster level. Using unsupervised machine learning techniques, we segment both free and premium users based on listening habits, engagement patterns, and contextual usage. The analysis provides actionable insights to support targeted retention strategies for premium users and conversion strategies for free users.

## Problem Statement
Subscription-based platforms like Spotify face the dual challenge of retaining premium users while converting free users into paid subscribers. User behavior varies widely in engagement level, listening context, and willingness to upgrade or renew, making one-size-fits-all strategies ineffective.
This project aims to:
* Segment Spotify users based on behavioral and contextual listening patterns
* Identify clusters with high churn risk among premium users
* Identify free-user segments with strong conversion potential
* Provide targeted, data-driven recommendations for retention and conversion strategies 

## Data
**Source**: Kaggle – Spotify User Behavior Dataset

**Dataset Size**: 520 unique users

**Total Columns**: 20

Key Features:
* Subscription type (Free vs. Premium)
* Listening time slots and frequency
* Usage period and engagement level
* Mood and listening context
* Willingness to upgrade or continue premium subscription

## Data Preparation
* Ingested raw survey-style user data and standardized formatting (e.g., age and categorical fields)
* Cleaned data by handling missing values and stripping extraneous whitespace
* Applied a split-and-explode transformation to multi-select variables to capture the full depth of user behavior
* Segmented users by subscription plan (Free vs. Premium) to allow targeted clustering

## Modeling Approach
* Applied K-Means clustering separately to free and premium user groups
* Evaluated multiple cluster sizes using silhouette scores to determine optimal segmentation
  * Selected k = 3 clusters for both free and premium users, balancing cohesion and separation
* Calculated cluster-level feature averages and visualized them using heatmaps
* Used PCA-based scatterplots to assess cluster separation and interpret behavioral differences

## Key Insights
**Premium Users**
* The Wanderers: Relatively new premium users with lower engagement and weaker renewal intent, representing the highest churn risk
* The Nighttime Loyalists: Highly context-driven users with strong renewal intent and consistent nighttime listening habits
* The Everyday Groovers: Long-term, highly engaged users with the strongest retention and habitual usage patterns

**Free Users**
* The Almost-Premiums: Highly engaged users with the strongest willingness to upgrade, representing the most promising conversion target
* The Free-Tier Fanatics: Active users with no interest in upgrading despite high engagement
* The Casual Dabblers: Low-engagement users with minimal upgrade intent

These clusters revealed clear behavioral and contextual differences that directly inform conversion and retention priorities.

## Business Recommendations
Based on our analysis, we recommend the following actions:

**Free User Conversion Strategy**
* Prioritize Almost-Premium users with targeted premium nudges and benefit-focused messaging
* Highlight premium features aligned with their behavior, such as offline listening, high-quality audio, and unlimited skips
* Offer short-term premium trials during periods of high engagement with personalized prompts

**Premium User Retention Strategy**
* Focus retention efforts on Wanderers, the lowest-engagement premium segment
* Deploy targeted onboarding campaigns, playlist recommendations, and habit-building nudges
* Improve the early premium lifecycle experience, particularly within the first 30 days, using guided personalization and context-based notifications
* These targeted strategies enable Spotify to allocate marketing resources more efficiently while reducing churn and increasing conversion rates

## Limitations
* Small dataset size increases the risk of overfitting and limits generalizability
* Dataset does not track whether users eventually converted or churned, restricting long-term validation
* Gender distribution in the data is skewed, potentially introducing bias into behavioral insights

## My Contributions
* Interpreted cluster-level behavioral patterns and visualizations to assess churn and conversion risk
* Translated analytical insights into targeted, actionable recommendations for premium retention and free-user conversion strategies

## Contributors
**Christie Shin**

Shivani Vallamdas

Gema Zhu

Vishal Srivastava

Shuai Zhao
