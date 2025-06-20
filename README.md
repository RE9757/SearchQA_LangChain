# 🔍 Search-Augmented Question Answering with LangChain

This project demonstrates a lightweight, search-augmented question answering system using the LangChain framework. It integrates SerpAPI (Bing search engine), web content extraction, semantic vector indexing (via FAISS), and a HuggingFace-powered LLM for end-to-end document retrieval and answer generation.

---

## 📌 Features

- 🔎 **Keyword-based web search** using [SerpAPI](https://serpapi.com/)
- 📰 **Article extraction** using `newspaper3k`
- 📄 **Text chunking and embedding** via `sentence-transformers`
- 🧠 **QA pipeline** built with `LangChain` + `FAISS` + HuggingFace LLM
- ✅ Minimal model used: `sshleifer/tiny-gpt2` for fast runtime and compatibility

---

## 🚀 How It Works

1. **Enter a search keyword**
2. **Use SerpAPI to fetch top URLs (Bing engine)**
3. **Extract full article content and save it to `result.txt`**
4. **Split the text into chunks and embed them into vectors**
5. **Use FAISS for similarity search**
6. **Answer a question using a HuggingFace LLM + LangChain RetrievalQA**

---

## 🔐 API Key Setup

To access search results, this notebook uses **SerpAPI**. You’ll need a free API key from [https://serpapi.com](https://serpapi.com):

1. **Sign up** at [serpapi.com](https://serpapi.com)
2. **Copy your API key** from your account dashboard
3. **Paste it when prompted in the notebook**

The key is securely provided via `input()` and stored in an environment variable:

```python
import os
os.environ["SERPAPI_API_KEY"] = input("Enter your SerpAPI key: ")
```
---

## Folder Structure
`SearchQA_LangChain.ipynb`: Main Colab notebook containing the full pipeline

`data/result.txt`: Output text file storing retrieved article content (auto-generated)

`README.md`: Project documentation

`requirements.txt`: (Optional) Dependency list for local installation

## Installation (for local use)
Install the required dependencies with:
```
pip install newspaper3k langchain faiss-cpu sentence-transformers transformers serpapi
```



