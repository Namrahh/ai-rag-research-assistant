
# AI & RAG Research Assistant

An AI-powered research assistant that uses Retrieval-Augmented Generation (RAG) to answer questions from a collection of research papers.

## Features

- Loads multiple research papers in PDF format
- Extracts text from the papers
- Splits documents into overlapping chunks
- Converts chunks into vector embeddings using BGE
- Uses FAISS for similarity-based retrieval
- Uses a Cross-Encoder to rerank retrieved chunks
- Uses Qwen 2.5 0.5B Instruct to generate answers
- Refuses to answer when the retrieved context is not relevant

## RAG Pipeline

Documents → Chunking → Embeddings → FAISS Retrieval → Reranking → Qwen → Answer

## Technologies Used

- Python
- Sentence Transformers
- BGE embeddings
- FAISS
- Cross-Encoder
- Qwen 2.5
- PyPDF2
- Google Colab

## Dataset

The project uses five research papers related to Retrieval-Augmented Generation, text embeddings, and RAG evaluation.

## Example Questions

- What is RAGCHECKER?
- What are text embeddings used for?
- Why are text embeddings important for RAG?
- How does RAG reduce hallucinations in large language models?

## Out-of-Scope Handling

If the retrieved documents do not contain enough information to answer a question, the system responds:

"The provided context does not contain enough information."

## Limitations

- The current system uses a small language model (Qwen 2.5 0.5B).
- The system currently selects the highest-ranked retrieved chunk as context.
- PDF text extraction may not work perfectly for scanned documents.
- The project is currently designed for research-paper question answering.

## Future Improvements

- Add a web or Streamlit interface
- Support more document formats
- Improve document retrieval and context selection
- Add citation display for generated answers
- Add conversation history
- Deploy the application

## Author

Namra Aftab
