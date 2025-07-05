Twitter-API-Integration-Sentiment-Analysis
Project: Twitter API Data Pipeline with AWS Lambda
Author: Manishankerreddy Sanampudi
Tools: Python · Tweepy · AWS Lambda · PostgreSQL · Pandas · Sentiment Analysis
📬 Scenario
A data engineering task was assigned to build a robust and scalable tweet collection and processing pipeline for the @CommBank Twitter handle. The client provided basic starter materials including a notebook (getting_started.pdf) to get familiar with the Twitter API, and a requirement to fully automate the collection and storage of tweets, interactions, and sentiment scores.

🎯 Objectives
Authenticate and collect recent tweets using the Twitter API

Store tweet data in a relational database (PostgreSQL)

Capture replies, mentions, and quotes as interactions

Integrate AWS Lambda to schedule data collection automatically

Perform basic sentiment analysis on user interactions

⚙️ Workflow Overview
1. Twitter API Setup
Followed Twitter Developer Portal steps to obtain API credentials

Used Tweepy library for easy integration

2. Data Collection (via Python and Tweepy)
Authenticated using environment-secured tokens

Collected up to 200 tweets from @CommBank using user_timeline

Parsed tweet content, metadata, and engagement metrics

3. Database Design
Structured relational tables:

Users: stores user metadata

Tweets: core tweet information

Interactions: replies, mentions, quotes with sentiment scores

4. Lambda Deployment
Encapsulated tweet collection logic in a lambda_handler function

Connected to AWS RDS PostgreSQL instance securely

Ensured idempotent inserts using existence checks

5. Interaction Processing
Replies and mentions are fetched using query-based search

Each interaction is analyzed for sentiment and logged

📈 Key Features
Real-time or scheduled data collection via AWS Lambda

Sentiment scoring for user engagement insights

Optimized SQL insertion logic to avoid duplicates

Scalable and modular code suitable for expansion to other Twitter handles
