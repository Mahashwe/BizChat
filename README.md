# **Bizchat - AI-Powered PDF Assistant for Small Businesses** 💰  

**Bizchat** is an AI-powered **Retrieval-Augmented Generation (RAG) system** designed for **small business owners** to extract insights from their PDF documents. It leverages **similarity search** to find the most relevant sections of uploaded PDFs and generate intelligent responses using **Google Gemini AI**.  

## **Features** 🚀  
✅ **AI-Powered Chatbot** – Uses RAG with Gemini AI for intelligent responses.  
✅ **PDF Processing** – Extracts text from PDFs for semantic search.  
✅ **Similarity Search** – Finds the most relevant document sections using **vector embeddings**.  
✅ **User-Friendly Interface** – Built with Streamlit for ease of use.  
✅ **Small Business Focused** – Helps in managing contracts, reports, and financial documents.  

## **Installation** 🛠️  

### **1. Clone the Repository**  
```bash
git clone https://github.com/yourusername/bizchat.git
cd bizchat
```

### **2. Create a Virtual Environment (Optional but Recommended)**  
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

### **3. Install Dependencies**  
```bash
pip install -r requirements.txt
```

### **4. Set Up API Keys**  
Create a `.env` file in the root directory and add:  
```
GEMINI_API_KEY=your_google_gemini_api_key
```

### **5. Run the Application**  
```bash
streamlit run app.py
```

## **Usage** 🎯  

1. **Upload PDFs** – Drag and drop your business documents.  
2. **Process Documents** – The app extracts, splits, and indexes the text.  
3. **Ask Questions** – Enter a query related to the uploaded documents.  
4. **Get AI-Powered Answers** – The system retrieves **similar text sections** and generates responses via **Gemini AI**.  

## **How It Works** 🧠  

🔹 **Text Extraction** – Extracts text from PDFs using **PyPDF2**.  
🔹 **Text Chunking** – Splits extracted text into smaller segments for better searchability.  
🔹 **Embedding Generation** – Converts text chunks into vector representations using **SentenceTransformers**.  
🔹 **Similarity Search with FAISS** – Finds the most relevant text chunks based on the query.  
🔹 **RAG (Retrieval-Augmented Generation)** – Sends the retrieved text to **Google Gemini AI** for response generation.  

### **🔍 Similarity Search with FAISS**  
- Each text chunk is converted into a **vector representation** using **sentence embeddings**.  
- The system uses **FAISS (Facebook AI Similarity Search)** to store and search for **similar** text segments.  
- When a query is made, FAISS retrieves the **most relevant** text based on **cosine similarity**.  
- The retrieved text is used as **context** to generate AI-powered responses.  

## **Tech Stack** 🔧  

- **Frontend**: Streamlit  
- **PDF Processing**: PyPDF2  
- **Text Splitting**: LangChain  
- **Embeddings**: SentenceTransformers (all-MiniLM-L6-v2)  
- **Vector Search**: FAISS  
- **AI Model**: Google Gemini API  
- **Backend**: Python  

## **Future Enhancements** 🚀  

🔹 **Summarization** – Generate summaries for uploaded documents.  
🔹 **Multi-Document Search** – Compare insights from multiple files.  
🔹 **Integration with Notion/Google Drive** – Fetch documents directly from cloud storage.  
🔹 **Chat History** – Store previous queries for better continuity.  

## **Contributing** 🤝  
Contributions are welcome! If you'd like to improve **Bizchat**, feel free to submit a pull request.  

## **License** 📜  
This project is licensed under the **MIT License**.  

