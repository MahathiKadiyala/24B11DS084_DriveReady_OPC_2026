# Day 3 – Building Your First AI Agent

**Date:** 25 November 2026

## Overview

Day 3 introduced AI agents and explained how they differ from traditional chatbots and basic LLM applications.

I explored the components of an AI agent, the agent loop, and LangChain building blocks. I also developed and tested business-specific assistants and experimented with Python functions that can later be used as agent tools.

## Concepts Learned

### 1. Chatbot vs AI Agent

A chatbot mainly responds to user messages, whereas an AI agent can work towards a goal by making decisions and using tools.

### 2. Four Main Components of an AI Agent

- **Brain:** The LLM that understands tasks and helps make decisions.
- **Instructions:** Define the agent's role, goals and rules.
- **Tools:** Allow the agent to perform specific operations.
- **Memory:** Provides relevant information from previous interactions.

### 3. Agent Loop

Learned the basic working cycle:

**Think → Act → Observe → Repeat**

The agent understands a task, performs an action, observes the result and decides what to do next.

### 4. Three Levels of AI

Explored:
- Traditional AI.
- Generative AI.
- Agentic AI.

### 5. Choosing Between Code, LLM and Agent

- **Plain Code:** Suitable for fixed and predictable tasks.
- **LLM:** Suitable for understanding, generating and classifying text.
- **AI Agent:** Suitable for tasks involving decisions, multiple steps and tool usage.

### 6. LangChain Basics

Explored the following LangChain components:

- **Model:** Connects the application to an LLM.
- **Prompt Template:** Organises instructions and user inputs.
- **Chain:** Connects components into an application workflow.
- **Agent:** Uses an LLM to decide how to handle tasks and interact with available tools.

## Practical Implementation

### 1. Sweet Crumbs Home Bakery Assistant

Built an LLM-powered bakery assistant using LangChain.

Implemented:
- Connected the Groq model using `ChatGroq`.
- Created prompts using `ChatPromptTemplate`.
- Used `MessagesPlaceholder` to include conversation history.
- Used `StrOutputParser` to process model responses.
- Created a reusable `ask()` function for customer queries.

### 2. Testing and Prompt Improvement

Created a `tests.csv` file containing customer questions and expected keywords.

Implemented a test runner to:
- Read test cases from the CSV file.
- Generate assistant responses.
- Check expected keywords.
- Display PASS/FAIL results and the overall pass rate.

**Testing results:**

| Stage | Result |
|---|---:|
| Initial prompt | 2/5 (40%) |
| Improved prompt | 5/5 (100%) |

The checks were keyword-based, so the pass rate does not guarantee complete response correctness.

### 3. LangChain Agent Preview

Explored `create_agent` to understand the basic structure of a LangChain agent.

The preview used an empty tool list (`tools=[]`), helping me understand the agent setup before learning actual tool integration.

### 4. EV Customer & Service Assistant

Extended my EV service assistant practice by preparing customer questions and evaluating its responses.

Implemented:
- Created 10 EV customer questions in `ev_tests.csv`.
- Built a test runner to evaluate responses.
- Improved the assistant's prompt based on test results.
- Experimented with temperature `1.0` and compared responses.
- Classified example tasks into code, LLM or agent-based approaches.

### 5. Python Functions for EV Service Operations

Created two reusable Python functions as basic building blocks for future agent tools.

**`get_service_price(service_type)`**

Returns sample price information for supported EV services.

Example:

```python
get_service_price("battery_check")
```

Output:

```text
Estimated service price: Rs 800
```

**`check_service_availability(service_type)`**

Checks whether a service type is supported for an appointment enquiry.

Example:

```python
check_service_availability("general_service")
```

Output:

```text
Service enquiry accepted. Appointment availability must be confirmed by the service team.
```

These functions use sample data. They do not retrieve live service prices or confirm actual appointment slots.

## Files

- `Agentic_AI_DAY-3.ipynb` – Day 3 concepts, LangChain implementation and practical exercises.
- `ev_tests.csv` – EV customer questions used for assistant testing.
- `tests.csv` – Bakery assistant test cases.

## Technologies Used

Python, Google Colab, Groq API, LangChain and CSV.

## Key Learnings

- Understood the difference between chatbots and AI agents.
- Learned the four main components and working cycle of an agent.
- Explored LangChain models, prompt templates, chains and agents.
- Learned how to evaluate and improve LLM responses.
- Practised temperature experimentation.
- Created reusable Python functions for EV service operations.
- Understood how functions can become tools for AI agents.

## Outcome

Built and tested LLM-powered business assistants, explored the basic structure of an AI agent, and prepared Python functions for future tool integration.