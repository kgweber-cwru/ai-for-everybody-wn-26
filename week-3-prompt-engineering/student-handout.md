# Week 3: Prompt Engineering Fundamentals
## Student Handout (Updated Jan 2026)

---

## The Core Principle: Steering the Logic
In 2026, we don't just "chat" with AI; we **direct logic**. Because models like GPT-5 and Claude 4 now "think" before they speak, your prompt is the map for that thought process.

### The Five Pillars of a Great Prompt
1. **ROLE:** Give the AI an identity (e.g., "You are a Senior NIH Grant Reviewer").
2. **CONTEXT:** What is the background? (e.g., "We are reviewing a 500-page trial report").
3. **TASK:** Use an action verb (e.g., "Extract," "Synthesize," "Critique").
4. **CONSTRAINTS:** Set the boundaries (e.g., "Do not use jargon," "Max 5 bullet points").
5. **THOUGHT PROCESS:** For reasoning models, tell it *how* to think (e.g., "Compare the methodology against established Delphi standards before concluding").

---

## New for 2026: Prompting "Reasoning" Models
When using **Reasoning Models** (GPT-5, Gemini 3 Pro), prompts should be more goal-oriented:
* **The "Pause" Prompt:** "Take your time to reason through the ethical implications of this study before providing a summary."
* **Chain of Thought (CoT):** Explicitly add "Let's think through this step-by-step" to the end of complex logic requests.

---

## Handling "Massive Context" (1M+ Tokens)
When you upload a 200-page PDF or a 1-hour video to Gemini 3 or GPT-4.1, use **Delimiters** to help the AI navigate:
* Use `###` or `---` to separate your instructions from the data.
* **Example:**
  > "Using the data provided between the `[DATA]` tags below, identify three conflicting findings."

---

## Hands-On: The "Prompt Lab" (In-Class)
**Scenario:** You need to explain the "SleepFM" model (from our video) to a patient who has no medical background.

**Task 1: The "Lazy" Prompt**
* Prompt: "Explain SleepFM to a patient."
* *Observe:* Is it too technical? Too long?

**Task 2: The "Engineered" Prompt**
* Prompt: "You are a compassionate Sleep Specialist. Using the concepts of 'leave-one-out learning' from the provided video, explain to a patient why this AI helps predict their heart risk. Use a cooking analogy. Keep it under 100 words."
* *Observe:* How does the quality change?

---

## Take-Home Assignment: The "Stress Test"
**Part A: Create a Prompt Library**
Create 3 "Production-Ready" prompts for your daily work. 
1. **A Data Task:** (e.g., Summarizing clinical notes)
2. **A Creative Task:** (e.g., Drafting a department newsletter)
3. **A Logic Task:** (e.g., Finding a flaw in a research methodology)

**Part B: Test & Refine**
* Run each prompt and evaluate the output
* Document what works and what doesn't
* Iterate at least once on each prompt
* Save both the original and refined versions

**Part C: Comparison (Bonus)**
Run your "Logic Task" prompt through a **Predictive model** (GPT-4o) and a **Reasoning model** (GPT-5 or Gemini Thinking). 
* Did the reasoning model catch something the predictive one missed?
* How much "thinking time" did the reasoning model take?
* Which model was better suited for your task?

**Part D: Build Your Library**
* Save your refined prompts in a reusable format
* For each prompt, document: Purpose, Full text, What works well, Sample outputs
* Bring your library to next week's session!

---

## 💡 Key Takeaways

**The Five Pillars:**
1. **ROLE** - Who is the AI?
2. **CONTEXT** - What's the situation?
3. **TASK** - What specific action?
4. **CONSTRAINTS** - What are the boundaries?
5. **THOUGHT PROCESS** - How should AI reason? ⭐

**Best Practices:**
- ROLE and CONSTRAINTS are your most powerful tools
- Reasoning models need "permission" to think
- Use delimiters (###, ---) for large documents
- Iterate - first prompt is rarely your best prompt
- Build a library for recurring tasks

**Model-Specific Tips:**
- **GPT-5:** Add "Take your time to reason through this"
- **GPT-4o:** Add "Provide a concise answer"
- **Claude:** Add "Consider multiple perspectives"
- **Gemini:** Add "Reference specific sections of the provided document"

---