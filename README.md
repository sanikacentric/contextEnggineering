# Context Engineering for LLMs

A comprehensive Jupyter notebook exploring context engineering techniques for Large Language Models — the art and science of designing, structuring, and optimizing the context provided to LLMs to maximize response quality, accuracy, and relevance.

## Description

Context engineering goes beyond basic prompt engineering to systematically manage what information an LLM can "see" during inference. This repository covers techniques including context window management, dynamic context selection, context compression, memory systems, retrieval-augmented context injection, and structured context formatting.

## Features

- **Context Window Optimization** — Techniques to maximize information density within token limits
- - **Dynamic Context Selection** — Intelligently select which information to include based on query relevance
  - - **Context Compression** — Summarize and compress long contexts while preserving key information
    - - **Memory-Augmented Context** — Integrate episodic and semantic memory into context windows
      - - **RAG Context Injection** — Retrieve and inject relevant document chunks into the context at inference time
        - - **Structured Context Formatting** — Use XML tags, JSON, and structured templates for consistent context organization
          - - **Multi-turn Conversation Context** — Manage conversation history and context across multiple turns
            - - **Tool Output Integration** — Format and inject tool/API call results into context
             
              - ## Context Engineering Techniques
             
              - | Technique | Purpose |
              - |---|---|
              - | Sliding Window | Maintain recent conversation history within token budget |
              - | Semantic Compression | Summarize older turns to reclaim context space |
              - | Selective Retrieval | Only inject RAG results most relevant to current query |
              - | Structured Templates | Use consistent XML/JSON schemas for predictable parsing |
              - | Tiered Memory | Short-term (in-context) + long-term (external) memory |
              - | Context Prioritization | Weight recent and high-relevance information higher |
             
              - ## Tech Stack
             
              - | Component | Technology |
              - |---|---|
              - | Language | Python 3 |
              - | LLM Framework | LangChain / OpenAI API |
              - | Vector Store | FAISS / Chroma |
              - | Memory | LangChain Memory modules |
              - | Tokenization | tiktoken |
              - | Notebook | Jupyter (Google Colab) |
             
              - ## Setup Instructions
             
              - ### Prerequisites
             
              - - Python 3.8+
                - - OpenAI API key
                 
                  - ### Installation
                 
                  - ```bash
                    git clone https://github.com/sanikacentric/contextEnggineering.git
                    cd contextEnggineering
                    pip install langchain openai tiktoken faiss-cpu chromadb jupyter
                    ```

                    ### Configuration

                    ```bash
                    export OPENAI_API_KEY=your-openai-api-key
                    ```

                    ### Running the Notebook

                    ```bash
                    jupyter notebook
                    ```

                    ## Key Concepts

                    **Context Window**: The total tokens an LLM can process at once (e.g., GPT-4 Turbo: 128K tokens, Claude: 200K tokens).

                    **Context Engineering vs. Prompt Engineering**: Prompt engineering focuses on instruction design; context engineering focuses on what supporting information surrounds those instructions.

                    **The Context Budget Problem**: With finite token limits, every token counts — context engineering ensures the most valuable information fills the available space.

                    ## License

                    Open source — for educational and AI research purposes.
