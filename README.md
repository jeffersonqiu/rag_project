# Retrieval Augmented Generation 

This repository contains my learning related to Retrieval-Augmented Generation (RAG) system for Large Language Model. As the project grows, more components and enhancements will be added.

## Contents

- [RAG Components](#rag-components)
- [RAGCeption](#ragception)

## RAG Components

Retrieval-Augmented Generation (RAG) is a technique that combines the strengths of retrieval-based models and generation-based models. The key components of RAG include:

1. **Document Loader**: It is an interface to load documents from different sources.

2. **Indexing**
   a. **Splitting**: to ensure limitation of max token input for LLM is meet and due to cost consideration.
   b. **Embedding**: to create vector representation of a piece of document/ text, enabling efficiency in document retrieval.
   c. **Vector Store**: to enable quick search over unstructured data for efficient data retrieval.
  
4. **Retriever**: This component is responsible for fetching relevant documents or passages from a large corpus based on a given query. 

5. **Generator**: This component takes the retrieved documents and generates a coherent response or answer. The generator is typically a language model (such as GPT-3 or T5) that has been fine-tuned for the specific task.

## RAGCeption

RAGCeption is an advanced approach designed to improve the retrieval coverage and accuracy of the RAG system. It introduces the concept of Query Translation through Multi-Query and RAGFusion techniques.

### Query Translation

Instead of relying solely on the original query, RAGCeption leverages Large Language Models (LLMs) to create multiple similar queries. This multi-query approach enhances the retrieval process by covering a wider range of relevant documents.

#### 1. Multi-Query

Multi-Query involves generating several variations of the original query using the LLM. These variations are used to retrieve additional documents that might be missed by the original query alone. This approach increases the likelihood of finding relevant information.

#### 2. RAGFusion

RAGFusion combines the results from multiple queries to produce a more accurate and comprehensive set of retrieved documents. By aggregating the information from different queries, RAGFusion ensures that the generated responses are based on a richer and more diverse set of data.

## Getting Started

To get started with this project, clone the repository and explore the existing components. Contributions and suggestions are welcome as we continue to develop and enhance the RAG system.

```bash
git clone https://github.com/jeffersonqiu/rag_project.git
