# 02-RAG: Embeddings

## 1. What are Vector Embeddings?
Vector embeddings are dense numerical arrays that translate human language, images, or tokens into coordinates inside a high-dimensional mathematical space. The core principle of an embedding model is semantic proximity: words or phrases with similar conceptual meanings are mapped closely together in this geometric layout.

## 2. Mathematical Similarity Metrics
Once text is converted into multi-dimensional vectors, databases use geometry to determine how closely related two chunks of information are:

* **Cosine Similarity**: Measures the exact angle between two directional vectors, completely ignoring differences in document length. It is the most common metric used in semantic search.
* **Euclidean Distance (L2)**: Measures the straight-line distance between two coordinates in space. Smaller values signify higher contextual similarity.
* **Dot Product**: Multiplies vector magnitudes along with their directional alignment. It is highly efficient but heavily influenced by document length.

## 3. Data Chunking Strategies
Before text can be turned into an embedding, it must be broken down into manageable segments. Choosing a strategy is critical to keeping the right balance of context and accuracy:

* **Fixed-Size Chunking**: Chops text at a strict, pre-set character or token limit (e.g., exactly 500 tokens). It is fast to execute but often breaks apart sentences mid-thought.
* **Overlapping Chunks**: Incorporates a small overlap buffer (e.g., 50 tokens) between consecutive chunks. This prevents critical context from getting sliced in half at the boundaries.
* **Semantic/Document Chunking**: Uses natural structural boundaries—like paragraphs, markdown headers, or markdown tables—to keep related thoughts intact.
