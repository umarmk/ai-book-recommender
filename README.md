# LLM Book Recommender

A semantic book recommendation system designed to find books based on natural language queries, categories, and emotional tones.
<img width="1916" height="902" alt="image" src="https://github.com/user-attachments/assets/2c04e1b4-668a-4d69-9379-a6c783cdbc6e" />


## Description

This project utilizes a large language model (LLM) to bridge the gap between human intent and book metadata. Unlike traditional keyword search, this system understands the semantic meaning of your query (e.g., "a heartwarming story about friendship") to provide relevant recommendations.

**Key Features:**

- **Semantic Search:** Finds books based on the content of their descriptions rather than just title matches.
- **Emotion Analysis:** Filters books by emotional tone (Happy, Surprising, Angry, Suspenseful, Sad).
- **Category Filtering:** Refine results by genre or category.
- **Interactive Dashboard:** Built with Gradio for a user-friendly web interface.

## Heavy Compute & Data Processing

The recommendations are powered by enriched metadata generated through heavy computational tasks. The following notebooks were executed using **Google Colab's T4 GPU runtime**:

- `text_classification.ipynb`: Categorizes books into broad genres (Fiction, History, Biography, etc.) based on their descriptions.
- `sentiment_analysis.ipynb`: Analyzes the emotional tone of book descriptions to enable mood-based filtering.

## Dataset

The underlying dataset consists of 7,000 books, including metadata like titles, authors, descriptions, and thumbnails.

**Source:** [7k Books with Metadata (Kaggle)](https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata)

## Usage

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
2. **Environment Setup:**
   Create a `.env` file and add your OpenAI API key and Huggingface Token:
   ```env
   OPENAI_API_KEY=your_api_key_here
   HUGGINGFACEHUB_API_TOKEN=your_huggingface_token_here
   ```
3. **Run the Dashboard:**
   ```bash
   python gradio_dashboard.py
   ```
