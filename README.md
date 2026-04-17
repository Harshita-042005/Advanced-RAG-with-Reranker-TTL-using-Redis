# Advanced RAG with Reranker & TTL Cache using Redis

## 📌 Project Overview

This project is an Advanced Retrieval-Augmented Generation (RAG) application built using Python, LangChain, Redis, FAISS, HuggingFace, and Streamlit. It retrieves relevant information from a knowledge source, reranks results using a Cross-Encoder model, and generates accurate answers using a local LLM (TinyLlama).

The system also integrates Redis Semantic Cache with TTL (Time-To-Live) to improve performance by reducing repeated LLM calls and speeding up responses.

---

## 🚀 Features

* Semantic document retrieval using FAISS
* Intelligent reranking using Cross-Encoder
* Fast response with Redis Semantic Cache
* TTL support for automatic cache expiration
* Local LLM answer generation using TinyLlama
* Interactive Streamlit web interface
* Wikipedia-based dynamic knowledge source

---

## 🛠️ Tech Stack

* Python
* Streamlit
* LangChain
* Redis
* FAISS
* HuggingFace Embeddings
* Sentence Transformers
* TinyLlama (Ollama)

---

## 📂 Project Structure

```
Advanced-RAG-Redis/
│── Reranker_web2.py
│── requirements.txt
│── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/Advanced-RAG-Redis.git
cd Advanced-RAG-Redis
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Start Redis (Docker)

```bash
docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```

### 4️⃣ Install Ollama & Pull TinyLlama

```bash
ollama pull tinyllama
```

### 5️⃣ Run the Application

```bash
streamlit run Reranker_web.py
```

---

## 💡 How It Works

1. User enters a query
2. FAISS retrieves top relevant document chunks
3. Cross-Encoder reranks the retrieved results
4. Top-ranked context is selected
5. TinyLlama generates the final answer
6. Redis caches responses with TTL for faster future queries

---

## 🎯 Use Cases

* Intelligent Question Answering Systems
* Research Assistants
* Document-based Chatbots
* Knowledge Retrieval Applications

---

## 📢 Future Improvements

* Add support for multiple document sources
* Improve UI/UX design
* Deploy as a cloud-based application

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit a pull request.

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 🙌 Acknowledgements

* LangChain
* HuggingFace
* FAISS
* Redis
* Ollama
