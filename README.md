# AI-Powered Market Trend & Consumer Sentiment Forecaster

An intelligent system that analyzes market trends and consumer sentiment using AI, providing real-time insights through data aggregation from multiple sources including e-commerce reviews, news, and social media.

## 🚀 Features

- **Multi-Source Data Integration**: Aggregates data from Amazon, Flipkart, news APIs, and Reddit
- **Sentiment Analysis**: Advanced sentiment analysis using transformers and NLP techniques
- **Topic Modeling**: LDA-based topic modeling to identify key themes in consumer feedback
- **RAG System**: Retrieval-Augmented Generation using FAISS vector database for intelligent query responses
- **Real-Time Monitoring**: Automated scheduling for continuous data collection and analysis
- **Interactive Dashboard**: Streamlit-based visualization dashboard with Plotly charts
- **Trend Detection**: Identifies sentiment spikes and emerging trends
- **Notification System**: Automated alerts via email and Slack

## 📋 Table of Contents

- [Installation](#installation)
- [Data Processing Pipeline](#data-processing-pipeline)
- [API Integrations](#api-integrations)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/Loki12103/AI-Powered-Market-Trend-Consumer-Sentiment-Forecaster_.git
cd AI-Powered-Market-Trend-Consumer-Sentiment-Forecaster_
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
Create a `.env` file in the root directory with your API keys:
```
GOOGLE_API_KEY=your_google_api_key
SLACK_WEBHOOK_URL=your_slack_webhook
EMAIL_CREDENTIALS=your_email_credentials
REDDIT_API_KEY=your_reddit_api_key
NEWS_API_KEY=your_news_api_key
RAPID_API_KEY=your_rapid_api_key
```

## 📊 Data Processing Pipeline

### Step 1: Data Cleaning (`cleaning.py`)
- Cleans raw data from e-commerce platforms
- Removes duplicates, handles missing values
- Standardizes data format for better analysis

### Step 2: Data Merging (`merged_data.py`)
- Merges product review data from Amazon and Flipkart
- Consolidates multiple data sources into unified format
- Maintains data integrity across different platforms

### Step 3: Data Reduction (`reduce_data.py`)
- Optimizes large datasets for efficient processing
- Filters relevant data points
- Reduces computational overhead while preserving insights

### Step 4: Category Classification (`category.py`)
- Defines and assigns product categories
- Enables category-wise trend analysis
- Supports multi-category sentiment tracking

### Step 5: Sentiment Analysis (`sentiment.py`)
- Applies transformer-based sentiment analysis
- Assigns sentiment scores to reviews and feedback
- Generates temporal data for trend analysis

### Step 6: Topic Modeling (`topic_modeling_2.py`)
- Applies LDA (Latent Dirichlet Allocation)
- Extracts key topics from consumer feedback
- Provides thematic insights into customer opinions

## 🔌 API Integrations

### 1. News API (`news.py`)
- Fetches latest market and product news
- Analyzes news sentiment for trend detection
- Identifies potential market shifts

### 2. Reddit API (`reddit_api.py`)
- Monitors relevant subreddits for consumer discussions
- Tracks social sentiment and trending topics
- Provides real-time community insights

### 3. Rapid API (`rapid_api.py`)
- Aggregates additional review data
- Cross-platform sentiment validation
- Enhanced data coverage

## 🎯 Usage

### Running the Dashboard

```bash
streamlit run dashboard.py
```

The dashboard provides:
- Real-time sentiment trends visualization
- Category-wise analysis
- Interactive charts and graphs
- AI-powered insights using RAG system

### Running Individual Components

**Add data to Vector Database:**
```bash
python add_data_vector_db.py
```

**Analyze Review Sentiment Trends:**
```bash
python review_sentiment_trend_spike.py
```

**Manual API Data Collection:**
```bash
# News data
python external_api/news.py

# Reddit data
python external_api/reddit_api.py

# Rapid API data
python external_api/rapid_api.py
```

## 📁 Project Structure

```
AI-Powered-Market-Trend-Consumer-Sentiment-Forecaster_/
│
├── data analysis/                 # Data processing scripts
│   ├── cleaning.py               # Data cleaning
│   ├── merged_data.py            # Data merging
│   ├── reduce_data.py            # Data reduction
│   ├── category.py               # Category classification
│   ├── sentiment.py              # Sentiment analysis
│   └── topic_modeling_2.py       # Topic modeling
│
├── external_api/                 # External API integrations
│   ├── news.py                   # News API integration
│   ├── reddit_api.py             # Reddit API integration
│   ├── rapid_api.py              # Rapid API integration
│   ├── sentiment_news_spike.py   # News sentiment analysis
│   └── sentiment_reddit_spike.py # Reddit sentiment analysis
│
├── notification/                 # Notification system
│   └── notification.py           # Email and Slack notifications
│
├── consumer_sentiment_faiss/     # FAISS vector database
│   └── index.faiss              # Vector embeddings
│
├── final data/                   # Processed datasets
│   ├── category_wise_lda_output_with_topic_labels.csv
│   ├── news_data_with_sentiment.csv
│   ├── rapid_api_reviews_final.csv
│   └── reddit_category_trend_data.xlsx
│
├── dashboard.py                  # Main Streamlit dashboard
├── main.py                       # Main application entry
├── add_data_vector_db.py        # Vector DB management
├── review_sentiment_trend_spike.py # Trend detection
├── requirements.txt              # Python dependencies
└── README.md                     # Project documentation
```

## 🧰 Technologies Used

- **Python 3.x** - Core programming language
- **Streamlit** - Interactive dashboard framework
- **Plotly** - Data visualization
- **Transformers** - Sentiment analysis models
- **Scikit-learn** - Machine learning and topic modeling
- **FAISS** - Vector database for RAG
- **LangChain** - RAG framework
- **Google Gemini** - AI-powered insights
- **Pandas** - Data manipulation
- **NLTK** - Natural language processing
- **Schedule** - Task automation

## 📈 Key Features Explained

### Sentiment Analysis
Uses state-of-the-art transformer models to analyze consumer sentiment across multiple data sources, providing accurate and nuanced sentiment scores.

### RAG System
Implements Retrieval-Augmented Generation using FAISS vector database to provide context-aware AI responses about market trends and consumer sentiment.

### Automated Monitoring
Scheduled tasks run daily to collect fresh data from news sources and social media, ensuring up-to-date insights.

### Trend Detection
Identifies significant spikes in sentiment and emerging market trends through advanced statistical analysis and pattern recognition.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is part of the Infosys Springboard program.

## 📧 Contact

For questions or support, please open an issue on GitHub.

---

**Note**: Remember to configure your API keys in the `.env` file before running the application.
