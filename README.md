
# Chat With Your Docs

Welcome to the **Chat With Your Docs** repository, where we explore the integration of ChatDocs and GPTQ quantization method for an interactive chat app with your documents!

## Quantizing the Model with AutoGPTQ

In the `AutoGPTQ-transformers.ipynb` notebook, discover the process of creating a quantized model using AutoGPTQ. Additionally, in the `C Transformers (GPTQ).ipynb` notebook, explore how to utilize the GPTQ model with CTransformer.

## Chat App Development with ChatDocs

### Installation

1. To incorporate GPTQ models, install the `auto-gptq` package using:
```bash
pip install chatdocs[gptq]
```

2. In the main directory, create `chatdocs.yml`.

3. Add the following to your `chatdocs.yml`:
```yaml
llm: gptq
```

4. To change the GPTQ models, modify your `chatdocs.yml` as follows:
```yaml
gptq:
    model: TheBloke/Llama-2-7B-GPTQ
    model_file: model.safetensors
```
**Note: When adding a new model for the first time, run `chatdocs download` to download the model before use.**

```bash
chatdocs download
```
###  CTransformers & GPTQ model:

To change the C Transformers with GPTQ model, add and change the following in your `chatdocs.yml`:
```yaml
ctransformers:
  model: TheBloke/Llama-2-7B-GPTQ
  model_file: model.safetensors
  model_type: gptq
```
You can also use an existing local model file:
```yaml
ctransformers:
  model: /path/to/ggml-model.bin
  model_type: gptq
```
### Usage

1. Add a directory containing documents to engage in conversation with using:
```bash
chatdocs add /path/to/documents
```

The processed documents will be stored in the `db` directory by default.

2. Chat with your documents:
```bash
chatdocs ui
```

Access the web UI at http://localhost:5000 in your browser.

The command-line interface is also available:
```bash
chatdocs chat
```


\
\
\
**For further configuration options, visit the ChatDocs repository:** [ChatDocs Repo](https://github.com/marella/chatdocs)


