# ✈️ AI Trip Planner (Agent + LLM Modes)

An interactive AI-powered trip planner built using **Gradio + LangChain + Groq**, supporting both **direct LLM generation** and **agent-assisted planning with live search**.

---

## 🚀 Demo

![Demo](assets/demo.gif)

> DEMO

---

## ✨ Features

### ⚡ No-Agent Mode (Fast LLM)
- Direct itinerary generation using LLM
- Real-time streaming output
- Simple and fast

### 🤖 Agent Mode (Tool-Assisted)
- Uses live **flight search (SerpAPI)**
- Controlled tool execution (no duplicate calls)
- Clean progress tracking
- Final LLM-based itinerary synthesis

---

## 🎯 Key Capabilities

- Budget-aware trip planning
- Travel-style personalization (Family, Luxury, Adventure, etc.)
- Supports preferences like:
  - Toddler-friendly travel
  - Vegetarian-friendly options
- Structured output:
  - ✈️ Flights
  - 🏨 Hotels
  - 🍽️ Activities & food
  - 📅 Day-by-day itinerary
  - 💰 Budget summary

---

## 🧠 Architecture
# ✈️ AI Trip Planner (Agent + LLM Modes)

An interactive AI-powered trip planner built using **Gradio + LangChain + Groq**, supporting both **direct LLM generation** and **agent-assisted planning with live search**.

---

## 🚀 Demo

![Demo](assets/demo.gif)

> Add your demo GIF here (recommended: 10–15 seconds, <10MB)

---

## ✨ Features

### ⚡ No-Agent Mode (Fast LLM)
- Direct itinerary generation using LLM
- Real-time streaming output
- Simple and fast

### 🤖 Agent Mode (Tool-Assisted)
- Uses live **flight search (SerpAPI)**
- Controlled tool execution (no duplicate calls)
- Clean progress tracking
- Final LLM-based itinerary synthesis

---

## 🎯 Key Capabilities

- Budget-aware trip planning
- Travel-style personalization (Family, Luxury, Adventure, etc.)
- Supports preferences like:
  - Toddler-friendly travel
  - Vegetarian-friendly options
- Structured output:
  - ✈️ Flights
  - 🏨 Hotels
  - 🍽️ Activities & food
  - 📅 Day-by-day itinerary
  - 💰 Budget summary

---

## 🧠 Architecture
User Input
↓
Mode Selection
↓
├── No-Agent Mode
│ → PromptTemplate → LLM → Streaming Output
│
└── Agent Mode
→ Flight Search (SerpAPI)
→ LLM Synthesis
→ Final Itinerary


---

## ⚙️ Tech Stack

- 🧠 LLM: Groq (`langchain_groq`)
- 🔗 Framework: LangChain
- 🌐 Search: SerpAPI
- 🎨 UI: Gradio
- 🐍 Language: Python

---

## 📦 Installation

```bash
pip install -U gradio langchain-core langchain-groq langchain-community google-search-results
```
### 🔐 Environment Setup

Set your API keys (Colab secrets or environment variables):

GROQ_API_KEY=your_groq_api_key
SERPAPI_API_KEY=your_serpapi_key
### ▶️ Run the App
demo.launch()
#### 🧪 How It Works
🔹 No-Agent Mode
##### Builds a structured prompt
##### Streams response directly from LLM
##### No external tool calls
🔹 Agent Mode
##### Uses flight search tool once
##### Avoids repeated tool loops
##### Uses  LLM to synthesize final itinerary

###🛠️ Challenges Solved
❌ Prevented repeated / infinite agent tool calls
⚡ Clean separation of streaming vs final rendering
🎯 Deterministic tool orchestration
🧹 Removed noisy agent logs for better UX
###📌 Future Improvements
Parallel tool execution (flights + hotels + activities)
Smarter budget optimization
Save/share itineraries
Multi-city planning
Calendar export integration
📣 Author
Ravi K Sharma
Senior Principal Software Engineer
AI Systems | Distributed Systems
