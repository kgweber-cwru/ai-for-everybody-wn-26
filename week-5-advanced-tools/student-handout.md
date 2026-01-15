# Week 5: Grounded AI & Knowledge Agents
## Student Handout (2026 Update)

---

## 🧠 The Concept: Grounded AI (RAG - Retrieval-Augmented Generation)
In the first four weeks, we focused on how to *talk* to AI. This week, we focus on what the AI *knows*. In 2026, the most effective medical AI is "Grounded"—it is restricted to using only the sources you provide.

**What is RAG?**
- **Retrieval:** AI searches through YOUR documents
- **Augmented:** Uses that content to enhance its response
- **Generation:** Creates answers ONLY from your sources

**Why This Matters:**
- Prevents hallucinations (no making up facts)
- Ensures citations to specific sources
- Keeps AI answers within your knowledge domain
- Creates audit trail for verification

---

## 📚 Tool 1: NotebookLM (Google)
NotebookLM is a "research-first" tool. Unlike a standard chatbot, it builds a model of **your specific data**.

**2026 Features to Use:**
- **2-Million Token Window:** You can upload an entire library of medical journals (up to 50 sources, each up to 500k words).
- **Interactive Audio Overviews:** Generate a "podcast" of your research, then interrupt the hosts to ask for more detail on a specific data point.
- **Direct Citation:** Every answer includes a blue number. Clicking it opens the exact page and paragraph used to generate that answer.

---

## 🤖 Tool 2: Custom GPTs (OpenAI)
Custom GPTs are best for **repetitive workflows**. If you find yourself pasting the same instructions every day, you should build a GPT.

**The Architecture of a GPT:**
1. **Instructions:** The "System Prompt" that defines its personality and limits.
2. **Knowledge Base:** Files the GPT "knows" (e.g., your lab’s specific SOPs).
3. **Capabilities:** Can it browse the web? Can it generate images (DALL-E 3)?4. **Actions (Advanced):** Can connect to external tools via API

**NotebookLM vs Custom GPT - When to Use Which?**

| Feature | NotebookLM | Custom GPT |
|---------|------------|------------|
| **Best For** | Research & analysis | Repetitive workflows |
| **Source Limit** | 50 sources, 500k words each | Knowledge base less flexible |
| **Citations** | Excellent (page-level) | Basic (file-level) |
| **Audio Overviews** | Yes (podcast generation) | No |
| **Custom Instructions** | Limited | Fully customizable |
| **Web Access** | No | Optional |
| **Sharing** | Link sharing | Public or private |
| **Cost** | Free | Free tier + paid options |

**Pro Tip:** Use NotebookLM for discovery and analysis, then build a Custom GPT for recurring tasks based on what you learned.
---

## 🧪 Seminar Activity: Building the "Department Brain"
**Goal:** Use Grounded AI to find contradictions in clinical guidance.

1. **Upload:** Gather 2-3 different clinical guidelines for the same condition (e.g., an AHA guideline vs. a European Society of Cardiology guideline).
2. **Grounding:** Upload them to a new notebook at [notebooklm.google.com](https://notebooklm.google.com).
3. **The Query:** Use this prompt:
   > "Compare these guidelines. Identify three specific areas where the recommendations (dosages, timelines, or diagnostic criteria) differ. Create a table of these contradictions."
4. **The Audit:** Click the citations to verify that the AI didn't misinterpret the data.

---

## 🏠 Take-Home Assignment: The "Clinical Protocol Agent"
**Task:** Design your own Knowledge Agent for a task you do weekly.

**Option A (NotebookLM):**
- Create a notebook containing your 5 most-referenced research papers or protocols.
- Generate a 5-minute Audio Overview.
- Listen to it and note one "connection" the AI made between the papers that you hadn't considered.

**Option B (Custom GPT):**
- Plan an agent that helps with a specific admin task (e.g., "The Grant Formatting Assistant" or "The Patient Hand-off Summarizer").
- Write the **System Instructions** using the **Five Pillars** (Role, Context, Task, Constraints, Thought Process) from Week 3.

---

## 📅 Looking Ahead: The Grand Finale
**Next Week:** We tie it all together. You will learn to **Orchestrate**—moving data from a Reasoning Model to a Knowledge Agent to a Final Document. You will leave with a personalized **"2026 AI Workflow Map."**