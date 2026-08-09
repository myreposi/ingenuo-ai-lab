# 01-Foundations: Transformers

## 1. What is the Transformer Architecture?
Introduced in the seminal 2017 paper *"Attention Is All You Need"*, the Transformer is a deep learning architecture that completely abandoned recurrent loops (RNNs) and convolutions (CNNs). Instead, it relies entirely on mathematical attention mechanisms to process data sequences in parallel, making it highly scalable and the foundational backbone of all modern Large Language Models.

## 2. Core Breakthrough Concepts

### A. Self-Attention Mechanism
Allows the model to evaluate the relationship between all words in a sentence simultaneously, regardless of their physical distance from one another.
* **Queries (Q)**: What the current word is looking for.
* **Keys (K)**: What relevance characteristics other words in the sequence hold.
* **Values (V)**: The actual content payload extracted once a Query matches a Key.
* **Formula**: $\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$

### B. Multi-Head Attention
Instead of performing attention once, the network splits Q, K, and V into multiple subsets ("heads"). This allows the model to simultaneously track different types of contextual relationships (e.g., matching a pronoun to its subject while also matching a verb to its object).

### C. Positional Encoding
Because Transformers process all words in parallel, they naturally lack an inherent sense of word order. Positional encodings add static mathematical vectors to word embeddings to preserve sequential order information without using sequential processing loops.

## 3. Structural Design Blueprint

### A. The Encoder Block
Processes the input sequence to build a rich, contextual representation of the entire text string.
* *Components*: Multi-Head Self-Attention, Layer Normalization, Residual Connections, Feed-Forward Networks.
* *Example Models*: BERT (Bidirectional Encoder Representations from Transformers).

### B. The Decoder Block
Generates output sequences autoregressively (one token at a time), referencing both its past generated tokens and the representations created by the Encoder.
* *Components*: Masked Multi-Head Self-Attention (prevents looking at future tokens), Encoder-Decoder Attention, Feed-Forward Networks.
* *Example Models*: GPT series, Llama series.
