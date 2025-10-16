# LLM Book Recommender 📚🤖

A lightweight book recommendation system powered by large language models (LLMs). This project aims to suggest books based on input prompts, sentiment, and semantic similarity, wrapped in an interactive Gradio interface.

---

## Table of Contents

- [Features](#features)  
- [Project Structure](#project-structure)  
- [Installation](#installation)  
- [Usage](#usage)  
- [How It Works](#how-it-works)  
- [Dataset](#dataset)  
- [Future Work](#future-work) 

---

## Features

- Explore book dataset enriched with categories and emotional labels  
- Vector search / semantic similarity based recommendations  
- Sentiment & text classification analysis  
- Web interface using Gradio for user interaction  
- Exploratory data notebooks to understand dataset and pipeline

---

## Project Structure

``text
.
├── books_cleaned.csv
├── books_with_categories.csv
├── books_with_emotions.csv
├── data_exploration.ipynb
├── gradio-dashboard.py
├── sentiment_analysis.ipynb
├── text_classification.ipynb
└── vector_search.ipynb

---

## Installation

Clone the repository:
git clone https://github.com/Ruchir0403/llm_book_recommender.git
cd llm_book_recommender

Create & activate a virtual environment (optional but recommended):
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

Install dependencies:
pip install -r requirements.txt

## Usage

To start the web-based interface:
python gradio-dashboard.py

Then open the local URL (usually http://127.0.0.1:7860) in your browser to interact with the recommender.
You can also run individual notebooks (e.g. vector_search.ipynb) to explore embedding, similarity, classification, or data processing steps.

## How It Works

Data Preparation & Augmentation
Books are cleaned and enriched with categories and emotion labels to provide richer context.

Embedding & Vector Search
Each book’s descriptive text is encoded into embeddings (via a sentence transformer or similar). A user prompt or query is also embedded and matched to nearest book embeddings to recommend closest matches.

Sentiment / Text Classification
Optionally, the system may use sentiment classification or topic classification (from trained models) as additional features to filter or reorder recommendations.

Gradio Interface
Users can input text prompts (e.g. “I like science fiction about space & exploration”) and get book suggestions in real time.

## Dataset

The repository includes three main CSV files:
books_cleaned.csv
books_with_categories.csv
books_with_emotions.csv

You can inspect and explore them using the provided notebooks. If you want to expand the dataset, ensure consistency in your preprocessing pipeline (e.g. tokenization, normalization).

## Future Work

Improve recommendation by blending collaborative filtering + content-based methods
Add user interaction / feedback loop to refine suggestions
Extend the UI (e.g. user profiles, saved lists)
Support multilingual book datasets
Deploy as a web app (e.g. via Streamlit, FastAPI + frontend)
Optimize model speed & embedding retrieval (e.g. FAISS, ANN search)
