# Google AI Agents & Agentic Framework Learning Plan

This guide gives you a practical, project-first path to build **Google AI agents** and agentic systems.

## 1) What to Learn First (2 weeks)

- **Python fundamentals for AI apps**: async basics, APIs, virtual environments.
- **LLM fundamentals**: prompting, context windows, temperature/top-p, hallucination handling.
- **Google stack overview**:
  - Gemini API (prompting + multimodal)
  - Vertex AI (managed deployment)
  - Agent Development Kit (ADK)
  - Tool/function calling patterns
  - Retrieval-Augmented Generation (RAG)

## 2) Core Agent Building Blocks

1. **Planner**: decides what to do next.
2. **Tools**: external functions (search, database query, APIs).
3. **Memory**:
   - short-term conversation state
   - long-term store (vector DB / SQL)
4. **Retriever**: fetches relevant documents for grounded answers.
5. **Evaluator/Guardrails**: checks response quality and safety.
6. **Orchestrator**: runs multi-step workflows and retries.

## 3) Real-Time Project Track

Build these in order so each project reuses prior components.

### Project 1 — Support FAQ Agent (Beginner)

**Goal**: Build a Gemini-powered chat assistant for company FAQs with citations.

**Features**:
- Upload docs (PDF/Markdown)
- Ask questions in chat
- Return cited answers
- Basic fallback: “I don’t know from provided docs”

**Skills gained**:
- Prompt templates
- RAG basics
- Tool invocation

---

### Project 2 — Incident Triage Agent (Intermediate)

**Goal**: Agent that reads system alerts and suggests triage actions.

**Features**:
- Input: live alert text / logs
- Classify severity (P1/P2/P3)
- Propose runbook steps
- Generate summary for Slack/Email

**Skills gained**:
- Structured outputs (JSON schema)
- Agent policy prompts
- Error handling/retry design

---

### Project 3 — Multi-Agent Research Assistant (Intermediate+)

**Goal**: Build a small multi-agent system:
- **Researcher Agent** (finds sources)
- **Analyst Agent** (extracts insights)
- **Writer Agent** (creates final brief)

**Features**:
- Web/doc ingestion
- Source ranking
- Final report with confidence and citations

**Skills gained**:
- Multi-agent orchestration
- Task decomposition
- Quality evaluation loops

---

### Project 4 — Real-Time Ops Copilot (Advanced)

**Goal**: A production-style ops assistant for dashboards + tickets.

**Features**:
- Reads metrics/events in near real time
- Correlates anomalies with historical incidents
- Creates Jira/Linear tickets automatically
- Human-in-the-loop approval before critical actions

**Skills gained**:
- Event-driven architecture
- Tool permissions and safety boundaries
- Observability for agent behavior

## 4) Suggested Tech Stack (Google-centric)

- **Model/API**: Gemini API or Vertex AI Gemini models
- **Agent Framework**: Google ADK (Agent Development Kit)
- **Backend**: Python (FastAPI)
- **Memory/RAG**: Vector DB + document chunking pipeline
- **UI**: Streamlit / Next.js chat interface
- **Deployment**: Cloud Run (fast iteration), GKE (scale)
- **Monitoring**: request logs, traces, prompt/response audits

## 5) 30-Day Execution Plan

### Week 1
- Set up Gemini API + Python environment
- Build a simple tool-calling agent
- Add logging for every step

### Week 2
- Implement RAG pipeline
- Finish Project 1 end-to-end
- Add evaluation dataset (20–50 test questions)

### Week 3
- Build Project 2 with structured outputs and retries
- Add safety rules and refusal policy

### Week 4
- Start Project 3 (multi-agent)
- Add agent metrics:
  - response latency
  - tool-call success rate
  - factuality score (manual rubric)

## 6) Portfolio-Ready Deliverables

For each project, publish:
- Architecture diagram
- Short demo video (2–4 min)
- README with setup + sample prompts
- “What failed and how I improved it” section
- Benchmark table (before/after improvements)

## 7) Practical Tips

- Start with one agent + 1–2 tools before multi-agent designs.
- Keep prompts versioned in files; avoid hardcoding in scattered code.
- Log all tool calls and decisions for debugging.
- Add strict action policies for any write/delete operations.
- Use eval sets early; do not rely only on demo chats.

## 8) Next Step You Can Build Today

Build **Project 1** first:
1. Create an FAQ knowledge base from your own notes.
2. Build a Gemini chat endpoint.
3. Add retrieval and citations.
4. Deploy a minimal UI and share with 3 users for feedback.

---

If you follow this sequence, you will move from prompt-level apps to robust, production-style agentic systems with real project proof.
