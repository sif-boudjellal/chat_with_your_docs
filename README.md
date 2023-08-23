# Chat With Your Docs

in this repo I will create chatAPP using chatdocs and GPTQ

1. Quantizing the Model with AutoGPTQ

in AutoGPTQ-transformers.ipynb Notebook, you will see how create quantize model using AutoGPTQ.
in C Transformers (GPTQ).ipynb Notebook, you will see how you can use GPTQ model with CTransformer.

2. Chat App Development with ChatDocs

## Installation 

-	To use GPTQ models, install the auto-gptq package using:
```bash
pip install chatdocs[gptq]
```

-	in the main directory create chatdocs.yml.
-	and add the following to your chatdocs.yml:
```bash
llm: gptq
```
-	To change the GPTQ model, add and change the following in your chatdocs.yml:

```bash
gptq:
    model: TheBloke/Llama-2-7B-GPTQ
    model_file: model.safetensors
```
**Note: When you add a new model for the first time, run chatdocs download to download the model before using it.**

```bash
chatdocs download
```
## Usage

-	Add a directory containing documents to chat with using:
```bash
chatdocs add /path/to/documents
```

The processed documents will be stored in db directory by default.
-	Chat with your documents using:
```bash
chatdocs ui
```

Open http://localhost:5000 in your browser to access the web UI.
It also has a nice command-line interface:
```bash
chatdocs chat
```

for more Configuration visit Chatdocs repo: https://github.com/marella/chatdocs

