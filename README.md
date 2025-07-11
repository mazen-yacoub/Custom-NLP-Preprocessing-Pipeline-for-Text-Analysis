# Custom-NLP-Preprocessing-Pipeline-for-Text-Analysis
A complete Natural Language Processing (NLP) pipeline that cleans, tokenizes, normalizes, and analyzes text from two contrasting topics in the 20 Newsgroups dataset.

# NLP Text Cleaning Pipeline: sci.space vs comp.graphics

This project implements a custom text preprocessing pipeline to clean and analyze raw text data from the [20 Newsgroups](https://scikit-learn.org/0.19/datasets/twenty_newsgroups.html) dataset using two contrasting categories:

- `sci.space`
- `comp.graphics`

## Objective

To evaluate how preprocessing transforms noisy, unstructured text into clean and meaningful input for analysis or machine learning — **even without training a model**.

---

## Preprocessing Pipeline

The custom pipeline includes:

1. **Regex Cleaning**  
   Remove punctuation, numbers, and symbols using `re`.

2. **Tokenization**  
   Split documents into words using `nltk.word_tokenize()`.

3. **Lowercasing**  
   Convert all tokens to lowercase.

4. **Stopword Removal**  
   Remove common English stopwords using NLTK.

5. **Lemmatization**  
   Normalize words to their base form using `WordNetLemmatizer`.

### also there are notebook for: Investigate How Preprocessing Steps Change the Vocabulary and Semantics
**Description:**
   This notebook explores the impact of common NLP preprocessing steps (tokenization, stopword removal, stemming)
   on a text dataset. We analyze how each step affects vocabulary size, document length, and word frequency
   using a subset (100 documents) from the "sci.space" category in the 20 Newsgroups dataset.
** Versions **:
- Version A: Raw text (no preprocessing)
- Version B: Regex cleaning + tokenization
- Version C: Version B + lowercasing + stopword removal
- Version D: Version C + stemming

---

## Analysis

After cleaning and preprocessing, the project:

- Extracts the **Top 10 most frequent words** for each category.
- Compares vocabularies between sci.space and comp.graphics.
- Identifies **unique vs. shared words** in both topics.

---

## Folder Structure

```bash

## install Requirements
`pip install nltk scikit-learn pandas matplotlib seaborn`

## Download NLTK Resources
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('omw-1.4')
