# NLU Assignment 2 🚀
## Word Embeddings & Character-Level Name Generation

---

## 📌 Overview
This repository contains the implementation of:
- **Problem 1:** Word2Vec training on IIT Jodhpur dataset  
- **Problem 2:** Character-level name generation using RNN, BLSTM, and Attention  

---

## 🧠 Key Learnings
- Text preprocessing and corpus creation
- Word embedding techniques (CBOW & Skip-gram)
- Sequence modeling using RNNs
- Overfitting issues in deep learning
- Attention mechanism for improved sequence learning

---

## ⚠️ Challenges Faced & Solutions

### 🔴 1. ModuleNotFoundError: gensim
**Problem:**  
Gensim library not installed.

**Solution:**
```python
!pip install gensim
```

---

### 🔴 2. NLTK Tokenizer Error (punkt_tab not found)
**Problem:**  
NLTK tokenizer resources missing.

**Solution:**
```python
import nltk
nltk.download('punkt')
nltk.download('punkt_tab')
```

---

### 🔴 3. Attention Model Shape Mismatch
**Problem:**  
ValueError due to mismatch between model output and target shape.

**Solution:**  
Modified attention model to return sequence-level outputs.

---

### 🔴 4. BLSTM Overfitting
**Problem:**  
Very low loss but poor generated outputs.

**Solution:**
- Added dropout
- Increased number of layers

```python
num_layers = 2
dropout = 0.2
```

---

### 🔴 5. Poor Name Generation Quality
**Problem:**  
Generated names were unrealistic or too short.

**Solution:**
- Controlled sampling
- Started generation with uppercase characters
- Filtered short outputs

---

### 🔴 6. Confusion Between corpus.txt and TrainingNames.txt
**Problem:**  
Misunderstanding dataset roles.

**Solution:**
- corpus.txt → Problem 1 (text corpus)
- TrainingNames.txt → Problem 2 (names dataset)

---

### 🔴 7. Multiple Attention Models Defined
**Problem:**  
Duplicate attention implementations.

**Solution:**
Removed incorrect model and kept sequence-based attention model.

---

## 📊 Results Summary

| Model | Performance |
|------|------------|
| RNN | Moderate |
| BLSTM | Overfitting |
| Attention | Best |

---

## 📁 Final Submission

- corpus.txt → Cleaned dataset (Problem 1)
- report.pdf → Complete report

---

## 🚀 Conclusion
This project demonstrates:
- Effective use of Word2Vec for semantic learning  
- Challenges in sequence modeling  
- Importance of attention mechanisms  

---

## 👨‍💻 Author
Divyansh Rawat
