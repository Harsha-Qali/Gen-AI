# Gen-AI


\# 🤖 Harsha's Simple RAG Q\&A Assistant



A lightweight \*\*Retrieval-Augmented Generation (RAG)\*\* chatbot built with \*\*LangChain\*\*, \*\*Ollama\*\*, and \*\*Streamlit\*\*.  

It allows users to upload PDFs or enter website URLs, processes them into a vector database using \*\*Chroma\*\*, and answers questions strictly from the provided data.



---



\## 🚀 Features

\- Load data from \*\*URLs\*\* or \*\*PDFs\*\*

\- Ask questions based only on your uploaded content  

\- Works fully \*\*offline\*\* using local Ollama models  

\- Clean and simple \*\*Streamlit\*\* web interface  



---



\## ⚙️ Tech Stack

\- \*\*LangChain\*\* – Framework for LLM pipelines  

\- \*\*Ollama\*\* – Local LLM and embedding generator  

\- \*\*Chroma\*\* – Vector store for document retrieval  

\- \*\*Streamlit\*\* – Frontend UI  

\- \*\*BeautifulSoup4\*\* \& \*\*PyPDF\*\* – For data extraction  



---





1. Create a Virtual Environment



python -m venv venv

\# Activate it

\# On Windows:

venv\\Scripts\\activate



2. Install Dependencies



pip install -r requirements.txt



3. Install and Set Up Ollama



Download and install Ollama from:



https://ollama.ai/download

Once installed, pull the models required by this app:

ollama pull llama3.2:1b

ollama pull embeddinggemma:300m



**4. Running the App**



**Start the Streamlit app:**


**streamlit run app.py**










🧠 How It Works



User Input:

Enter one or more URLs or upload a PDF file.



Document Loading:

Text is extracted from the sources using LangChain loaders.



Chunking \& Embeddings:

Documents are split into small chunks and converted into embeddings with Ollama.



Vector Storage:

Embeddings are stored in a Chroma vector database (temporary folder).



Query Time:

When a question is asked, the most relevant chunks are retrieved and passed to the LLM.



Answer:

The model answers only using the uploaded data. If the answer is not found, it responds:

“I don’t know.”











