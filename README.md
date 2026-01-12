# 🎬 TMDB 5000 Movie Dataset - EDA & Recommendation System

A comprehensive exploratory data analysis and content-based movie recommendation system built on the TMDB 5000 Movie Dataset.

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Ready-20BEFF.svg)](https://www.kaggle.com/)

## 📋 Overview

This project provides an in-depth analysis of 5000 movies from The Movie Database (TMDB), featuring:

- **Advanced Data Cleaning**: Robust JSON parsing, missing value handling, and data validation
- **Comprehensive EDA**: 40+ visualizations covering temporal trends, genre analysis, budget tiers, and more
- **Feature Engineering**: ROI calculations, profitability metrics, budget categorization, and director/actor extraction
- **Recommendation System**: Content-based filtering using TF-IDF and cosine similarity with weighted ratings
- **Statistical Analysis**: Correlation analysis, outlier detection, and performance metrics

## 🎯 Key Features

### 📊 Exploratory Data Analysis
- **Temporal Trends**: Movie production over time, budget/revenue evolution, rating trends
- **Genre Analysis**: Performance metrics by genre (rating, profit, ROI)
- **Financial Insights**: Success stories, flops, budget tier analysis, ROI patterns
- **People Analytics**: Top directors, actors, and their impact on movie performance
- **Seasonal Patterns**: Release month analysis and seasonal trends
- **Genre Evolution**: How genres have changed over decades

### 🎯 Recommendation System
- **Content-Based Filtering**: TF-IDF vectorization with cosine similarity
- **Weighted Ratings**: IMDB-style formula balancing vote count and average
- **Smart Matching**: Fuzzy title matching with partial search support
- **Advanced Filtering**: Filter by year range, genre, or custom criteria
- **Rich Features**: Combines genres, keywords, overview, cast, and director (2x weight)

### 🔧 Feature Engineering
- **Financial Metrics**: Net profit, ROI, profitability ratio
- **Temporal Features**: Release year, month, day of week, decade
- **Categorization**: Budget tiers (Low/Medium/High/Very High)
- **People Extraction**: Director and lead actor from JSON data
- **Count Features**: Number of genres, keywords, cast, crew, etc.

## 📁 Dataset

**Source**: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) on Kaggle

**Files**:
- `tmdb_5000_movies.csv` - Movie metadata (budget, revenue, genres, etc.)
- `tmdb_5000_credits.csv` - Cast and crew information

**Size**: ~5000 movies with 20+ features each

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas seaborn matplotlib scikit-learn scipy
```

### Running on Kaggle

1. Go to [Kaggle](https://www.kaggle.com/)
2. Create a new notebook
3. Add the TMDB 5000 Movie Metadata dataset
4. Upload `tmdb-5k-movie-eda-recommendation-system-improved.ipynb`
5. Run all cells

### Running Locally

```bash
# Clone the repository
git clone https://github.com/yourusername/tmdb-5k-movie.git
cd tmdb-5k-movie

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook tmdb-5k-movie-eda-recommendation-system-improved.ipynb
```

**Note**: Update file paths from `/kaggle/input/...` to your local data directory.

## 📊 Sample Visualizations

The notebook includes 40+ professional visualizations:

- Distribution plots with optimized KDE rendering
- Time series analysis with trend lines
- Correlation heatmaps
- Genre performance comparisons
- Budget tier analysis
- Director/actor impact charts
- Seasonal release patterns
- Genre evolution over decades

## 🎯 Recommendation System Usage

```python
# Basic recommendation
get_recommendations('Inception', n=10)

# Filter by year
get_recommendations('Iron Man', n=10, min_year=2010)

# Filter by genre
get_recommendations('Toy Story', n=10, genre_filter='Animation')

# Show similarity scores
get_recommendations('The Matrix', n=10, show_scores=True)
```

**Sample Output**:
```
🎬 Recommendations for "Inception":
====================================
title_x              release_year  vote_average  weighted_rating  similarity_score
Interstellar         2014          8.1           7.953            0.456
The Prestige         2006          8.2           8.015            0.389
Memento              2000          8.2           7.998            0.367
Shutter Island       2010          8.0           7.876            0.342
The Matrix           1999          8.1           7.945            0.328
```

## 📈 Key Insights

### Financial Insights
- Strong correlation between budget and revenue (r = 0.73)
- Lower budget films often achieve higher ROI percentages
- Budget tier doesn't guarantee better ratings

### Genre Insights
- Drama, Comedy, and Thriller are most common genres
- Animation and Adventure show strong commercial performance
- Action films have grown significantly in recent decades

### Temporal Trends
- Steady increase in movie production over time
- Average budgets have increased significantly
- Ratings remain relatively stable across decades
- Summer and holiday releases perform better

### Director Impact
- Top directors show consistent patterns in ratings and profitability
- Director is a strong predictor for movie similarity

## 🛠️ Technical Details

### Optimization Highlights
- **Fast Rendering**: Conditional KDE for distributions (2-5 sec vs 28+ min)
- **Proper Director Extraction**: Parses crew JSON to find actual directors
- **Memory Efficient**: Optimized TF-IDF with 8000 features
- **Error Handling**: Robust JSON parsing with fallbacks

### Performance
- **Distribution Plots**: ~2-5 seconds (optimized)
- **TF-IDF Matrix**: ~3-5 seconds for 5000 movies
- **Cosine Similarity**: ~5-10 seconds
- **Recommendations**: <1 second per query

## 📚 Project Structure

```
tmdb-5k-movie/
├── tmdb-5k-movie-eda-recommendation-system-improved.ipynb  # Main notebook
├── README.md                                                # This file
├── requirements.txt                                         # Python dependencies
├── optimized_distribution_plot.py                          # Speed optimization fix
├── complete_feature_engineering_fix.py                     # Director extraction fix
└── data/                                                    # Data directory (not included)
    ├── tmdb_5000_movies.csv
    └── tmdb_5000_credits.csv
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Dataset**: The Movie Database (TMDB) via Kaggle
- **Recommendation Algorithm**: Content-Based Filtering with TF-IDF
- **Rating Formula**: IMDB Weighted Rating Formula

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

**⭐ If you found this project helpful, please consider giving it a star!**
