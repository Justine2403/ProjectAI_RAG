# ProjectAI_RAG

*Last update: 29/10/2024*

## Create and run a local RAG pipeline from scratch
The goal of this project is to build a RAG (Retrieval Augmented Generation) pipeline from scratch and have it run on a local GPU.

Specifically, we'd like to be able to open a PDF file, ask questions (queries) of it and have them answered by a Large Language Model (LLM).

There are frameworks that replicate this kind of workflow, including LlamaIndex and LangChain, however, the goal of building from scratch is to be able to inspect and customize all the parts.

## Currently working project

The working project but which has not been finalized is the notebook called [`Jack_RAG_project`](/Jack_RAG_project.ipynb).

- What is the current state of the project? <br>
Curerntly, the RAG pipeline is perfectly working fine in the Python notebook.
    - [x] Preprocessing of the data (sentences in a pdf file).
    - [x] Creating embeddings of the text
    - [x] Loading the model (Gemma-2B)
    - [x] Generating text
    - [ ] Deployment with a user interface (hosted frontend) | Not done yet.

- Which LLM model did we use and why? <br>
The model is based on the Gemma-2B open LLM model from Google. <br> 
This model was chosen for relatively great performance with low resources. Due to the hardware limitations available with Google Colab (15GB of VRAM with T4 GPU, we opted for this solution.


- Information of Gemma-2B model:
  - **Description:**<br>
Gemma is a family of lightweight, state-of-the-art open models from Google, built from the same research and technology used to create the Gemini models. They are text-to-text, decoder-only large language models, available in English, with open weights, pre-trained variants, and instruction-tuned variants. Gemma models are well-suited for a variety of text generation tasks, including question answering, summarization, and reasoning. Their relatively small size makes it possible to deploy them in environments with limited resources such as a laptop, desktop or your own cloud infrastructure, democratizing access to state of the art AI models and helping foster innovation for everyone.

  - **Context Length:** <br>
Models are trained on a context length of **8192 tokens**.

  For additionnal information, check this [link](https://huggingface.co/google/gemma-2b).


