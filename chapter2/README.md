# Chapter 2 - Working with Text Data

In Chapter 2, I focus on processing and preparing text data for the language model. This chapter follows the tutorial by Sebastian Raschka, where we work through various stages of transforming raw text into a format suitable for training a large language model (LLM).

The dataset used in this chapter is `the_verdict.txt`, which is a small text file containing some example sentences. The steps cover everything from tokenization to creating token embeddings.

---

## 🧑‍💻 Steps Covered in This Chapter

### 2.1 Setting Up MacBook GPU
I configured my MacBook to use its GPU for computations to accelerate the model training process. This setup ensures faster training times and better utilization of hardware resources.

- Installed the necessary libraries and drivers.
- Set up the environment to enable GPU usage.

### 2.2 Tokenizing Text
The first step in processing text is to tokenize it — splitting the raw text into smaller units (tokens). These tokens can be words, subwords, or characters.

- Used basic tokenization techniques.
- Implemented custom functions for handling punctuation and splitting.

### 2.3 Converting Tokens into Token IDs
After tokenizing the text, I converted each token into a corresponding token ID. These IDs represent the vocabulary used in the model.

- Mapped tokens to token IDs based on a predefined vocabulary.
- Added handling for unknown tokens.

### 2.4 Adding Special Tokens
Special tokens are added to the vocabulary for various tasks (e.g., beginning-of-sequence, end-of-sequence, padding).

- Added tokens like `[CLS]` (start), `[SEP]` (end), and `[PAD]` (padding) to the dataset.

### 2.5 Byte Pair Encoding (BPE)
Byte Pair Encoding (BPE) is a subword tokenization technique that is often used in NLP models to handle rare words. This technique reduces the vocabulary size and helps in efficient handling of out-of-vocabulary tokens.

- Implemented BPE to break down words into subword units.
- Trained BPE on the dataset to create a new vocabulary.

### 2.6 Data Sampling with Sliding Window
To prepare the data for training, I implemented a sliding window technique. This technique breaks the text into smaller, overlapping sequences to ensure the model can learn from multiple contexts.

- Used a window size and stride to sample text from the dataset.
- Generated training examples that consist of sequential tokens.

### 2.7 Creating Token Embeddings
Token embeddings are continuous vector representations of tokens. These embeddings allow the model to learn semantic meaning and relationships between tokens.

- Used random initialization for token embeddings.
- Set up a lookup table to map token IDs to their respective embeddings.

### 2.8 Encoding Word Position
Since transformers are not inherently aware of the order of tokens, position encodings are added to the embeddings to provide sequence order information.

- Added positional encodings to the token embeddings to help the model learn token positions within a sequence.

---
