# Day 01 — Introduction to Agentic AI & the Modern AI Landscape

**Bootcamp:** Agentic AI Engineering & Automation  
**Venue:** FAST-NUCES Islamabad, AIM LAB  
**Format:** Conceptual session — slides, live demos, 
interactive activities

---

## What this day covered
A foundational session covering the full evolution of AI —
from rule-based systems to modern Agentic AI. Focused on 
building the mental model of what agents are, how they 
think, and where they're applied in the real world.

---

## Part 1 — Evolution of AI

The session traced AI's evolution across 5 stages:

### 1. Rule-Based Systems
Manual IF/THEN logic. No learning. Completely rigid.  
Real example: ATM PIN check — IF pin correct → allow, 
ELSE → block.  
Limitation: Can't handle anything outside the programmed 
rules.

### 2. Machine Learning (ML)
Learns patterns from data and improves over time.  
Real example: Gmail spam filter — learns what spam looks 
like from thousands of emails.  
Upgrade from rules: doesn't need manual programming for 
every case.

### 3. Deep Learning (DL)
Neural networks that handle vision, speech, and language.  
Real example: Face unlock on your phone.  
Upgrade from ML: handles unstructured data (images, 
audio, video).

### 4. Large Language Models (LLMs)
Understand language, follow instructions, reason 
step-by-step.  
Real example: ChatGPT writing emails, summarizing PDFs.  
Upgrade from DL: natural language interface, instruction 
following, reasoning.

### 5. Agentic AI
Autonomous systems that plan, act, and adapt.  
Real example: An AI that compares flights, books tickets, 
emails HR, and updates your calendar — all from one goal.  
Upgrade from LLMs: doesn't just respond, it takes action.

**The key insight:**
Rule-Based → ML → DL → LLMs → Agentic AI

Each level adds: learning → perception → language → autonomy



---

## Part 2 — Traditional AI vs Agentic AI

| | Traditional AI (Chatbot) | Agentic AI |
|--|--------------------------|------------|
| Responds to | What you ask | Your goal |
| Planning | ❌ None | ✅ Breaks into steps |
| Tool usage | ❌ None | ✅ Calendar, browser, APIs |
| Memory | ❌ No cross-step memory | ✅ Remembers context |
| Self-correction | ❌ Cannot retry | ✅ Retries when failed |
| Duration | Short single response | Long multi-step task |

**Example that made this clear:**  
Chatbot: "What are budget meals?" → gives a list. Done.  
Agent: "Help me eat healthy on a budget" → checks 
schedule, plans weekly meals, creates shopping list, 
sets reminders.

---

## Part 3 — The 4 Core Components of an Agent

Every intelligent agent has these 4 components working 
in a loop:

### 1. Perception — Understanding the input
What the agent reads and interprets:
- Text (emails, chats, documents)
- Data (tables, logs, numbers)  
- User instructions (prompts)
- API responses (live signals — weather, maps)
- File contents (uploaded CVs, PDFs)

**Activity example:** "Remind me to submit the tax form 
before Friday. Also check if last year's form is on my 
laptop."  
Agent perceives: deadline (Friday), task type (reminder), 
secondary task (file search), urgency level.

### 2. Planning — Breaking the goal into steps
Agent asks internally:
- What is the goal?
- What steps are needed?
- What order should they run in?
- Which tool is needed at each step?

**Example:** "Make a study plan for my exams next month"  
Plan: identify subjects → evaluate timeline → divide 
syllabus into weekly chunks → add to calendar → set 
revision reminders.

### 3. Action Execution — Doing each planned step
Agent decides:
- Which tool to call right now
- What data to send to that tool
- How to handle errors or missing info
- When to retry or move to next step

**Example:** Posting a LinkedIn update → selects API → 
generates request → if tag invalid, fetches correct ID → 
if rate limited, waits and retries → on success, moves 
to next step.

### 4. Feedback Loop — Checking results
After every action the agent checks:
- Did the action succeed?
- Does the result match expectations?
- Are additional steps needed?
- Should a different tool be used?

This enables **self-correction** — the most powerful 
property of an agent.

---

## Part 4 — Real-World Agent Applications

### Customer Service Agent
Perception → reads and classifies the message  
Planning → decides to reply, escalate, or fetch info  
Action → pulls data from CRM, prepares response  
Feedback → checks if response is complete  
Outcome → customer receives accurate, quick support

### Document Automation Agent
Perception → understands document structure  
Planning → decides how to extract fields  
Action → reads files, extracts data, formats output  
Feedback → validates extracted fields, retries errors  
Outcome → automated workflows with high accuracy

### Sectors covered
- **Governance:** document routing, citizen requests, 
  compliance tasks
- **Education:** attendance, grading, student queries, 
  lecture note generation
- **Healthcare:** patient note summarization, medical 
  history processing, admin workflows
- **Business:** customer service, document processing, 
  workflow automation

---

## Part 5 — The 4R Method: Identifying Agent Opportunities

A task is a good candidate for an agent if it meets 
2-3 of these:

| R | Meaning | Example |
|---|---------|---------|
| **Repeatable** | Happens daily/weekly | CI/CD pipeline runs every push |
| **Rules-Based** | Clear steps or criteria | Jira ticket → QA → regression tests → notify |
| **Routine** | Doesn't need creativity | Daily standup summary from Slack/Git |
| **Resource-Heavy** | Takes significant staff time | Manually scanning logs after deployment |

---

## Key distinctions I need to remember

**AI ≠ Robots**  
AI = Decision-making software. Robots are physical 
machines. They can use AI but AI alone is not a robot.

**Chatbot ≠ Agent**  
Chatbot responds. Agent acts. The difference is autonomy, 
planning, and tool usage.

**LLM ≠ Agent**  
LLM is the brain. Agent is the complete system — 
perception + planning + action + feedback — that uses 
the LLM to reason.

---


## The most important thing I learned today
Agentic AI is not a smarter chatbot. It's a fundamentally 
different architecture — one that perceives goals, 
plans multi-step workflows, executes actions using tools, 
and self-corrects based on feedback. The shift from 
"responding to prompts" to "achieving goals" is what 
makes it powerful.

---

*Day 1 of 10 — Agentic AI Engineering Bootcamp*  
*FAST-NUCES Islamabad | AIM LAB | June 2026*
