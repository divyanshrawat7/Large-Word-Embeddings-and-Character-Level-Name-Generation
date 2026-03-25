# NLU Assignment 2
## Word Embeddings and Character-Level Name Generation

---

## Overview
This repository contains implementations for:
- Problem 1: Word2Vec on IIT Jodhpur dataset
- Problem 2: Character-level name generation using RNN, BLSTM, and Attention

---

## Requirements

Install the following libraries before running the code:

pip install torch gensim nltk scikit-learn wordcloud

---

## Setup

1. Clone the repository or download the files.
2. Place all files in a single working directory.

---

## Problem 1: Word Embeddings

### Steps to Run

1. Open the Problem 1 notebook.
2. Ensure your raw dataset is available.
3. Run all cells sequentially:
   - Data preprocessing
   - Tokenization
   - Word2Vec training (CBOW and Skip-gram)
   - Semantic analysis
   - Visualization

4. Generate the cleaned corpus file by running:

   with open("corpus.txt", "w") as f:
       f.write(" ".join(token_stream))

5. Ensure the following outputs are generated:
   - Word cloud image
   - PCA/t-SNE visualization
   - corpus.txt

---

## Problem 2: Name Generation

### Steps to Run

1. Ensure the file `TrainingNames.txt` is present in the same directory.
2. Open the Problem 2 notebook.
3. Run all cells sequentially:
   - Load dataset
   - Build character vocabulary
   - Train RNN model
   - Train BLSTM model
   - Train Attention model
   - Generate names
   - Evaluate using novelty and diversity

4. Observe generated outputs for each model.

---

## Output Files

After execution, ensure you have:
- corpus.txt (from Problem 1)
- Generated visualizations (Problem 1)
- Generated names and evaluation results (Problem 2)

---

## Submission

Final submission should include:
- corpus.txt
- report.pdf

---
