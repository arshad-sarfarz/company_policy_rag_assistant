# 🧠 Company Policy RAG Assistant

The **Company Policy RAG (Retrieval-Augmented Generation) Assistant** is an intelligent AI-powered tool designed to help employees quickly find information from company policies across multiple domains such as HR, IT, Security, and Operations. It uses a Retrieval-Augmented Generation pipeline to deliver precise, contextually relevant answers drawn directly from approved policy documents.

---

## 🚀 Features

* **Policy Search:** Quickly retrieve relevant sections from corporate policy documents.
* **Multi-Domain Coverage:** Supports HR, IT, Security, Travel, Diversity, and more.
* **Contextual Q&A:** Uses RAG to ensure every answer is grounded in actual company content.

---

## 🏗️ Project Structure

```
company_policy_rag_assistant/
│
├── data/                     # Folder containing policy documents (.txt)
├── src/                      # Core application
│   ├── app.py                # Entry point for running the RAG assistant
│   ├── vectordb.py           # Document retrieval logic
├── .env.example              # Environment template
├── requirements.txt          # Python dependencies
├── README.md                 # Project overview (this file)
└── LICENSE                   # License information (MIT license)
```

---

## ⚙️ Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-org>/company_policy_rag_assistant.git
   cd company_policy_rag_assistant
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure your API key:**

   ```bash
   # Create environment file (choose the method that works on your system)
   cp .env.example .env    # Linux/Mac
   copy .env.example .env  # Windows
   ```

   Edit `.env` and add your API key:

   ```
   OPENAI_API_KEY=your_key_here
   # OR
   GROQ_API_KEY=your_key_here  
   # OR
   GOOGLE_API_KEY=your_key_here
   ```

4. **Run the application**

   ```bash
   python src/app.py
   ```

---

## 🧩 How It Works

1. **Document Ingestion**
   All policy files in the `data/` folder are parsed, cleaned, and embedded into a vector database (ChromaDB).

2. **Retrieval**
   When a user asks a question, the system retrieves the most relevant document chunks using semantic similarity search.

3. **Augmented Generation**
   The context retrieved from policies is passed into a Large Language Model (LLM) like GPT-4 or similar for grounded answer generation.

4. **Response Delivery**
   The assistant responds with an answer.

---

## 🧠 Example Queries

| Example Question                       | Example Output                                                                                                            |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| “What is our hybrid work policy?”      | The hybrid work policy allows employees to work remotely up to 3 days a week, subject to manager approval.                |
| “How do I claim travel reimbursement?” | Employees must submit receipts through the Expense Portal within 14 days. Approvals are routed automatically to managers. |

---

## 📊 Supported Policy Areas

* 🏠 **Remote & Hybrid Work Policy**
* 🧳 **Expense & Travel Policy**
* 💻 **IT Security & Data Protection**
* 🧍‍♂️ **Employee Code of Conduct**
* 📈 **Performance & Career Development**
* 🏖️ **Time Off & Leave Policy**

---

## 🧰 Tech Stack

| Component               | Technology                           |
| ----------------------- | ------------------------------------ |
| **Language Model**      | OpenAI GPT-4 / GPT-5                 |
| **Vector Store**        | ChromaDB                             |
| **Framework**           | LangChain                            |
| **Frontend (optional)** | Streamlit / Lovable.dev / FastAPI UI |
| **Language**            | Python 3.10+                         |

---

## 👥 Contributors

| Name   | Role                                       | Contact                       |
| ------ | ------------------------------------------ | ----------------------------- |
| Arshad | Technology Consultant / Solution Architect | arshad.sarfarz.1979@gmail.com |

---

## 🪪 License

This project is released under the **MIT License**. See [LICENSE](LICENSE) for more details.

---
