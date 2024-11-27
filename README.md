#Stock Movement Analysis Based on Social Media Sentiment
#Project Overview
This project aims to predict stock movements using sentiment analysis of user-generated content from Reddit. The steps include scraping relevant posts, performing sentiment analysis, and building a machine learning model to predict stock trends.
#Features
Data Scraping:
Fetch posts from Reddit subreddits.
Collect data such as title, content, upvotes, comments, and timestamps.
Sentiment Analysis:
Clean and preprocess post content.
Perform sentiment analysis to classify posts as positive or negative.
Prediction Model:
Use processed sentiment data to predict stock movements using machine learning.
#Technologies Used
Python Libraries:
praw: For Reddit API interaction.
pandas: For data manipulation.
TextBlob: For sentiment analysis.
scikit-learn: For machine learning model development.
Other Tools:
Reddit API for data scraping.
#Setup Instructions
Clone the Repository
git clone <repository_url>
cd stock-movement-analysis
2. Install Dependencies
pip install praw pandas textblob scikit-learn
3. Configure Reddit API Credentials
Visit Reddit App Preferences.
Create a Script Application.
Copy the following credentials:
Client ID: Found below your app name.
Client Secret: Found under the secret field.
User Agent: Custom string describing your application.
Replace placeholders in the code with your credentials:
CLIENT_ID = 'your_client_id'
CLIENT_SECRET = 'your_client_secret'
USER_AGENT = 'your_user_agent'
4. Run the Script
Data Scraping:
To scrape Reddit posts:
python data_scraping.py
This script fetches data from a subreddit (e.g., stocks) based on specific queries (e.g., AAPL).
Sentiment Analysis:
To perform sentiment analysis:
python sentiment_analysis.py
This script preprocesses and analyzes the sentiment of the scraped data.
Prediction Model:
To train and evaluate the model:
python prediction_model.py
This script uses sentiment data to predict stock movements.
#How It Works
Data Flow
Data Scraping:
Fetches stock-related posts using keywords like "AAPL" or "Tesla".
Stores results in a Pandas DataFrame.
Data Analysis:
Cleans content by removing noise and special characters.
Classifies posts as positive or negative based on sentiment polarity.
Prediction:
Uses a RandomForestClassifier to train on sentiment and simulate stock movements.
Evaluates the model with metrics like accuracy, precision, and recall.
#Example Usage
Sample Command:
Scrape posts about Apple stock:
data = fetch_reddit_posts('stocks', 'AAPL', limit=100)
Analyze sentiment of scraped posts:
analyzed_data = analyze_sentiment(data)
Train and test prediction model:
model.fit(X_train, y_train)
#Results
Model Performance:
Accuracy: ~88%
Precision: ~88%
Recall: 0.1
Sentiment scores reveal public perception about specific stocks.
#Future Enhancements
Extend scraping to multiple platforms (e.g., Twitter, Telegram).
Integrate advanced NLP techniques like BERT for sentiment analysis.
Include more stock features like volume and market trends for prediction.
#Contact
For queries or suggestions, reach out to:
Name: Niharika R A
Email: niharikara9162@gmail.com

