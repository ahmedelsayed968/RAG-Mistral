# RAG-Mistral
## What is RAG
Simply we provide the LLM with external data for example pdfs,urls,...etc helping to generate more conventent answer based on the source knowledge and parameteric knowledge that gained from the training on large amount of data

## Pipeline
![image](https://github.com/ahmedelsayed968/RAG-Mistral/assets/88388782/59697d70-859f-411c-aa6b-d410aac072f2)

1. Load data and split it into chunks
2. Configure a suitable vector database for example FAISS or Pinecone
3. configure the embeddings that used to embedded taxt into vector of numbers understandable by Models
4. Create index by passing the chunks throught the embedding matrix and then store it into the vector database
5. Configure the LLM
   - Get the name of the model from huggingface 
   - load the tokenizer first
   - set the configuration used for that model
   - add quantization settings to load it with small size
   - create a HuggingFace wrapper for the loaded model to integrate it easily with langchain
   - config the Retrieval Chain from Langchain
   - Enjoy using it!
    
