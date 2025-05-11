This notebook demonstrates development of a document-aware chatbot using LangChain’s Conversational Retrieval Chain to answer questions about history books. 

The notebook covers the following steps:
1. Load and preprocess documents using LangChain's document loaders and text splitters.
2. Create embeddings and set up a vector store for efficient document retrieval.
3. Implement a conversational retrieval chain that combines document retrieval with language model responses.
4. Add conversational memory to allow the chatbot to remember and refer to previous interactions.
5. Test the chatbot with sample questions and analyze its performance.

Note:
* This notebook was built in Google Colab free version and only utlizes open-source language models and packages.
* MiniLM sentence transformer is used for constructing the vector space for semantic searching.
* A quantized Llama 3-8B Instruct model is uesed for question answering.
	