# Overview of Large Language Models
## What are LLMs?
LLMs: AI models that are usually (but not necessarily) derived from the Transformer architecture and are designed to understand and generate human language, code, etc.   

The Transformer architecture is quite impressive, as it can be highly parallelized and scaled. Self-attention is used to capture long-range dependencies and contextual relationships.

### NLP tasks that LLMs solve
1. autoencoding: fill in missing words; the encoder part; sentence classification; BERT
2. autoregressive: generate the next word; the decoder part; GPT
3. both

### Key characteristics
The original transformer architecture is a seq-to-seq model that has two main components:
- encoder  
    raw text => core components => vectors => context understandings
- decoder
    predict next token

### How LLMs work
1. Pretraining  
For example, BERT was originally pretrained on English Wikipedia, BookCorpus, and on two specific language modeling specific tasks. Different LLMs are usually trained differently.

2. Transfer Learning
