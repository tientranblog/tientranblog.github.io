---
title: Building a local Q&A chatbot on custom dataset
excerpt: An AI chatbot run locally to query information from a private dataset
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/163dacc0795d369e7f58ab83d514b34d.png
---

## **Business Scenario**

The business scenario for this application is to provide a Q&A chatbot running locally that can provide quick and accurate answers based on the content of the uploaded documents.
This chatbot is ensure the information answering based on private provided materials, prevent hallucination, a common problem when using cloud-based large language models (LLM). Additionally, the uploaded file mad model are saved locally, ensuring the privacy of the data. Finally, the chat bot is free to use after setup because users don’t have to pay per API request.

## **Techniques**

**Streamlit**: A framework for creating interactive web applications in Python.
**LangChain**: A library for building language model applications.
**Ollama**: A open-source framework for managing LLMs locally.
**LLM**: DeepSeek R1 model, which is significant for chain-of-thought reasoning
**RAG**: stand for Retrieval-Augmented Generation, an AI technique that combines retrieval-based and generative approaches to improve the accuracy and relevance of responses in language models.

## **Workflow**

### **1. File upload** 
Users can upload files in PDF, DOCX, TXT, or CSV formats. The uploaded file is saved locally.
### **2. Document processing** 
Document loader modules to load documents in various formats. The document is split into chunks using  RecursiveCharacterTextSplitter HuggingFace embeddings are created for the document chunks. The document chunks are stored in a vector store (FAISS). A retriever is set up to perform similarity search on the vector store.
### **3. Query input** 
Users can input questions via text box.
### **4. Generating responses**
Ollama DeepSeek R1 model is instantiated for generating responses based on A prompt template. A ConversationalRetrievalChain is created to handle question-answering with the LLM and retriever.
### **5. Response display**
The response is displayed in three tabs: "Answer," "Reasoning," and "History." Any errors during processing are caught and displayed as error messages. The app maintains a history of questions and responses in the session state.

## **Functionalities**

- **Interactive Interface**: The app provides an interactive interface with file upload on sidebar and chatbot question and answer on the main page

<img src="/assets/obsidian/6cbaccb124fca8996ef60df165f97196.png" />

<img src="/assets/obsidian/47b96d50fd891726008b87f0200989ab.png" />

<img src="/assets/obsidian/163dacc0795d369e7f58ab83d514b34d.png" />

- **Support multiple format:** Users can ask questions related to many format docucments such as pdf, docx, txt, csv

<img src="/assets/obsidian/7aa5810deb46b2fb136beaf1c47d8883.png" />

<img src="/assets/obsidian/e4b3259bebc0955f54d047c9bd9b6710.png" />

<img src="/assets/obsidian/d84050f61e61ee7eab750a203d1a5b5a.png" />

<img src="/assets/obsidian/a8cde9d7315642ebc7b1ce991e5e8eeb.png" />

- **Reasoning explanation:** every answer is explained by chain of reasoning supported by Deepseek.

<img src="/assets/obsidian/8ddeb8f0a42db0a88ba68ac41e585ff7.png" />

- **Conversational History**: The app maintains a history of questions and answers, allowing users to review past interactions.

<img src="/assets/obsidian/08258e2e5a2c017efd1587f59e9dac79.png" />

<img src="/assets/obsidian/135e3704fb4234e08fa8505f0fb46a43.png" />


- **Work with tabular data**

<img src="/assets/obsidian/41d53f237796c32f4490d3fce4452551.png" />

<img src="/assets/obsidian/ca2d3fb4d1387d7f254944cea127faac.png" />



## **Demo**

<iframe width="560" height="315" src="https://www.youtube.com/embed/Igcjqi368fk?si=jCjyR4_cBMz4fSD3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>





