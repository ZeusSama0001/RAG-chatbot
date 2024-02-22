# RAG Bot

The RAG Bot is a powerful tool designed to provide responses to user queries using llama2 language model and vector stores. This README will guide you through the setup and usage of the RAG Bot.

## Table of Contents

- [Introduction](#rag-bot)
- [Table of Contents](#table-of-contents)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Usage](#usage)


## Prerequisites

Before you can start using the RAG Bot, make sure you have the following prerequisites installed on your system:

- Python 3.6 or higher
- Required Python packages (you can install them using pip):
    - langchain
    - chainlit
    - ctransformers
    - faiss_cpu
    - PyPDF2 (for PDF document loading)
    - torch
    - accelerate
    - bitsandbytes
    - sentence_transformers
    - huggingface_hub
    - openai

## Installation

1. Clone this repository to your local machine.

    ```bash
    git clone https://github.com/ZeusSama0001/RAG-chatbot.git
    cd RAG-chatbot
    ```

2. Create a Python virtual environment (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use: venv\Scripts\activate
    ```

3. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Download the [Llama-2-7B-Chat-GGML model ](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/blob/main/llama-2-7b-chat.ggmlv3.q8_0.bin) on Hugging Face. Please refer to the llama2 documentation for specific instructions on how to download and set up the language model.


5. Set up the necessary paths and configurations in your project, including the `DB_FAISS_PATH` variable and other configurations as per your needs.

## Getting Started

To get started with the RAG Bot, you need to:

1. Set up your environment and install the required packages as described in the Installation section.

2. Configure your project by updating the `DB_FAISS_PATH` variable and any other custom configurations in the code.

3. Prepare the language model and data as per the llama2 documentation.

4. Start the bot by running the provided Python script or integrating it into your application. You can run the RAG chatbot using the following command:
    ```bash
    chainlit run model.py
    ```
   Before running the RAG chatbot, make sure to run `ingest.py` beforehand to create data for the vector database.

## Usage

The RAG Bot can be used for answering queries based on the information stored in its vector database. To use the bot, you can follow these steps:

1. Start the bot by running your application or using the provided Python script.

2. Send a query to the bot.

3. The bot will provide a response based on the information available in its database.

4. If sources are found, they will be provided alongside the answer.

5. The bot can be customized to return specific information based on the query and context provided.

