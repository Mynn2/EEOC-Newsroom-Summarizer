# EEOC-Newsroom-Summarizer

This project automatically scrapes and summarizes the latest news releases from the U.S. Equal Employment Opportunity Commission (EEOC) newsroom.  
It uses Python web scraping and a pre-trained summarization model to generate concise summaries for each article and saves the results as CSV and HTML files.


## Overview
The goal of this project is to build an automated system that:
- Collects the latest EEOC newsroom articles
- Extracts and cleans the main article content
- Summarizes text using a pre-trained BART model
- Saves results in CSV and HTML formats for easy viewing
- Can be extended to publish summaries automatically to WordPress or social platforms in the future


## Features
- Automatic crawling of EEOC newsroom pages  
- Pagination support (e.g., `?page=0` to `?page=5`)  
- Filters out non-article or disallowed URLs according to `robots.txt`  
- Extracts article title and body text from multiple HTML structures  
- Summarizes each article using the `facebook/bart-large-cnn` model  
- Exports both CSV and HTML summary files  
- Includes a debug mode for quick testing (3 articles, short summaries)  
- Designed for future integration with WordPress and short-form video generation  


## Tech Stack
- **Language:** Python 3.10+  
- **Libraries:** `transformers`, `torch`, `requests`, `beautifulsoup4`, `pandas`  
- **Model:** `facebook/bart-large-cnn` (Hugging Face pre-trained summarizer)  
- **Environment:** Google Colab or VS Code  
