Overview : This is PART 2

This application allows users to upload PDFs, which are processed and indexed by the system, enabling them to ask questions about the content. It leverages Amazon Bedrock for embeddings, LangChain for retrieval-based question answering (RAG), and FAISS for vector search. The system consists of two key components:
Admin Interface: Uploads PDFs, processes them, and creates the vector store.
User Interface: Allows users to query the uploaded PDF content using natural language.
Both services are hosted using Streamlit and deployed via Docker containers.

How the Application Works
+-------------------------+
|      Admin (Streamlit)   |
|-------------------------|
| - PDF Upload            |
| - Text Splitting        |
| - Embedding with Bedrock|
| - Vector Store Creation |
| - Upload to S3          |
+-------------------------+
           |
           | S3 (Storage)
           v
+-------------------------+
|      User (Streamlit)    |
|-------------------------|
| - Download FAISS Index  |
| - Load Vector Store     |
| - LLM (Claude-v2)       |
| - Query and Answer      |
+-------------------------+

For Detailed Documentation of RAG app Refer to 'RAG-APP-0n-AWS-DOCs' File
