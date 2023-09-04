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
Transfer learning is a technique used in machine learning to leverage the knowledge gained from one task to improve performance on another related task.

3. Fine Tuning  
Training the LLM on a smaller, task-specific dataset to adjust its parameters for the specific task.

4. Attentions  
Attention is a mechanism used in deep learning models that assigns different weights to different parts of the input, allowing the model to prioritize and emphasize the most important information while performing tasks like translation or summarization.

5. Embedding  
Embeddings are used to represent the words, phrases, or tokens in a way that captures their semantic meaning and relationships with other words.

6. Tokenization  
Breaking text down into the smallest unit of understanding - tokens.
Stop words removal, stemming, and truncation are not used for LLMs.

7. Beyond Language Modeling—Alignment + RLHF  
Alignment in language models refers to how well the model can respond to input prompts that match the user’s expectations.

## Popular LLMs
### BERT
- Bi-directional Encoder Representation from Transformers
- encoder
- good at processing/understanding massive amounts of text very quickly

### GPT-3 and ChatGPT
- Generative Pre-trained Transformers
- decoder 
- good at generating text one token at a time.

### T5
- Text to Text Transfer Transformer
- encoder/decoder
- perform multiple tasks with no fine-tuning

### Domain-Specific LLMs
BioGPT

## Applications of LLMs
- Using a pre-trained LLM’s underlying ability to process and generate text with no further fine-tuning as part of a larger architecture.
- Fine-tuning a pre-trained LLM to perform a very specific task using Transfer Learning.
- Asking a pre-trained LLM to solve a task it was pre-trained to solve or could reasonably intuit.