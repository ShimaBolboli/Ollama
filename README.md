<div align="center">
 <img alt="ollama" height="200px" src="https://github.com/ollama/ollama/assets/3325447/0d0b44e2-8f4a-4e99-9b52-a5c1c741c8f7">
</div>
This document provides a step-by-step guide to using Ollama, a powerful tool for interacting with
large language models (LLMs). We'll cover the installation process, how to use the Ollama API with
Curl.

# Ollama

[![Discord](https://dcbadge.vercel.app/api/server/ollama?style=flat&compact=true)](https://discord.gg/ollama)

Get up and running with large language models.

### macOS

[Download](https://ollama.com/download/Ollama-darwin.zip)

### Windows preview

[Download](https://ollama.com/download/OllamaSetup.exe)

### Linux

```
curl -fsSL https://ollama.com/install.sh | sh
```

[Manual install instructions](https://github.com/ollama/ollama/blob/main/docs/linux.md)


## Quickstart

To run and chat with [Llama 3](https://ollama.com/library/llama3):

```
ollama run llama3
```


## Model library

Ollama supports a list of models available on [ollama.com/library](https://ollama.com/library 'ollama model library')

Here are some example models that can be downloaded:

| Model              | Parameters | Size  | Download                       |
| ------------------ | ---------- | ----- | ------------------------------ |
| Llama 3            | 8B         | 4.7GB | `ollama run llama3`            |
| Llama 3            | 70B        | 40GB  | `ollama run llama3:70b`        |
| Phi 3 Mini         | 3.8B       | 2.3GB | `ollama run phi3`              |
| Phi 3 Medium       | 14B        | 7.9GB | `ollama run phi3:medium`       |
| Gemma              | 2B         | 1.4GB | `ollama run gemma:2b`          |
| Gemma              | 7B         | 4.8GB | `ollama run gemma:7b`          |
| Mistral            | 7B         | 4.1GB | `ollama run mistral`           |
| Moondream 2        | 1.4B       | 829MB | `ollama run moondream`         |
| Neural Chat        | 7B         | 4.1GB | `ollama run neural-chat`       |
| Starling           | 7B         | 4.1GB | `ollama run starling-lm`       |
| Code Llama         | 7B         | 3.8GB | `ollama run codellama`         |
| Llama 2 Uncensored | 7B         | 3.8GB | `ollama run llama2-uncensored` |
| LLaVA              | 7B         | 4.5GB | `ollama run llava`             |
| Solar              | 10.7B      | 6.1GB | `ollama run solar`           |


----------------------------------------------------------------------------------------------------------------------------------------------------
## Different LLm Model


<div align="center">
 <img alt="GPTNeo" height="200px" src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg">
</div>

<h2>GPt Neo</h2>

GPT-Neo, a variant of the GPT family developed by EleutherAI, as our different large language model (LLM). GPT-Neo is known for being highly configurable and efficient, making it suitable for running on local machines. Here’s how you can set up and demonstrate GPT-Neo's functionality locally using curl.

---------------------------------------------------------------------
The steps need to run on the local machine:

## 1-Installation on Mac OS

GPT-Neo can be installed via the Hugging Face Transformers library, which provides an easy interface to interact with various language models.
•	First, ensure you have Python installed on your machine. You can download it from python.org or use a package manager like Homebrew.

```
brew install python
```

•	Install the necessary libraries:

```
pip install torch==1.10.0+cpu torchvision==0.11.1+cpu torchaudio===0.10.0+cpu -f https://download.pytorch.org/whl/cpu/torch_stable.html
pip install transformers
```
## 2- Download and Load GPT-Neo Model
Use the Hugging Face Transformers library to load the GPT-Neo model and tokenizer. GPT-Neo models come in various sizes; for demonstration, we'll use EleutherAI/gpt-neo-1.3B, which is a smaller variant compared to larger models like GPT-3.

•	Create a Python script (gpt_neo.py) to serve the model

Demonstrating Functionality via curl
-----------------------------------------------------------------------
## 1-Set Up a Server to Serve GPT-Neo
Typically, for local interaction via curl, you'd need to set up a simple server that listens for HTTP requests and processes them using the loaded GPT-Neo model. We'll use Python and Flask for this purpose.
•	Create a Python script (gpt_neo_server.py) to serve the model

## 2- Run code
Open a terminal, navigate to the directory where gpt_neo_server.py is saved, and run the server

## 3- Interact with GPT-Neo via curl
Now, simulate interaction with the GPT-Neo model server using curl in another terminal window:

```
curl -X POST -H "Content-Type: application/json" -d '{"text": "Where is the Capital city of Canada?"}' http://127.0.0.1:5000/generate

```

## 4- Expected output 

____________________________________________________________________
{"response":"where is the capital city of Canada?\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital city of Canada is Ottawa.\n\nA:\n\nThe capital"}
_____________________________________________________________________

The generated text will vary based on the prompt provided and the response from the GPT-Neo model.





