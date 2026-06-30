🚀 LLM Zoomcamp – Module 2: Vector Search

This repository contains my implementation and solutions for Module 2 (Vector Search) of the LLM Zoomcamp by DataTalksClub.

The goal of this module is to understand how modern semantic search systems work by building them step by step—from embeddings to hybrid search.

📚 Overview

In this project, we explore how to build and evaluate different search techniques using real course materials as the knowledge base.

We work with 72 markdown lesson pages from the LLM Zoomcamp repository (fixed at commit 8c1834d) and implement:

Text preprocessing and chunking
Vector embeddings using ONNX models
Pure vector search
Keyword (text) search
Hybrid search using Reciprocal Rank Fusion (RRF)
🧠 Key Concepts Learned
🔹 1. Embeddings

We convert text into dense vector representations using a lightweight ONNX embedding model.

🔹 2. Vector Search

We compute similarity between query and document vectors using dot product (cosine similarity since vectors are normalized).

🔹 3. Chunking

Long documents are split into smaller chunks to improve retrieval accuracy.

🔹 4. Keyword Search

Traditional text-based search using exact token matching.

🔹 5. Hybrid Search (RRF)

We combine vector and keyword search results using Reciprocal Rank Fusion (RRF) to improve relevance.

⚙️ Tech Stack
Python 
NumPy
ONNX Runtime
Tokenizers
minsearch
gitsource (for loading course data)
HuggingFace Hub

📂 Project Structure

llm-zoomcamp-hw2/

│
├── download.py 

├── embedder.py          

├── hw_2.ipynb   

├── ingest.py/      

└── README.md


🔍 What This Project Covers
✔️ Q1 – Query Embedding

Generate embeddings for a natural language query.

✔️ Q2 – Cosine Similarity

Measure similarity between query and document embeddings.

✔️ Q3 – Chunked Vector Search

Improve retrieval by splitting documents into chunks.

✔️ Q4 – Vector Search with minsearch

Use a vector index for efficient similarity search.

✔️ Q5 – Keyword vs Vector Search

Compare semantic vs lexical retrieval methods.

✔️ Q6 – Hybrid Search (RRF)

Combine both approaches for better ranking results.

🚀 How to Run
1. Clone the repository
git clone https://github.com/<your-username>/llm-zoomcamp-hw2.git
cd llm-zoomcamp-hw2
2. Create environment
uv init --no-workspace
uv add onnxruntime tokenizers numpy tqdm minsearch gitsource
uv add --dev huggingface-hub jupyter
3. Download embedding model
python download.py
4. Run notebook
jupyter notebook



📊 Results

This project demonstrates how:

Semantic search improves retrieval over keyword matching
Chunking significantly boosts embedding quality
Hybrid search (RRF) combines strengths of both methods



🙌 Acknowledgements
DataTalksClub for the LLM Zoomcamp
Alexey Grigorev for the course design and guidance
📌 License

This project is for educational purposes as part of the LLM Zoomcamp. 
