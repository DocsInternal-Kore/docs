
# About Answers in Search AI

Answers refer to specific pieces of information extracted or generated by a search application in response to a user query. Unlike traditional search results, which typically present a list of documents, web pages, or content ranked by relevance, **answers** aim to provide precise, exact information tailored to the user's query.

## Getting Started with Search AI

The answer-generation process mainly consists of the following steps.


1. **Content Ingestion**: This step involves ingesting source documents that will be used to generate answers.
2. **Chunking**: Chunking involves breaking down the source documents into smaller, meaningful units called chunks.
3. **Generating Vector embeddings**: Involves converting chunks into multi-dimensional vectors representing the chunks.
4. **Chunk Retrieval**: Involves selecting the most relevant chunks of text from the vector space based on their similarity to the user query.
5. **Answer Generation**: Involves generating a response to the user query based on the retrieved chunks. 

![Answer Generation Process](../images/answer-generation-process.png "Answer Generation Process")

## Commonly Used Terms

* **Chunking:** In the context of answers, Chunking is the process of segmenting large content units into smaller segments. Search AI offers multiple chunking strategies for generating Answers. The choice of strategy depends on the format of the ingested content.

* **Chunking strategy**: Chunking Strategy refers to the rules used for chunk generation. Search AI supports two types of chunking strategies: 
    * **Text-based chunking**: This technique is based on the concept of tokenization. A fixed number of consecutive tokens are identified as one chunk, the next set of tokens as the next chunk, and so on. 
    * **Rule-based chunking**: This technique uses the headers and content in a document to identify chunks. The header and the text between the header and the next header are treated as a chunk. 
* **Embeddings**: Generating Embeddings is the process of creating multi-dimensional vectors from the chunks. These embeddings are then stored in a vector database or vector store. There are different embedding models for generating embeddings. 
* **Chunk retrieval:** It is the process of extracting the most relevant chunk corresponding to a user query. Search AI supports the following two techniques to retrieve chunks. You can experiment with both retrieval methods to find the one that provides the optimum results.
    * **Vector retrieval**: In this method,  the idea is to find vectors that are more similar to the query vector. The chunks corresponding to the vectors most similar to the query vector are then used to generate answers.
    * **Hybrid retrieval**: This method combines the keyword-based retrieval technique with the vector retrieval techniques, leveraging the strengths of both approaches. 
* **RAG (Retrieval Augmented Generation)**: It is a method that allows you to extract data from fragmented, unstructured data and formulate responses based on the information. It involves retrieving both the content and context from a dataset and utilizing this knowledge to generate responses. This technique significantly enhances the precision and relevance of the generated answers.
* **Tokens**: A Token refers to a group of characters. In computing terminology, a token is the smallest unit of data. Roughly, 1 token ~= 4 chars in English.
