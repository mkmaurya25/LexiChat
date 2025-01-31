## 🚀 Overview
LexiChat is an AI-powered chatbot that allows users to **upload PDFs and ask questions** about their content. It utilizes **LangChain, FAISS, Hugging Face embeddings, and Groq’s LLMs** to provide intelligent responses based on document content.

## 🛠️ Tech Stack

| Component          | Technology Used |
|--------------------|----------------|
| **Frontend**      | Streamlit      |
| **LLM Provider**  | Groq (Gemma-2B) |
| **Embeddings**    | Hugging Face (`all-MiniLM-L6-v2`) |
| **Vector Storage**| FAISS          |
| **File Processing** | PyPDF          |
| **Backend**       | Python (LangChain) |

## 📌 Features
✅ **Upload PDFs** – Supports multi-page PDFs  
✅ **Text Extraction** – Extracts and preprocesses text  
✅ **Vector Storage** – Uses FAISS for efficient search  
✅ **AI-powered Q&A** – Uses Groq's LLM for responses  
✅ **Persistent Cache** – Stores embeddings to reduce computation  

## 🏗️ System Architecture
```
+-------------+        +------------+        +-------------+        +-----------+
|  Streamlit  | -----> |  PyPDF     | -----> | Text Splitter| -----> | FAISS     |
| (Frontend)  |        | (Extracts  |        | (LangChain)  |        | (Vector DB)|
+-------------+        |   Text)    |        +-------------+        +-----------+
        |                    |                    |
        v                    v                    v
+------------------------------------+         +----------------+
| Hugging Face Embeddings (MiniLM)  | ----->  | Groq LLM (Gemma) |
+------------------------------------+         +----------------+
                   |
                   v
              +---------------------+
              |  QA Chain (LangChain)|
              +---------------------+
```

## 📥 Installation Guide

### 📌 Prerequisites
- Python 3.8+
- pip & virtual environment  
- A **Groq API Key** ([Get one here](https://groq.com))  

### 🔹 Steps to Install & Run

1️⃣ **Clone the Repository**  
```bash
git clone https://github.com/your-repo/pdfchat-ai.git
cd pdfchat-ai
```

2️⃣ **Create a Virtual Environment**  
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3️⃣ **Install Dependencies**  
```bash
pip install -r requirements.txt
```

4️⃣ **Run the Streamlit App**  
```bash
streamlit run app.py
```

5️⃣ **Upload a PDF and Ask Questions!** 🎉  

## ⚙️ Configuration

### Setting the API Key

PDFChatAI requires a **Groq API Key** to interact with the LLM. You can set it in two ways:

#### 1️⃣ Using Environment Variables
```bash
export GROQ_API_KEY=your_api_key_here  # Linux/macOS
set GROQ_API_KEY=your_api_key_here  # Windows
```

#### 2️⃣ Using `.env` File
Create a `.env` file in the root directory and add:
```
GROQ_API_KEY=your_api_key_here
```

## 🤝 Contributing
We welcome contributions! 🎉  

### 📝 How to Contribute?
1. **Fork the repository**  
2. **Create a new branch**  
   ```bash
   git checkout -b feature-branch
   ```
3. **Make changes and commit**  
   ```bash
   git commit -m "Add new feature"
   ```
4. **Push changes and create a PR**  
   ```bash
   git push origin feature-branch
   ```
5. **Submit a Pull Request** 🚀  

## 📜 License
This project is licensed under the **MIT License**. See the [LICENSE](https://github.com/your-repo/pdfchat-ai/blob/main/LICENSE) file for details.  

## 🔮 Future Enhancements
🔹 Support for multiple PDFs at once  
🔹 Multi-language support  
🔹 More LLM integrations (OpenAI, Mistral, etc.)  
🔹 UI enhancements  

---
💡 **Got any suggestions or issues?** Feel free to open an [issue](https://github.com/your-repo/pdfchat-ai/issues)! 🚀

