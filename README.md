# From Captions to Cart: A Cross-Domain Recommendation System

## Project Overview

This project implements a cross-domain recommendation system that leverages Instagram post content to suggest relevant Amazon products. By utilizing TF-IDF and cosine similarity, the system bridges the gap between social media engagement and e-commerce platforms, offering personalized product recommendations based on user-generated content.

## Features

- **Cross-Domain Integration**: Combines Instagram post data with Amazon product reviews for unique recommendations.
- **TF-IDF Vectorization**: Transforms textual data from both domains into feature vectors.
- **Cosine Similarity Matching**: Ranks product relevance based on content similarity.
- **Scalable Architecture**: Designed to handle large datasets efficiently.

## Dataset

The project utilizes two main datasets:

1. **Instagram Dataset**: 119 posts with engagement metrics and textual content (captions and hashtags).
2. **Amazon Reviews Dataset**: Over 700,000 product reviews, including ratings and textual feedback.

## Model Description

The recommendation system employs a content-based approach using TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity:

1. Text data from Instagram posts (captions and hashtags) and Amazon reviews are preprocessed and vectorized using TF-IDF.
2. Cosine similarity is calculated between Instagram post vectors and Amazon product review vectors.
3. Products are ranked based on similarity scores, with the most relevant items recommended.

## Installation

```bash
git clone https://github.com/fourierblob/Captions-To-Cart.git
cd Captions-To-Cart
pip install -r requirements.txt
```

## Usage

To run the recommendation system:

```
Run the ipynb file
```

## Results

The model demonstrates varying effectiveness in matching Instagram posts to Amazon products:

- Mean Similarity Score: 0.0027
- Median Similarity Score: 0.0000
- Maximum Similarity Score: 1.0000

While some recommendations show high relevance, the low mean and median scores indicate challenges in consistent content alignment.

## Limitations and Future Work

- **Context Insensitivity**: The model struggles with ambiguous terms and lacks semantic understanding.
- **Noisy Data Handling**: Generic hashtags can reduce recommendation precision.
- **Feature Simplicity**: TF-IDF doesn't capture complex semantic relationships.

Future improvements could include:
- Implementing advanced NLP techniques like BERT or Word2Vec for better semantic understanding.
- Exploring graph-based methods to capture complex user-product relationships.
- Incorporating collaborative filtering techniques when user-product interaction data becomes available.
