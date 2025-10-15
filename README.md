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
| “What is the minimum internet speed requirement for remote workers?”      | The minimum internet speed requirement for remote workers is 25 Mbps download and 5 Mbps upload.                |
| “How many core office days are required per week for hybrid employees?” | Hybrid employees are required to be in the office on two core office days per week: Tuesdays (designated collaboration day) and Thursdays (team meeting day). |
| “what is the weightage of business results vs behavioural competencies during performance review”      | The weightage of business results versus behavioral competencies during performance reviews is typically 70% for business results and 30% for behavioral competencies and collaboration.                |
| “How many days in advance the tickets need to be booked for air travel?”      | How many days in advance the tickets need to be booked for air travel?                |
| “Is MFA mandatory for remote access?”      | Yes, Multi-Factor Authentication (MFA) is mandatory for all remote access, as stated in the password and authentication standards section of the context provided.                |


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
