# 01-Foundations: Large Language Models (LLMs)

## 1. What is an LLM?
A Large Language Model (LLM) is an advanced deep learning model trained on massive text corpora to understand, process, and generate human-like language. At their core, LLMs are statistical next-token predictors scaled up to billions of parameters, allowing complex linguistic patterns, logic, and world knowledge to emerge during training.

## 2. Training Paradigms & Lifecycle

### A. Pre-training (Unsupervised / Self-Supervised)
The model reviews massive, unlabelled datasets (web crawls, books, code repositories) to learn raw language structure.
* **Objective**: Predict the next hidden token in a sequence given the previous context window.
* **Result**: A "Base Model" that understands grammar and facts but behaves like an autocomplete engine instead of an assistant.

### B. Instruction Fine-Tuning (SFT)
The base model is trained further on high-quality, curated datasets containing explicit human prompts and correct response paths.
* **Objective**: Transform raw next-token prediction into an interactive, helpful conversational assistant.

### C. Alignment (RLHF / RLAIF / DPO)
Methods used to align model behaviors with human values regarding safety, truthfulness, and utility.
* **RLHF**: Reinforcement Learning from Human Feedback (ranking model answers to train a reward model).
* **DPO**: Direct Preference Optimization (skips the reward model to optimize directly on human preference pairs).

## 3. Core Architectural Concepts

### A. Tokenization
The process of breaking raw text strings down into smaller sub-word units called tokens. Models do not read letters; they process arrays of integers representing token dictionary IDs.
* *Examples*: Byte-Pair Encoding (BPE), WordPiece.

### B. Context Window
The strict maximum limit of tokens a model can accept and process simultaneously in its memory buffer during a single inference pass.

### C. Scaling Laws
Empirical observations demonstrating that an LLM's cross-entropy loss drops predictably as compute budget, dataset size, and total parameter counts scale up in unison.
