# Information Summarizer: Powered by Wikipedia

> TL;DR: This project fetches content from Wikipedia based on a keyword and summarizes it using both extractive (word frequency) and abstractive (deep learning) techniques. Ideal for users looking for quick, accurate information on any topic.

---

## Overview

Summarized data can help users understand lengthy content at a glance. This project leverages **Wikipedia** as the primary data source and provides a shortened, readable version of the article using:

- **Extractive Summarization** — Word frequency-based summarization
- **Abstractive Summarization** — Transformer models (PEGASUS, BART)

---

## How It Works

### 1. Data Collection
- Wikipedia content is fetched using the `wikipedia` Python library.
- Users input a keyword; the corresponding article is retrieved.

### 2. Preprocessing
- Removes citations, references, and special characters using regex.
- Cleans and structures the article for processing.

### 3. Extractive Summarization
- Tokenizes the article and calculates word frequency.
- Scores sentences based on the frequency of significant words.
- Top-scoring sentences are selected to generate the summary.

### 4. Abstractive Summarization
Two pretrained transformer models are used:
- **PEGASUS** (by Google): Designed for abstractive summarization using a sequence-to-sequence architecture.
- **BART** (by Facebook): Fine-tuned on the [xsum](https://huggingface.co/datasets/xsum) dataset from Hugging Face.

The models paraphrase and condense content based on contextual understanding.

---

## Analysis & Visualization

- **Pie Charts** — Summary size comparison
- **Word Clouds** — Frequent word visualization in original, extractive, and abstractive summaries
- **Venn Diagrams** — Common words across summary types
- **Bar Charts** — Bigram & trigram frequency analysis
- **Top 50 Words** — Most common terms across all summaries

---

## Results

- Extractive summaries are sentence-based and pull directly from the article.
- Abstractive summaries provide more natural and concise results, often outperforming extractive methods in readability.
- PEGASUS and BART models show promising results in capturing the core idea of the content.

---

## Conclusion

- **Extractive summarization** is simple but can miss context.
- **Abstractive summarization** offers more flexibility and understanding, making it a better long-term solution—given proper data and training.

---

## Tech Stack

- Python
- Wikipedia API
- NLTK, spaCy, re
- Transformers (Hugging Face): BART, PEGASUS
- Matplotlib & WordCloud for visualization

---

## References

- [Text Summarization in Python – Great Learning](https://www.mygreatlearning.com/blog/text-summarization-in-python/)
- [Abstractive Summarization using Deep Learning – Section.io](https://www.section.io/engineering-education/abstractive-summarization-using-deep-learning/)
- [Hugging Face: Pegasus-xsum](https://huggingface.co/google/pegasus-xsum)
- [Matplotlib Documentation](https://matplotlib.org/)

---
