# Chat 'Privately' in Google Colab with Ollama/llama3.1/RAG 

This repository contains a Google Colab notebook that demonstrates how to set up and run a Retrieval-Augmented Generation (RAG) system using Ollama's Llama3.1 model. The notebook includes steps to install necessary packages, set up an xterm terminal, and run the Ollama server. It also provides a Gradio interface for uploading files and asking questions based on the provided context.

## Setup and Running in Google Colab

### Prerequisites

- A Google account to use Google Colab.
- Basic knowledge of Python and Jupyter notebooks.

### Steps to Run

1. **Open the Colab Notebook**

   Click the badge below to open the notebook in Google Colab:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mrodgers/ollama_rag_colab/blob/main/Testing_Ollama_RAG.ipynb)

2. **Install Required Packages**

   Run the following cells to install the necessary packages:

   ```python
   !pip install colab-xterm -q
   %load_ext colabxterm
   %xterm
   ```

   ```python
   !pip -q install langchain langchain-core langchain-community ollama beautifulsoup4 chromadb gradio pypdf
   ```

3. **Set Up xterm and Ollama**

   After running the `%xterm` cell, an xterm terminal will open. In the terminal, run the following commands:

   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ollama pull llama3.1 &
   ollama pull nomic-embed-text &
   ollama serve &
   ```

4. **Run the Main Script**

   The main script includes functions to load text and PDF files, process them, and create a vector store. It also defines a Gradio interface for interacting with the RAG system.


5. **Use the User Interface**

   The interface allows you to upload a file and ask questions about its content. Simply upload a text or PDF file and enter your question in the provided textbox.

## Notes

- **Is Colab Safe for Private Data?**

  Colab is NOT safe for any Cisco data. In general, it is as safe as your private Google Docs. No one can access your private Colab notebooks, and Google has an incentive to make it as safe as possible for their reputation. However, avoid sharing any sensitive or confidential information.

## Acknowledgements

Thanks to [Tharindu Madhusanka](https://medium.com/@tharindumadhusanka99/llama3-rag-on-google-colab-73c43aa53281) for some of the code used in this notebook.
