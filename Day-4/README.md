# Day 4 – Tools, Pydantic and Google Sheets

**Date:** 26 November 2026

## Overview

Day 4 focused on extending AI agents with tools, structured output and external integrations.

I learned how agents use function calling, how to create tools using LangChain, how to handle errors, and how to extract structured information using Pydantic. I also integrated Google Sheets with VoltCare AI to store customer enquiries.

## Concepts Learned

### 1. Why Agents Need Tools
- How tools extend an agent's capabilities.
- How agents use function calling to perform tasks.

### 2. Writing Good Tools
- Creating LangChain tools using `@tool`.
- Understanding tool names, descriptions and parameters.

### 3. Agents with Tools
- Using `create_agent()` to build tool-using agents.
- Understanding how agents select and invoke tools.

### 4. Error Handling and Rate Limits
- Handling API rate limits.
- Managing tool execution errors and exceptions.

### 5. Pydantic Structured Output
- Creating Pydantic models.
- Extracting and validating structured customer information.

### 6. Google Sheets Integration
- Connecting Google Colab with Google Sheets using `gspread`.
- Authenticating and accessing spreadsheets.
- Saving customer enquiries permanently.

## Practical Implementation

### 1. VoltCare AI Agent
Built an EV customer service agent using Groq and LangChain.

Implemented:
- Initialized the Groq model using `ChatGroq`.
- Created an agent using `create_agent()`.
- Integrated Python functions as tools.
- Tested EV service-related customer queries.

### 2. Pydantic and Structured Output
- Created an `EVServiceEnquiry` model.
- Extracted structured information from customer messages.
- Tested five different customer messages.

### 3. Customer Enquiry Logging
- Created a `log_service_enquiry()` tool.
- Experimented with temporary Python-list storage.
- Integrated enquiry logging with Google Sheets.

### 4. Tool Experiments and Agent Traces
- Experimented with poor tool naming.
- Inspected agent execution traces.
- Counted AI messages and tool calls.

### 5. Google Sheets Integration
- Connected Google Colab with Google Sheets.
- Used `gspread` to insert customer enquiries.
- Verified actual enquiry records in the spreadsheet.

### 6. Day 5 Preparation
Prepared 20 EV business facts for the upcoming Memory and RAG session.

## Files

- `Agentic_AI_DAY-4.ipynb` – Contains Day 4 concepts, LangChain tools, VoltCare AI implementation, Pydantic structured output, enquiry logging, agent trace experiments and Google Sheets integration.

## Technologies Used

Python, Google Colab, Groq API, LangChain, Pydantic, Google Sheets, gspread and google-auth.

## Key Learnings

- Learned how AI agents use tools and function calling.
- Created and integrated LangChain tools.
- Built a tool-using AI agent.
- Learned structured data extraction using Pydantic.
- Explored error handling and agent traces.
- Integrated Google Sheets for permanent enquiry storage.

## Outcome

Built **VoltCare AI**, an EV customer service agent that uses tools, extracts structured customer enquiries using Pydantic and stores enquiry records permanently in Google Sheets.
