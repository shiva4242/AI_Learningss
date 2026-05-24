# AI Notes

- `ctrl+shift+v` --> to convert md file to readable
- `/compact` --> gives the summary of the chat and tokens used

## RAG

### Why do we need RAG?
LLMs have several key limitations that RAG helps overcome:

- **Knowledge Cut-off:** Models are only aware of information up to a specific date.
- **Proprietary Data:** Models cannot access a company's internal or private data.
- **Context Window Limits:** Models have a limit on how much text they can process at once.
- **Data Privacy:** Sending private data to a model's server can raise security concerns.

### Breaking down RAG

- **Retrieval:** Fetching relevant information from your external sources (e.g., PDF, database, cloud storage).
- **Augmented:** Taking that fetched information and adding it to your prompt.
- **Generation:** Letting the LLM generate a response based on both its pre-trained knowledge and the newly added, relevant information.

### How RAG works in practice

1. **External Data:** The process starts with your specific data.
2. **Loading & Chunking:** The data is loaded and split into smaller, manageable pieces (chunks).
3. **Embedding:** These chunks are converted into numerical vectors.
4. **Vector Store:** These vectors are stored in a database where they can be searched based on similarity.
5. **Retrieval & Generation:** When a user asks a question, the system finds the most relevant chunks, adds them to the query (augmentation), and sends everything to the LLM to generate the final answer.

### Difference betweek RAG and MCP

<img width="1693" height="1041" alt="image" src="https://github.com/user-attachments/assets/8a92d4a7-af16-43d4-8714-315aedc6c4fc" />

