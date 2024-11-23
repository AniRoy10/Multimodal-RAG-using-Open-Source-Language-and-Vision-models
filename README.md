This project implements a Multimodal Retrieval-Augmented Generation (RAG) pipeline using open-source Language and Vision models, designed for efficient semantic search and question answering across multiple data types, including text, tables, and images.

Pipeline Overview:

1. Data Collection: Gather multimodal data consisting of text, tables, and images.  
2. Data Organization: Segregate data into separate placeholders for text, tables, and images.  
3. Summarization:  
   - Use language models to generate concise summaries for text and tables.  
   - Use vision models to create summaries for image data.  
4. Indexing and Storage:  
   - Assign unique `doc_id`s to each element.  
   - Store summaries in a VectorStore for semantic search.  
   - Store the original documents in a DocumentStore, linking them to summaries via `doc_id`.  
5. Query Handling:  
   - Perform semantic search on the VectorStore to retrieve relevant summaries.  
   - Use the `doc_id` from metadata to fetch original documents from the DocumentStore.  
   - Provide the retrieved context and user query to a language model, which generates an accurate response with source attribution.  

This pipeline efficiently handles multimodal data, supports accurate information retrieval, and provides contextual, source-referenced answers, all powered by open-source models.
