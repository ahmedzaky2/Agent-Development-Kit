# 🔍 AI Agent Project using Google's Agent Development Kit (ADK)

This project showcases the development of two AI agents built using the **Agent Development Kit (ADK)** by Google. ADK is a modular and flexible framework for developing intelligent agents that integrate tightly with the Google ecosystem, especially Gemini models.

## 🚀 About Agent Development Kit (ADK)

**Agent Development Kit (ADK)** is a framework from Google designed to simplify the development and deployment of AI agents. It supports:

- Tight integration with **Gemini models** and Google AI tools.
- Support for popular LLMs and open-source generative tools.
- Modular architecture to build simple or complex agents.
- Tool-based orchestration and extensibility.

Learn more about ADK on [Google's official documentation](https://developers.google.com/).

---

## 🤖 Project Overview

This project includes **two AI agents**, each designed with a specific purpose and demonstrating key ADK functionalities.

### 1. 🌤️ Weather & Time Agent

An AI agent that provides:
- **Current weather reports** (currently supports New York).
- **Current time** based on city and timezone info (currently supports New York).

#### 🛠️ Tools/Functions Used

```python
def get_weather(city: str) -> dict:
    ...
    
def get_current_time(city: str) -> dict:
    ...

✅ Example Capabilities
"What’s the weather in New York?" → Returns weather report.

"What time is it in New York?" → Returns current time with timezone info.


2. 🔎 Basic Search Agent
An AI agent that uses Google Search to answer user questions with factual, grounded responses.

🧠 Agent Configuration
python
Copy
Edit
root_agent = Agent(
    name="basic_search_agent",
    model="gemini-2.0-flash-exp",
    description="Agent to answer questions using Google Search.",
    instruction="You are an expert researcher. You always stick to the facts.",
    tools=[google_search]
)
✅ Example Capabilities
"Who won the last FIFA World Cup?" → Agent will search Google and respond with accurate, up-to-date info.

"What are the health benefits of green tea?" → Returns grounded response from the web.