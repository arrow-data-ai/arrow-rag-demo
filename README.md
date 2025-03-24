# Welcome to Arrow RAG Assistant Demo! 

This demo demonstrates how to easily deploy and customize a **Retrieval Augmented Generation (RAG)** model using **NVIDIA NIMs** or locally on **NVIDIA DGX** or another other local hardware, enabling high-performance inference for enterprise use cases.


RAG, or Retrieval Augmented Generation, is a framework that combines the strengths of large language models (LLMs) and external knowledge retrieval systems. It allows the model to fetch relevant information from external sources, such as databases or knowledge bases, during the generation process, improving accuracy and relevance while reducing hallucinations.

![RAG Diagram(static/img/rag_diagram.png)](static/img/rag_diagram.png)

## Features

This demo offers flexibility and customization in the following areas:

**Deployment Options**: Choose between hosting the LLM locally or using NVIDIA NIMs.

![Deployment Selection(static/img/deployment-selection.png)](static/img/deployment-selection.png)

**Retrieval Sources**: You can select from different retrieval sources, including uploading a PDF, using previously chosen PDFs about Arrow Electronics in the "docs" folder, or specifying URLs in rag_engine.py file. 

![Database Selection(static/img/database-selection.png)](static/img/database-selection.png)

**LLM Selection**: The demo currently features LLaMA 3.1, Phi 3.5, and Gemma 2. However, you can swap out these models for any compatible LLM.

**LLM Parameters**: Use an interactive slider to adjust model parameter temperature. The code can also be customized to modify additional properties such as top-k or top-p values, allowing fine-tuning of the model's output.

![LLM Model Selection(static/img/llm-model-selection.png)](static/img/llm-model-selection.png)


**Application & UI Customization**: 

This demo is built using LangChain for the RAG process and Streamlit for the frontend, providing a seamless, interactive experience. You can personalize the theme, font, and branding to suit your preferences.


## Running the Demo

Follow these steps to set up and run the demo:

**1. Install Ollama and LLM Models**

Install **[Ollama](https://ollama.com)** and ensure the LLM models you want to use are installed. Run the following command for each model:

    ollama pull <modelname> 

You can replace ```<modelname>``` with ```llama3.1 ```, ```phi3.5```, and ```gemma2```for this demo. 


**2. Install Required Packages**

Install the necessary Python packages listed in requirements.txt:

    pip install -r requirements.txt

**3. Set NVIDIA_API_KEY**:

Generate your API key from [NVIDIA NIMs API Catalog](https://build.nvidia.com/explore/discover) and run the following command in your environment's terminal: 

    export NVIDIA_API_KEY='nvapi-???'

This step is required to run the demo properly. 

**4. Run the Frontend**
Start the Streamlit app:

    streamlit run rag.py

**4. Open Port 8501**

Make sure port ```8501``` is open on your localhost to access the demo in your browser. You can change the port in ```./.streamlit/config.toml``` file. 


**5. Experiment with the Demo**

Explore the demo and experiment with different deployment, retrieval, and model options to see how RAG can improve inference for your use cases.

![Nim Inference(static/img/nim_inference.png)](static/img/nim_inference.png)

![DGX Inference(static/img/dgx_inference.png)](static/img/dgx_inference.png)

## Additional Resources

* [NVIDIA NIM API Catalog](https://build.nvidia.com/explore/discover)

* [LangChain Documentation](https://python.langchain.com/docs/introduction/)

* [Streamlit Documentation](https://docs.streamlit.io)

* [Ollama Installation](https://ollama.com)