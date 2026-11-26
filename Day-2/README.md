# Day 2 – Prompt Engineering, JSON and Python

**Date:** 24 November 2026

## Overview

Day 2 focused on improving LLM responses through prompt engineering, generating structured JSON output, maintaining conversation history, and using Python concepts in AI applications.

The concepts were practised through a Sweet Crumbs Home Bakery Assistant and an EV Customer & Service Assistant.

## Concepts Learned

### 1. Prompt Engineering

Prompt engineering is the process of writing clear instructions to guide an LLM towards the expected response.

Explored:
- **System Prompts:** Define the assistant's role, behaviour, rules and limitations.
- **Zero-Shot Prompting:** Asking the model to perform a task using instructions without examples.
- **Few-Shot Prompting:** Providing examples to guide the model's responses.

### 2. JSON – Structured Data

JSON (JavaScript Object Notation) is a structured format used to exchange information between applications.

Learned:
- Generating structured JSON responses from an LLM.
- Extracting required fields from JSON.
- Using `json.loads()` to convert JSON strings into Python dictionaries.
- Using `json.dumps()` to convert Python data into JSON strings.

### 3. Conversation History

Conversation history allows an assistant to use previous messages as context while responding to new questions.

### 4. Python Concepts

Practised Python concepts useful for AI application development:

- Dictionaries and functions.
- Type hints and docstrings.
- Decorators.
- Exception handling.
- Working with structured data.

## Practical Implementation

### 1. Sweet Crumbs Home Bakery Assistant

Worked on a customer-support assistant for a sample home bakery.

Implemented and explored:
- Defining the assistant's role through system prompts.
- Adding business information, rules and instructions.
- Experimenting with zero-shot and few-shot prompting.
- Extracting customer order information into JSON.
- Processing structured responses using Python.
- Maintaining conversation history.

### 2. EV Customer & Service Assistant

Worked on a separate EV service-related assistant using business-specific instructions.

The assistant was designed to handle customer enquiries about EV services and provide responses based on the supplied business information.

## Files

- `Agentic_AI_DAY-2.ipynb` – Day 2 workshop concepts and implementations.
- `EV_Service_Assistant.ipynb` – Additional practical work on the EV Customer & Service Assistant.

## Technologies Used

Python, Google Colab, Groq API, LangChain and JSON.

## Key Learnings

- Learned how to write effective system prompts.
- Understood zero-shot and few-shot prompting.
- Learned to generate and process JSON responses.
- Understood how conversation history provides context.
- Practised Python concepts used in AI applications.
- Applied prompt engineering to business-specific assistants.

## Outcome

Built and experimented with business-specific LLM assistants and learned how prompt engineering, JSON and Python work together in AI application development.