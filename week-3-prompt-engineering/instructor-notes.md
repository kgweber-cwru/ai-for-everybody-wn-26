# Week 3: Prompt Engineering Fundamentals
## Instructor Notes (Updated Jan 2026)
### Slide 1: Title & Welcome Back
Title: Prompt Engineering Fundamentals: Moving from Chatting to Directing

Week 3 of 6

Quick Check-In:

From Week 2, who tried a "Reasoning" model (GPT-5) vs. a "Predictive" model (GPT-4o)?

Did anyone notice the "Thinking" pause?

Did the reasoning model change how you felt about the accuracy of the answer?

Speaker Notes:

Acknowledge that in 2026, prompting isn't just about "words"—it's about managing the AI's "internal logic."

### Slide 2: Today's Goals
Master the Five Pillars of 2026 Prompting.

Learn to "Direct" reasoning-heavy models (GPT-5, Claude 4).

Understand Context Stuffing: How to prompt inside 1M+ token windows.

Practice the "Lazy vs. Engineered" workflow.

### Slide 3: What is Prompt Engineering in 2026?
Definition: The systematic design of instructions to align an AI’s logic with your desired outcome.

Why the "Engineering" part matters now:

Context is King: With 2-million-token windows (Gemini 3), the prompt is the "search query" for the massive data you just uploaded.

Reasoning Costs Time: Good prompts help the model reason efficiently, reducing "hallucinations in thought."

Consistency: Professional-grade prompting ensures the AI doesn't drift off-task during long operations.

### Slide 4: The Five Pillars of a Modern Prompt
1. ROLE (The Persona)

Don't just ask for an answer; ask for an expert.

Ex: "You are a Senior NIH Grant Reviewer."

2. CONTEXT (The Background)

Give the "Why" and the "Who."

Ex: "We are reviewing a 500-page trial report."

3. TASK (The Action)

Use strong, singular verbs.

Ex: "Distill," "Critique," "Standardize," "Synthesize."

4. CONSTRAINTS (The Boundaries)

Format, length, tone, and "Negative Constraints" (what not to do).

Ex: "Maximum 200 words. Do not mention pharmaceutical brand names."

5. THOUGHT PROCESS (The Logic Path)

NEW for 2026: Tell the model how to step through the problem.

Ex: "Before writing the summary, analyze the methodology for bias. Show your thinking."

### Slide 5: Prompting "Reasoning" Models
Concept: Directing the "Chain of Thought."

The Reasoning Pause: Explain that models now "pre-compute" logic.

Prompt Tip: Use the phrase "Let's think through this step-by-step" to force the model to show its work.

When to use: Use for math, complex ethics, or extracting data from messy, conflicting sources.

### Slide 6: Managing Massive Context (The "Librarian" Workflow)
Concept: When you upload 1,000 pages (GPT-4.1 / Gemini 3), the AI needs "Anchors."

Use Delimiters: Use symbols like ### or [DATA] to separate your instructions from your source text.

Reference Specifics: Ask the AI to cite the page or section number within the context.

Example: "Using only the data in the [Clinical_Trial] block, summarize the adverse events."

### Slide 7: Live Demo: The Logic Gap
Instructor Activity:

Open a Predictive Model (GPT-4o). Ask a complex logic puzzle or medical ethics question. (Fast response).

Open a Reasoning Model (GPT-5). Ask the same question. (Watch the "Thinking..." bar).

Compare: Highlight how the Reasoning model caught nuances the Predictive model missed.

### Slide 8: The "Prompt Lab" (Hands-On)
Exercise: Using the SleepFM video or research paper.

Step 1: Write a "Lazy Prompt" (e.g., "Summarize this").

Step 2: Apply the Five Pillars to the same task.

Step 3: Critique the difference in output quality and "professionalism."

#### Advanced Examples: 🧪 Advanced Constraint Examples for Clinical Summarization
1. The "Guidelines-Anchored" Summary
Goal: Prevent the AI from giving "creative" medical advice by forcing it to anchor every summary point to a specific medical guideline.

Constraint: "Use the provided [NCCN_GUIDELINES] block as the exclusive source for treatment recommendations. For every summary point, provide a parenthetical citation to the specific section or page number found in the text. If the text does not contain a recommendation for a specific symptom, explicitly state 'Guideline does not address this symptom' rather than inferring a solution".

2. The "Chain-of-Density" Summary
Goal: Create a summary that is highly informative but extremely concise, perfect for quick hand-offs.

Constraint: "First, generate a 50-word summary of the patient's current status. Then, identify 3 'missing' technical entities (e.g., specific lab values or medications) and re-write the summary to include them while keeping the word count under 60. Repeat this process until the summary is packed with clinical data but remains under 75 words".

3. The "Differential-First" Reasoning Summary
Goal: Use a Reasoning Model (like GPT-5) to think through a case before summarizing it, reducing the risk of "anchoring bias".

Constraint: "Before writing the final summary, create a [THOUGHT_PROCESS] section. In this section:

List the three most likely differential diagnoses based on the clinical notes provided.

Identify one piece of conflicting data in the labs that challenges the primary diagnosis.

Only after completing these steps, write a 100-word 'Clinical Impression' for the attending physician".

4. The "Multi-Audience" Context Delimiter
Goal: Take a single complex source (like a 20-page research paper on SleepFM) and generate different outputs for different stakeholders in one go.

Constraint: "Process the [SOURCE_TEXT]. Provide two distinct summaries separated by ---:

Header: Resident Briefing. Focus on the machine learning architecture (multimodal foundation model) and C-index scores for clinical prediction.

Header: Patient Education. Explain the concept using a 'sleep-as-a-window' analogy. Avoid technical terms like 'leave-one-out contrastive learning'".

### Slide 9: Key Takeaways & Looking Ahead
Takeaways:

Roles and Constraints are the most powerful levers for quality.

Reasoning models need "permission" to take their time.

Context windows are huge; use delimiters to stay organized.

Next Week: Advanced Workflows & Guardrails

We will look at "Agentic" prompting—asking the AI to build its own plan.

Addressing hallucinations and privacy in 2026.
---
## Teaching Tips for Week 3
### Time Management (60 Mins):

- 00-10: Intro & Week 2 Review.
- 10-25: The Five Pillars (Direct Instruction).
- 25-40: Live Demos (Reasoning vs. Prediction).
- 40-55: Prompt Lab (Student Activity).
- 55-60: Wrap-up & Assignment.

**Common Student Question**: Q: "If the model is so smart, why do I need to be so specific?" A: "A smart intern still needs a clear project brief. Without it, they will use their own assumptions instead of your standards."

**Backup Activity**: If students finish early, have them try a "Reverse Prompt." Paste a high-quality piece of writing into the AI and ask: "What prompt would have generated this output?" (This is excellent for learning Constraint mapping).