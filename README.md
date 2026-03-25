# NLU Assignment 2
## Word Embeddings and Character-Level Name Generation

---

## Overview
This repository contains the implementation of:
- Problem 1: Word2Vec training on IIT Jodhpur dataset
- Problem 2: Character-level name generation using RNN, BLSTM, and Attention

---

## Key Learnings
- Text preprocessing and corpus creation
- Word embedding techniques (CBOW and Skip-gram)
- Sequence modeling using RNN-based architectures
- Understanding and handling overfitting
- Use of attention mechanism for improved sequence generation

---

## Challenges Faced and Solutions

### 1. ModuleNotFoundError: gensim
Problem:
The gensim library was not installed, causing import errors.

Solution:
pip install gensim

---

### 2. NLTK Tokenizer Error (punkt_tab not found)
Problem:
Required NLTK tokenizer resources were missing.

Solution:
import nltk
nltk.download('punkt')
nltk.download('punkt_tab')

---

### 3. Attention Model Shape Mismatch
Problem:
Mismatch between model output and target dimensions during training.

Solution:
Modified the attention model to return sequence-level outputs instead of a single vector.

---

### 4. BLSTM Overfitting
Problem:
The BLSTM model achieved very low training loss but produced poor outputs.

Solution:
- Added dropout
- Increased number of layers to improve generalization

---

### 5. Poor Name Generation Quality
Problem:
Generated names were unrealistic or too short.

Solution:
- Controlled sampling during generation
- Started generation with uppercase characters
- Filtered short or invalid outputs

---

### 6. Confusion Between corpus.txt and TrainingNames.txt
Problem:
Misunderstanding between text corpus and name dataset.

Solution:
- corpus.txt is used in Problem 1 for Word2Vec
- TrainingNames.txt is used in Problem 2 for name generation

---

### 7. Multiple Attention Models Defined
Problem:
Two versions of the attention model were present, causing inconsistency.

Solution:
Removed the incorrect implementation and retained the sequence-based attention model.

---

## Issues During Evaluation (Important)

### 1. Missing Dependencies
If required libraries are not installed, the code will fail.

Required libraries:
- torch
- gensim
- nltk
- sklearn
- wordcloud

Install using:
pip install torch gensim nltk scikit-learn wordcloud

---

### 2. Missing NLTK Data
If tokenizer resources are not downloaded, preprocessing will fail.

Solution:
Run nltk.download('punkt') before execution.

---

### 3. File Path Errors
If dataset files are not in the correct directory, the code will not run.

Ensure:
- TrainingNames.txt is in the same folder as the notebook
- corpus.txt is correctly generated for Problem 1

---

### 4. GPU/CPU Differences
The code is written for CPU execution. Running on GPU without proper configuration may cause issues.

---

### 5. Random Outputs
Generated names may differ each run due to randomness in sampling.

This is expected behavior.

---

### 6. Long Training Time
Training Word2Vec or sequence models may take time depending on dataset size.

---

## Results Summary

| Model   | Performance |
|--------|------------|
| RNN    | Moderate   |
| BLSTM  | Overfitting|
| Attention | Best   |

---

## Final Submission

- corpus.txt (Problem 1)
- report.pdf

---

## Conclusion
This project demonstrates:
- Learning semantic relationships using Word2Vec
- Challenges in sequence modeling
- Importance of attention mechanisms for improving output quality

---

## Author
Divyansh Rawat
