# Llama-2 with LlamaIndex: Document Querying System

This project demonstrates how to use Meta's **Llama-2** model with **LlamaIndex** (formerly GPT Index) for querying documents uploaded in Google Colab. The system retrieves and answers questions based on the content of PDF files you upload.

## Features:
- Uses **Llama-2 7B Chat** model from Hugging Face.
- Integrates **LlamaIndex** to query PDF files.
- Runs directly in Google Colab, making it easy to set up and experiment.

---

## Setup Instructions

1. **Fork and Clone the Repository**:
   Clone this repository to get started with the provided Colab notebook. You can either run this notebook on your local machine or directly in Google Colab.

   ```bash
   git clone <your-repo-url>
   ```

2. **Upload the Notebook to Google Colab**:
   Open Google Colab and upload the notebook file `Llama2_with_llamaindex.ipynb`. You can also upload it from this repo if needed.

3. **Apply for Access to Llama-2**:
   Before you can use Llama-2, ensure you have access to the model:
   - Go to the [Llama-2 7B Chat Model page on Hugging Face](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf).
   - Click **Request Access** and follow the steps to get permission.
   - Once approved, you’ll receive access to the model for free.

4. **Generate a Hugging Face Token**:
   - Visit your Hugging Face [API Tokens page](https://huggingface.co/settings/tokens).
   - Create a new token and ensure you check "Read access to contents of all public gated repos you can access" in the user permissions.
   - Copy this token as you’ll need it in the next step.

5. **Running the Notebook**:
   In Google Colab:
   - Install the required packages (included in the notebook).
   - Upload any PDF files of your choice. Make sure your PDF files are stored in the `/content/data/` directory.
   - The notebook uses `SimpleDirectoryReader` from LlamaIndex to load these PDFs:
     ```python
     documents = SimpleDirectoryReader("/content/data").load_data()
     ```
   - Once the documents are loaded, you can ask any questions about the content in the query cell:
     ```python
     query = "Your question about the document"
     response = query_engine.query(query)
     print(response)
     ```

6. **Query Documents**:
   After uploading the PDF files and setting up the Llama-2 model, you can start asking questions about your documents by simply running the query cell in the notebook.

---

## Example Workflow

1. **Upload PDF Files**: Upload your files using the Colab interface.
2. **Load Documents**: Use the `SimpleDirectoryReader` to load the documents.
3. **Ask a Question**: Input your question in the query section, and the system will return an answer based on the document content.

---

## Requirements
- Hugging Face account with access to Llama-2.
- Hugging Face API token with permission to access gated content.
- Google Colab environment.
