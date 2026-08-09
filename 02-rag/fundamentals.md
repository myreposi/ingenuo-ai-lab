# 02-RAG: Fundamentals

## 1. What is Retrieval-Augmented Generation?
Retrieval-Augmented Generation (RAG) is an architectural framework that optimizes Large Language Model outputs by querying an authoritative, external knowledge base before generating a response. Instead of relying solely on the static data a model learned during training, RAG injects dynamic, real-time context directly into the prompt payload.

## 2. Core Operational Flow
A standard RAG pipeline follows a clear 3-step sequence:
1. **Ingestion & Indexing**: Document sources are broken down into small, digestible chunks, converted into vector math format using embedding models, and saved in a vector repository.
2. **Retrieval**: When a human types a prompt, the system searches the vector repository to extract the most relevant document chunks based on mathematical similarity.
3. **Generation**: The extracted document text chunks and the user's original prompt are packed together inside a clean prompt template and sent to the LLM to write an accurate answer.

## 3. Critical Advantages of RAG
* **Mitigates Hallucinations**: Grounds the model's logic in verifiable, explicit document facts rather than statistical guesswork.
* **Low-Cost Knowledge Updates**: Avoids the massive compute expense, time commitments, and engineering overhead of fine-tuning or re-training base models.
* **Access Control & Permissions**: Allows system engineers to easily add security layers, ensuring users only retrieve documents they are explicitly authorized to view.
* **Data Provenance**: Provides a built-in citation trail by pointing directly back to the exact source documents used to build the answer.
