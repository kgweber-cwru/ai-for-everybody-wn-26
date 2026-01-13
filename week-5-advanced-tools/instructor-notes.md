# Week 5: Knowledge Agents & Grounded AI
## Instructor Notes (2026 Updated)

---

### Slide 1: Beyond the Chatbox
**Title:** From Assistant to Agent: Building Your Personal Knowledge Base
**Context:** We are moving away from "General Knowledge" (which hallucinates) to "Grounded Knowledge" (which stays within your documents).

**Speaker Notes:**
- Review Week 4: How did the "Red Team" audit go? Did anyone catch a reasoning error?
- Today’s goal: Stop asking the internet; start asking your own library.

---

### Slide 2: What is "Grounded" AI?
**Concept:** Reducing hallucinations by limiting the AI's "world" to your uploaded files.
- **RAG (Retrieval-Augmented Generation):** The technical term for when an AI looks at your PDFs before answering.
- **Why it matters in Medicine:** It ensures the AI follows *your* department's SOPs or *your* specific research papers, not a random blog post from 2021.

---

### Slide 3: NotebookLM (The Scholar's Tool)
**Concept:** A "Source-First" environment.
- **2026 Update:** Gemini 3 Pro integration allows for **2-million-token windows** (approx. 2,000 research papers in one notebook).
- **The "Deep Dive" Audio:** Audio overviews are now interactive—you can "join the conversation" with the AI hosts to ask follow-up questions.

---

### Slide 4: Custom GPTs & "Agentic" Workflows
**Concept:** Building a specialized colleague for repetitive tasks.
- **Identity:** Giving the GPT a narrow "System Prompt" (e.g., "You are an IRB Compliance Officer").
- **Actions:** In 2026, GPTs can connect to your Outlook or Calendar to schedule follow-ups based on the documents you analyze.

---

### Slide 5: The "Department Brain" Demo (10 Mins)
**Instructor Action:** Show a NotebookLM populated with 5-10 conflicting medical papers.
1. Ask for a **"Summary of Conflicts"** (finding where papers disagree).
2. Generate an **Audio Overview**.
3. Show the **Citations**: Click a citation to show the exact highlight in the PDF.

---

### Slide 6: The "Agent Lab" (30 Mins)
**Interactive Exercise:**
- **Step 1:** Students choose 3 PDFs related to their specific medical niche.
- **Step 2:** Upload to NotebookLM.
- **Step 3:** Perform the **"Guideline Reconciliation"** task (Instruction: "Find where these three documents provide different advice for the same condition").

---

### Slide 7: Wrap-Up & Implementation
- **Homework:** Build a "Clinical Protocol Agent."
- **Preview Week 6:** Orchestration—how to use Weeks 1-5 together to build a complete 2026 workflow.

---

## Teaching Tips
- **Stability Check:** Ensure everyone can log into `notebooklm.google.com` early.
- **The "Citation" Focus:** Repeatedly show students that if there is no citation, the answer might be a hallucination. In grounded AI, no citation = no trust.