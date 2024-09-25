# Facebook Marketplace Social Media Engagement Analysis

## Overview

This project analyzes social media engagement data from Thai fashion and cosmetics sellers on Facebook Marketplace. The analysis focuses on understanding user engagement patterns, post effectiveness, and provides insights for optimizing social media strategies.

## Project Description

The dataset captures comprehensive engagement metrics for Facebook posts including various types of reactions (likes, loves, wows, etc.), comments, and shares. Through exploratory data analysis and machine learning clustering, this project reveals patterns in social media engagement that can help businesses optimize their posting strategies.

## Dataset

The analysis is based on `Facebook_Marketplace_data.csv` which contains **7,050 posts** with the following key metrics:

### Features:
- **status_id**: Unique identifier for each Facebook post (1-7050)
- **status_type**: Type of post (video, photo, status, link)
- **status_published**: Date and time when the post was published (format: M/D/YYYY H:MM)
- **num_reactions**: Total number of reactions received (0-4,710)
- **num_comments**: Total number of comments received (0-20,990)
- **num_shares**: Total number of shares received (0-3,424)
- **num_likes**: Number of 'Like' reactions
- **num_loves**: Number of 'Love' reactions
- **num_wows**: Number of 'Wow' reactions
- **num_hahas**: Number of 'Haha' reactions
- **num_sads**: Number of 'Sad' reactions
- **num_angrys**: Number of 'Angry' reactions
- **Column1-4**: Empty columns (removed during preprocessing)

## Key Findings

### 1. **Post Type Distribution**
- Photos: 60.8% (4,288 posts)
- Videos: 33.1% (2,334 posts)
- Status updates: 5.2% (365 posts)
- Links: 0.9% (63 posts)

### 2. **Engagement Patterns by Post Type**
- **Status posts** generate the highest average reactions (439)
- **Video posts** receive the most comments (642) and shares (116)
- **Photo posts** have the lowest average reactions (181)
- **Link posts** show moderate reactions (370) but minimal comments (6) and shares (4)

### 3. **Correlation Analysis**
- **Strong correlation** between reactions and likes (Pearson: 0.995)
- **Moderate correlation** between reactions and comments at lower engagement levels
- **Weak positive correlation** between reactions and shares

### 4. **Timing Analysis**
- Engagement is distributed throughout the day
- Slightly higher concentrations in early morning and late evening hours

## Technical Analysis

### Data Preprocessing
- Cleaned and removed null columns (`Column1`, `Column2`, `Column3`, `Column4`)
- Converted data types for proper analysis
- Handled datetime formatting for time-based analysis
- Removed irrelevant identifier columns

### Machine Learning
- **K-Means Clustering** applied to identify engagement patterns
- **Optimal cluster number**: 3 (determined using elbow method)
- Features scaled using StandardScaler for better clustering performance
- Train-test split (80-20) for model validation

## Files in this Repository

- `Code.ipynb`: Main Jupyter notebook containing the complete analysis
- `Presentation_PDF.pdf`: Presentation slides summarizing key findings
- `README.md`: This documentation file
- `requirements.txt`: Python dependencies
- `Facebook_Marketplace_data.csv`: Dataset containing 7,050 Facebook posts from Thai fashion/cosmetics sellers

## Installation & Setup

### Prerequisites
- Python 3.7+
- Jupyter Notebook

## Usage

The notebook is structured in the following sections:

1. **Data Assessment**: Initial exploration and quality check
2. **Data Cleaning**: Preprocessing and data type corrections
3. **Exploratory Data Analysis**: Comprehensive analysis with visualizations
4. **K-Means Clustering**: Machine learning analysis for pattern recognition

Each section contains detailed analysis with conclusions and business insights.

## Key Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib & Seaborn**: Data visualization
- **Scikit-learn**: Machine learning (K-Means clustering, preprocessing)

## Business Impact

This analysis provides actionable insights for social media marketing:

- **Content Strategy**: Status posts generate highest reactions (439 avg) but represent only 5.2% of content
- **Video Strategy**: Videos drive the most comments (642 avg) and shares (116 avg), making them ideal for engagement
- **Photo Strategy**: Photos maintain consistent baseline engagement (181 reactions avg) and represent majority content (60.8%)
- **Link Optimization**: Links show surprising reaction potential (370 avg) but low shares/comments
- **Timing Optimization**: Post during early morning or late evening for better engagement
- **Resource Allocation**: Balance video content for high engagement with photo content for consistent reach

## Future Enhancements

- Sentiment analysis of comments
- Seasonal trend analysis
- Predictive modeling for engagement forecasting
- A/B testing framework for post optimization
- Integration with real-time social media APIs

