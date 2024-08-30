# RAG with Llama3.1 on Google Colab

This repository contains a Google Colab notebook that demonstrates how to use Retrieval-Augmented Generation (RAG) with the Llama3.1 model from Ollama. The notebook allows users to upload a file, process its content, and ask questions about the provided context using a Gradio interface.

## Features

- Load and process documents from a URL or an uploaded file.
- Split documents into chunks for efficient processing.
- Create embeddings and a vector store using Ollama's models.
- Use the Llama3.1 model to answer questions based on the provided context.
- Interactive Gradio interface for easy user interaction.

## Getting Started

### Prerequisites

- A Google account to use Google Colab.
- Basic knowledge of Python and Jupyter notebooks.

### Running the Notebook

1. **Open the Notebook in Google Colab**

   Click the badge below to open the notebook directly in Google Colab:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mrodgers/ollama_rag_colab/blob/main/Testing_Ollama_RAG.ipynb)

2. **Install Required Packages**

   Run the following cells to install the necessary packages:

   ```python
   !pip install colab-xterm
   %load_ext colabxterm
   %xterm
   ```

   In the terminal that opens, run the following commands:

   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ollama serve &
   ollama pull llama3.1 &
   ollama pull nomic-embed-text &
   ```

3. **Install Python Libraries**

   Run the following cell to install the required Python libraries:

   ```python
   !pip install langchain langchain-core langchain-community beautifulsoup4 chromadb gradio -q
   ```

4. **Run the Code**

   Execute the remaining cells in the notebook to load the models, process the documents, and launch the Gradio interface.

## Usage

### Uploading a File and Asking Questions

1. **Upload a File**

   Use the Gradio interface to upload a file containing the text you want to process.

2. **Ask a Question**

   Enter your question in the provided textbox and click the submit button. The model will process the question and provide an answer based on the content of the uploaded file.

## Acknowledgements

Thanks to [Tharindu Madhusanka](https://medium.com/@tharindumadhusanka99/llama3-rag-on-google-colab-73c43aa53281) for some of the code used in this notebook.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
