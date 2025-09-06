This is a Personal AI legal Assistant. 

Multi AI agent system capable of understanding legal issues, classifying them, conducting legal research such as identifying relevant legal sections and precedent cases, and even drafting legal documents in an automated worflow.

Streamlit user interface where users can input their legal issue, trigger the approved AI system and receive a well structured legal draft and response

* Understand the legal issue
* Find applicable IPC sections
* Retrieve matching precent cases
* Generate a formal legal document


- Agent 
    1. Case Intake Agent
    2. IPC section Agent
    3. Legal Precedent Agent
    4. Legal Document Drafting Agent
- Tasks
    1. Case Intake Task
    2. IPC Section Task
    3. Legal Precedent Task
    4. Legal Document Drafter Task
- Customized Tools 
    1. IPC Sections Search Tool - RAG to retrive relevant IPC Section (load/store IPC data (ipc.json) in ChromaDB(vectorDB)) --> Based on legal query we can extract relevant IPC coach. To build this VectorDB we use ipc_vectordb_builder.py
    2. Legal Precedent Search - Tavily Search tool to find relevent precedent cases

Uses ChromaDB to retrive data 

CrewAI for agents orchestration - crew.py

Output: Legal document/information requested --> Streamlit UI 

Streamlit app --> app.py
query_vectordb.py --> to test the query to retrive from vectordb before using it in main chromadb