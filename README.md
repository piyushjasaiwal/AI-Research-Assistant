# 🔧 AI Research Assistant with Web Search + Memory

## 🧠 Overview

This project is an AI-powered research assistant designed to intelligently respond to user queries using both memory and real-time web search.

### What It Does

- Users ask questions or start a topic (e.g., “Explain diffusion models in AI”).
- The assistant first checks if it has prior knowledge (from memory).
- If not, it uses the **TavilySearch** tool to fetch up-to-date information from the web.
- It summarizes the results and stores them in memory for future use.

---

## 📦 Components Used

| Component                  | Purpose                                              |
|---------------------------|------------------------------------------------------|
| **StateGraph**             | Manages the conversation flow                       |
| **Node: LLM Agent**        | Determines whether to answer, search, or clarify    |
| **Node: Tool Call (TavilySearch)** | Performs real-time web search                   |
| **Conditional Routing**    | Decides whether to use the search tool or memory   |
| **Memory** (File or Vector Store) | Stores and retrieves past responses            |

---

## 🔁 Sample Conversation Flow

**User:**  
> "What's LangGraph used for?"

**Agent:**
1. Checks memory → *Not found*
2. Calls TavilySearch tool
3. Tool result: *"LangGraph is used for..."*
4. Agent summarizes and stores the response
5. Next time, it responds instantly from memory
