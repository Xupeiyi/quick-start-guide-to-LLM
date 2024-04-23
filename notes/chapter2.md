# Semantic Search with LLMs
## Introduction
We can use LLMs to generate text embeddings.

Text embeddings are a way to represent words or phrases as machine-readable numerical vectors in a multidimensional space, generally based on their contextual meaning.

Can be thought of as a kind of hash with meaning.

## Task
### Asymmetric Semantic Search
The asymmetric part refers to the fact that there is an imbalance between the semantic information (basically the size) of the input query and the documents/information that the search system has to retrieve.

Can produce very accurate and relevant search results, even if you don’t use exactly the right words in your search.

## Solution
Ingest documents
- collect documents for embedding
- create text embeddings
- store embeddings

Retrieve documents
- user's query (may be preprocessed and cleaned)
- retrieve candidate documents via embedding similarity
- re-rank the candidate documents if necessary
- return the final search results to the user

## Component

### Text Embedder
Takes in a text document, or a single word or phrase, and converts it into a vector.  

The vector is unique to that text and should capture the contextual meaning of the phrase.

The choice of the text embedder is critical, as it determines the quality of the vector representation of the text. 
Options: OpenAI, Sentence Transformers

### Document Chunking
Often it's not practical to embed entire documents as a single vector. Divide a large document into smaller, more manageable chunks for embedding.  

1. Max Token Window Chunking  
Set overlapping windows with a specified amount of tokens to overlap so that tokens are shared between chunks, in case of splitting up meaningful context.

2. Finding Custom Delimiters  
Search for custom natural delimiters like page breaks in a PDF or newlines between paragraphs.

3. Clustering
Use clustering to create semantically-similar chunks, thus creating a new document.

4. No Chunking at all

### Vector Database
Pinecone: ideal for less than 1 million entries
Open Source Alternatives: Pgvector, Weaviate, 
