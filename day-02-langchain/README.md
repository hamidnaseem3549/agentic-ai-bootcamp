# Day 02 — LangChain Essentials

**Bootcamp:** Agentic AI Engineering & Automation  
**Venue:** FAST-NUCES Islamabad, AIM LAB  
**Format:** Practical hands-on session using Google Colab

---

## What this day covered
Complete hands-on introduction to LangChain — from the 
simplest possible chain all the way to agents that 
dynamically decide which tools to use. Worked entirely 
in Google Colab using a structured notebook.

---

## Core concepts learned

### 1. LCEL — The Pipe Operator |
The fundamental syntax of LangChain. Connects components 
left to right. Data flows through each step automatically.
```python
chain = prompt | llm | StrOutputParser()
```
This single pattern is the foundation of every LangChain 
application ever built.

### 2. PromptTemplate — Two versions
**from_template()** — simple single message with placeholder:
```python
prompt = ChatPromptTemplate.from_template("Explain {topic}")
```
**from_messages()** — system + human roles:
```python
prompt = ChatPromptTemplate.from_messages([
    ("system", "You are a concise tutor."),
    ("human", "Explain {topic} in simple words.")
])
```
System = sets AI behaviour. Human = the actual question.

### 3. Prompting Strategies
**Chain of Thought (CoT):** Tell LLM to think step by step 
before answering. Same chain, smarter system prompt.

**Tree of Thought (ToT):** Ask LLM to generate 3 solution 
paths, compare them, then pick the best. Better for complex 
decisions.

Key insight: CoT and ToT are just prompt engineering — 
the chain structure stays identical.

### 4. Multi-Step Chain
Two LLM calls connected together:
- Step 1: Clarify the messy user question
- Step 2: Answer the now-clean question

**RunnablePassthrough** — passes data unchanged between steps  
**Lambda** — reformats output of one step into input format 
for the next step

### 5. Tools — @tool decorator
Turns any Python function into something an LLM can call:
```python
@tool
def multiply(a: int, b: int) -> int:
    """Multiply two integers a and b."""
    return a * b
```
The LLM reads the function name + docstring to understand 
what the tool does and when to use it.
Critical rule: Write clear docstrings — bad docstrings 
make agents choose wrong tools.

### 6. Agents vs Chains
| | Chain | Agent |
|--|-------|-------|
| Who decides flow? | You (developer) | The LLM |
| Tool use | Fixed order | Dynamic |
| Speed | Faster | Slower |
| Use when | Flow is predictable | LLM needs to decide |

### 7. Router Pattern
Classifies query first → routes to chain (simple) or 
agent (needs tools). Best of both worlds.
```python
if "simple" in decision.lower():
    return single_step_chain.invoke(...)
else:
    return ask_agent(query)
```

---

## Files in this folder
| File | Description |
|------|-------------|
| `LangChain_updated.ipynb` | Full session notebook — all 7 patterns practiced |


---


## The most important thing I learned today
Chain = I decide the order of execution.  
Agent = the LLM decides the order of execution.  
This single distinction is the foundation of everything 
in agentic AI engineering.

---


## Resources
- [LangChain Python Docs](https://python.langchain.com)
- [Groq Console](https://console.groq.com)
- [LCEL Reference](https://python.langchain.com/docs/expression_language/)

---

*Day 2 of 10 — Agentic AI Engineering Bootcamp*  
*FAST-NUCES Islamabad | AIM LAB | June 2026*
