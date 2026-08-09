# 02-RAG: Retrieval

## 1. What is Retrieval in RAG?
Retrieval is the algorithmic process of scanning a knowledge database to extract the most relevant snippets of information based on a user's prompt. The quality of an LLM's response in a RAG pipeline depends entirely on the accuracy and relevance of the text pulled during this stage.

## 2. Core Retrieval Methodologies

### A. Dense Retrieval (Semantic Search)
Uses machine learning models to search by conceptual meaning rather than exact word matches.
* **Mechanism**: Converts queries and documents into mathematical vectors to calculate spatial proximity.
* **Strength**: Captures synonyms, intent, and contextual ideas perfectly.

### B. Sparse Retrieval (Keyword Search)
Matches exact characters, phrases, or word frequencies across a document index.
* **Mechanism**: Relies on classical statistical frequency mapping algorithms.
* **Algorithms**: BM25, TF-IDF.
* **Strength**: Excellent for finding specific serial numbers, unique product IDs, or precise names.

### C. Hybrid Retrieval
Combines Dense Semantic Search and Sparse Keyword Search into a unified retrieval step. Outputs from both methods are scored and merged using algorithms like Reciprocal Rank Fusion (RRF) to get the best of both worlds.

## 3. Advanced Optimization Techniques
* **Re-ranking**: Running a secondary, highly precise cross-encoder model over the top 20 or 30 retrieved chunks to re-order them by exact relevance before sending them to the LLM.
* **Query Expansion**: Using a smaller LLM to rewrite a user's short prompt into multiple variations or hypothetical answers (HyDE) to improve database search hit rates.
* **Metadata Filtering**: Hard-filtering search boundaries by specific attributes like date ranges, authors, or categories before executing a mathematical vector search.
  
