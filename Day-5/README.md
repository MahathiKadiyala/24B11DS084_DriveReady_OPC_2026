# Day 5 – Memory and RAG

**Date:** 27 November 2026

## Overview

Day 5 focused on giving AI agents memory and access to external knowledge using Retrieval-Augmented Generation (RAG).

I explored different types of memory, conversation management using LangGraph, embeddings, vector databases and knowledge retrieval using ChromaDB. I also extended my VoltCare AI customer and service assistant by integrating a knowledge base and conversation memory with the tools developed on Day 4.

## Concepts Learned

### 1. Three Types of Memory

Explored different ways an AI agent can retain and use information:

- **Conversation Memory:** Maintains context from previous messages in a conversation.
- **Knowledge Memory:** Stores information that an agent can retrieve when required.
- **Long-Term Memory:** Retains useful information across multiple interactions.

### 2. Conversation Memory

Learned how an agent can remember previous interactions using:

- LangGraph `InMemorySaver` checkpointer.
- Unique `thread_id` for each conversation.
- Conversation history across multiple messages.
- Separate memory for different customer conversations.

### 3. Why Not Everything Goes Into the Prompt

Understood why storing all business information directly in a system prompt is not ideal.

A searchable knowledge base allows the agent to retrieve only relevant information when answering a question, making the application easier to maintain and extend.

### 4. Embeddings and Vector Databases

Explored:

- **Embeddings:** Convert text into numerical representations that capture semantic meaning.
- **Vector Database:** Stores and retrieves information based on similarity.
- **ChromaDB:** Used to store business knowledge and retrieve relevant documents.

### 5. Retrieval-Augmented Generation (RAG)

Learned how RAG connects an LLM with an external knowledge source.

Basic RAG workflow:

**User Question → Embedding → Similarity Search → Retrieved Knowledge → LLM Response**

RAG helps the agent answer questions using relevant stored information instead of relying only on its pretrained knowledge.

### 6. Chunking

Understood how information is divided into smaller units called chunks before storing it in a vector database.

For the Day 5 implementation, each business fact was stored as one separate document in ChromaDB.

### 7. Grounded Responses and Hallucination Prevention

Learned to restrict the agent's answers to available knowledge.

If the requested information is not available in the knowledge base, the agent should clearly communicate that the information is not confirmed instead of inventing an answer.

## Practical Implementation

### 1. VoltCare AI Knowledge Base

Extended the EV customer and service assistant by creating a business-specific knowledge base.

Implemented:

- Prepared 20 VoltCare AI business facts.
- Covered service information, sample prices, customer enquiries and prototype limitations.
- Assigned a unique ID to each fact.
- Stored each fact as a separate document in ChromaDB.
- Verified the knowledge base document count.

### 2. ChromaDB and Knowledge Retrieval

Integrated ChromaDB to store and search VoltCare business information.

Implemented:

- Created an in-memory ChromaDB collection.
- Generated embeddings for business facts.
- Stored documents with unique IDs.
- Retrieved relevant information using similarity search.
- Tested knowledge retrieval with EV customer questions.

### 3. RAG Search Tool

Created a reusable knowledge retrieval function and integrated it into the agent.

**`search_ev_knowledge(question)`**

Searches the VoltCare knowledge base and returns relevant information for the given question.

Implemented:

- Created a search function with a descriptive docstring.
- Retrieved relevant business facts from ChromaDB.
- Exposed the search functionality as an agent tool.
- Used retrieved information to generate grounded responses.

### 4. Conversation Memory Using LangGraph

Integrated conversation memory using LangGraph's `InMemorySaver`.

Implemented:

- Added a checkpointer to the agent.
- Used unique `thread_id` values for separate conversations.
- Maintained context across follow-up questions.
- Tested conversation continuity.
- Verified that different customer threads do not share conversation history.

### 5. Day 4 Agent Integration

Extended the existing VoltCare AI agent by combining its tools with knowledge retrieval and conversation memory.

Integrated:

- `get_service_price()` – Retrieves sample EV service price information.
- `check_service_supported()` – Checks whether a service is listed in the supported service catalogue.
- `log_service_enquiry()` – Records customer enquiries when Google Sheets is connected and the write succeeds.
- `search_ev_knowledge()` – Retrieves relevant information from the ChromaDB knowledge base.

The upgraded agent can use its tools, retrieve business knowledge and maintain conversation context.

### 6. Testing and Hallucination Prevention

Tested the upgraded agent using different customer questions.

Implemented:

- Tested knowledge retrieval.
- Checked follow-up questions within the same conversation.
- Tested separate customer thread IDs.
- Asked questions outside the knowledge base.
- Checked whether the agent avoids inventing unsupported warranty and appointment information.
- Verified that the agent communicates when information is unavailable.

**Testing focus:**

| Test Area | Expected Behaviour |
|---|---|
| Knowledge retrieval | Retrieves relevant stored facts |
| Conversation memory | Remembers previous messages in the same thread |
| Thread isolation | Keeps separate conversations independent |
| Unknown questions | Does not invent unsupported information |
| Service price | Returns configured sample estimates |
| Service support | Checks only the supported service catalogue |

### 7. Final Testing and Sign-off

Included automated checks to evaluate the implementation.

The notebook reports the number of passed and failed checks and calculates the pass percentage.

The target is at least 80% passing checks, followed by manual verification of conversation memory, knowledge retrieval and unsupported questions.

## Files

- `Agentic_AI_Day5.ipynb` – Contains Day 5 concepts, VoltCare knowledge base creation, ChromaDB implementation, RAG search tool, LangGraph conversation memory, agent integration and testing.

## Technologies Used

Python, Google Colab, Groq API, LangChain, LangGraph, ChromaDB, embeddings, Pydantic and Google Sheets.

## Key Learnings

- Understood different types of memory used in AI agents.
- Learned how conversation memory works with checkpointers and thread IDs.
- Explored embeddings and vector databases.
- Learned how to store and retrieve knowledge using ChromaDB.
- Understood chunking and similarity search.
- Implemented a RAG-based knowledge retrieval tool.
- Integrated memory and knowledge retrieval into an existing AI agent.
- Learned how to reduce hallucinations through grounded responses.
- Tested conversation continuity and thread isolation.

## Outcome

Extended VoltCare AI into a more context-aware and knowledge-grounded EV customer and service assistant by integrating ChromaDB-based RAG, LangGraph conversation memory and existing Day 4 tools.
