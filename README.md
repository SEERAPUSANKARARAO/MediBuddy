# MediBuddy

Develop MediBuddy, an medical chatbot, by integrating the power of Mistral and Llama 2 models through the LangChain framework and Pinecone Vector Database. This innovative solution leverages either the Mistral or Llama 2 model to ensure robust natural language processing and understanding, providing accurate and insightful medical responses. The use of LangChain facilitates seamless chaining of model outputs for complex queries, while Pinecone's Vector DB ensures efficient and scalable vector search capabilities, enhancing the chatbot's ability to retrieve relevant medical information quickly and accurately. Whether you choose to deploy with Mistral or Llama 2, MediBuddy promises to deliver reliable and responsive healthcare assistance based on sample medical data.

## How to Run?

### Steps:

1. **Clone the Repository**

    ```bash
    git clone https://github.com/your-repo-link.git
    cd your-repo-directory
    ```

2. **Create a Conda Environment**

    ```bash
    conda create -n mchatbot python=3.8 -y
    conda activate mchatbot
    ```

3. **Install the Requirements**

    ```bash
    pip install -r requirements.txt
    ```

4. **Create a `.env` File**

    Add your Pinecone credentials in the root directory:

    ```ini
    PINECONE_API_KEY = "your_pinecone_api_key"
    PINECONE_API_ENV = "your_pinecone_api_env"
    ```

5. **Download the Quantized Models**

    Download the following models and place them in the `model` directory:

    - **Mistral-7B-Instruct-v0.2.Q8_0.gguf**
    - **Llama-2-7b-chat.Q8_0.gguf**
    - **Llama-2-7b-chat.ggmlv3.q4_0.bin**

    Download from these links:
    - [Mistral-7B-Instruct-v0.2-GGUF](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.2-GGUF)
    - [Llama-2-7B-Chat-GGUF](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF)
    - [Llama-2-7B-Chat-GGML](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main)

6. **Store the Index**

    ```bash
    python store_index.py
    ```

7. **Run the Application**

    ```bash
    python app.py
    ```

8. **Access the Application**

    Open your web browser and navigate to:

    ```bash
    localhost:your_port_number
    ```

## Tech Stack Used:

- **Python**
- **LangChain**
- **Flask**
- **Meta Llama 2**
- **Pinecone**

