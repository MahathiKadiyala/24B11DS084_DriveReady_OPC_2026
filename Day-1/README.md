# Day 1 – Introduction to LLMs

**Date:** 23 November 2026  
**Topic:** How LLMs Work and Your First API Call

## Overview

Day 1 introduced Large Language Models (LLMs), their basic working, and how to interact with them through an API. I learned how to connect an LLM to Python using the Groq API and explored LangChain for building AI-powered applications.

## Concepts Learned

### 1. Large Language Models (LLMs)
LLMs are AI models trained on large amounts of text data. They understand user prompts and generate responses based on the input and context provided.

### 2. Message Roles
Learned the basic message structure used in LLM applications:
- **System:** Defines the assistant's role and behaviour.
- **User:** Contains the user's question or input.
- **Assistant:** Contains the model-generated response.

### 3. Groq API
Groq provides API access to language models. It allows Python applications to send prompts and receive generated responses.

### 4. LangChain and ChatGroq
Explored LangChain as a framework for building LLM applications and `ChatGroq` for connecting LangChain with models available through Groq.

## Practical Implementation

Worked in Google Colab to:

- Install and import the required Python libraries.
- Configure the Groq API key using Colab Secrets.
- Connect to an LLM using `ChatGroq`.
- Send prompts and receive model-generated responses.
- Build a basic LLM-powered assistant.

## Files

- `Agentic_AI_DAY-1.ipynb` – Colab notebook containing the Day 1 concepts, API setup and practical implementation.

## Technologies Used

Python, Google Colab, Groq API and LangChain.

## Key Learnings

- Understood the basic working of LLMs.
- Learned how system, user and assistant messages are used.
- Understood API key configuration and model interaction.
- Made my first LLM API call using Python.

## Outcome

Successfully connected to an LLM through the Groq API and built the foundation for developing AI-powered applications.