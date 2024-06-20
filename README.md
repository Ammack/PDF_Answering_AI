# PDF Answering AI

The PDF Answering AI chatbot intelligently interacts with PDF documents, offering features like summarization, content location, simplification, and question answering. It’s built using Streamlit and can be accessed directly on Colab.

## Features 
**Summarization**:  Obtain brief summaries of essential content from uploaded PDFs.

**Information Retrieval**:  Locate specific details or data within the documents.

**Simplification**:  Simplify difficult-to-understand parts of the documents.

**Key Highlights**:  Identify key findings or critical clauses in the PDFs.

**Question Answering**:  Provide answers based on the document content and ongoing conversation.

# SETUP FOR COLAB

## Requirements

First, pull the repository from github and then, install the requirements by running the following 2 commands:

```python
!pip install streamlit -q
```

```python
!pip install -r requirements.txt
```


## Download the Model

Download the Mistral-7B-Instruct-v0.2 model by running the following command:

```python
!curl -L "https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.2-GGUF/resolve/main/mistral-7b-instruct-v0.2.Q5_K_M.gguf?download=true" -o ./mistral-7b-instruct-v0.2.Q5_K_M.gguf
```

Verify that the model file has been downloaded by running:

```python
!ls mistral-7b-instruct-v0.2.Q5_K_M.gguf
```


## Build the Llamacpp Package

Build the package by running the following command:

```python
!CMAKE_ARGS="-DLLAMA_CUBLAS=on" FORCE_CMAKE=1 pip install llama-cpp-python
```

This command is required for GPU activation.


## Get Your IP Address

Get your IP address by running the following command:

```python
!wget -q -O - ipv4.icanhazip.com
```

Copy this address and keep it.


## Run the App and Create a Local Tunnel

Run the app by creating a local tunnel by running the following command:

```python
!streamlit run app.py & npx localtunnel --port 8501
```

This will generate a link for a new page, which will look something like this:


```python
Collecting usage statistics. To deactivate, set browser.gatherUsageStats to false.
You can now view your Streamlit app in your browser.
Local URL: http://localhost:8501
Network URL: http://172.28.0.12:8501
External URL: http://34.147.102.1:8501
npx: installed 22 in 3.903s
your url is: https://rare-gifts-share.loca.lt
```

Copy the provided URL (e.g., `https://rare-gifts-share.loca.lt`) and paste it into your browser to access the app.


## Paste the Code

Once the app is open in your browser, paste the copied code into the text box and submit it.

That's it! You've now successfully installed and set up the PDF Answering AI on your colab.

## Dependencies and Device Specs (In case deployed locally)

### Model and Hardware Requirements
- **Model Size:** 5.13 GB
- **GPU Requirement:** 8 GB
- **Embedding Model Size:** 2.5 GB
- **CPU Requirement:** 4 GB

### Required Packages
To ensure the application runs smoothly, the following packages are required:

- `streamlit`
- `langchain==0.0.184`
- `PyPDF2==3.0.1`
- `python-dotenv==1.0.0`
- `faiss-cpu==1.7.4`
- `altair==4`
- `tiktoken==0.4.0`
- `huggingface-hub==0.14.1`
- `sentence-transformers==2.2.2`



