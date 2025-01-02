# Wine Critic Recognizer

An NLP-based machine learning project to identify cross-category beverage reviewers using writing style analysis.

## Problem Statement

This project addresses the challenge of identifying beverage critics who review across multiple drink categories (wine, beer, and spirits) based on their writing style. Using natural language processing and machine learning techniques, the model analyzes review text to detect reviewers who write about multiple beverage types, particularly focusing on wine critics who also review beer.

## Project Structure

```
wine_critic_recognizer/
│
├── data/
│   ├── raw/         # Original datasets from Wine Enthusiast
│   └── modified/    # Processed datasets ready for analysis
│
└── src/
    ├── taster_identification_trained_with_wine_and_spirits_data.ipynb   # Jupyter notebook containing analysis and ML model
    └── scrapper.py         # Python script that gets all the data from the website
```

## Data Sources

The project utilizes three datasets from Wine Enthusiast:
- Wine reviews dataset (from Kaggle, scraped by zackthoutt)
- Beer reviews dataset (scraped using zackthoutt's scraper)
- Spirits reviews dataset (scraped using zackthoutt's scraper)

Each review includes:
- Country of origin
- Detailed tasting notes
- Designation (vineyard information)
- Numerical rating (1-100 scale)
- Price
- Geographic information (province, region)
- Variety/Type
- Producer information

## Methodology

1. **Data Collection**: Gathered reviews from Wine Enthusiast across three beverage categories
2. **Feature Engineering**: Extracted textual features from review descriptions
3. **Model Training**: Built a binary classifier using wine and spirits reviews
4. **Cross-Category Testing**: Evaluated the model on beer reviews to identify cross-category reviewers

## Key Findings

- Identified 19 wine tasters, 2 beer tasters, and 1 spirits taster in the dataset
- The 2 beer tasters also review wines, making them our target for identification
- Developed a binary classification model to distinguish between wine and spirits reviewers
- Successfully identified cross-category reviewers based on writing style

## Technologies Used

- Python
- Jupyter Notebook
- NLTK, Spacy, scikit-learn

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/vasileiosvyzas/wine_critic_recognizer.git
```

2. Run the Jupyter notebook:
```bash
jupyter notebook src/taster_identification_trained_with_wine_and_spirits_data.ipynb
```

## Acknowledgments

- Data source: Wine Enthusiast
- Original data scraping: zackthoutt on Kaggle
