# AI For EverybodyPrompt Engineering Fundamentals

# Week 3: From Chatting to Directing

# Check-In

Did you work with models this week?

Did you try a “Reasoning” model (like GPT5) vs a “Predictive” model?

Did you look in to the “Thinking”

---

- Acknowledge that in 2026, prompting isn't just about "words"—it's about managing the AI's "internal logic"
- Today we learn to be AI directors, not just AI users
- The skills learned today directly impact output quality

# Today’s Goals

What We'll Cover:

Master the Five Pillars of 2026 prompting

Learn to "direct" reasoning-heavy models (GPT-5, Claude 4)

Understand context management in massive windows (1M+ tokens)

Practice the "Lazy vs. Engineered" workflow

Build your personal prompt library

---

This is the most technical week - but no coding!
Everything learned here will be used in Weeks 4-6
By end of session, you'll write professional-grade prompts

# Prompt Engineering in 2026

__Definition__ : Systematic design of instructions to align an AI’s logic with your desired outcome

Context is King

Reasoning Costs Time

Consistency

---

1. Context is King

With 2-million-token windows (Gemini 3), the prompt is the "search query" for massive data
Poor prompts = AI gets lost in your documents

2. Reasoning Costs Time

Good prompts help models reason efficiently
Reduces "hallucinations in thought"

3. Consistency

Professional-grade prompting ensures AI doesn't drift off-task during long operations
Reproducible results

2024 prompting: "Be nice to the AI"
2026 prompting: "Give the AI a clear specification"
We're writing instructions, not having conversations

# Five Pillars of a Modern Prompt

ROLE (Persona)

CONTEXT (The Background)

TASK (The Action)

CONSTRAINTS (The Boundaries)

THOUGHT PROCESS (The Logic Path)

__ROLE__  (The Persona)

Don't just ask for an answer; ask for an expert

Example: "You are a Senior NIH Grant Reviewer"

Why: Activates relevant patterns in training data

__2. CONTEXT __ (The Background)

Give the "Why" and the "Who"

Example: "We are reviewing a 500-page trial report for methodological rigor"

Why: Helps AI understand stakes and audience

__3. TASK__  __ __ (The Action)

Use strong, singular verbs

Examples: "Distill," "Critique," "Standardize," "Synthesize"

Avoid: "Tell me about..." or "What do you think..."

__4. CONSTRAINTS__  __ __ (The Boundaries)

Format, length, tone, and negative constraints (what NOT to do)

Example: "Maximum 200 words. Do not mention pharmaceutical brand names."

Why: Prevents AI from taking shortcuts

__5__  __. THOUGHT PROCESS __ (The Logic Path) ⭐ NEW for 2026

Tell the model HOW to step through the problem

Example: "Before writing the summary, analyze the methodology for bias. Show your thinking."

Why: Directs reasoning models' internal deliberation

---

All five aren't always needed, but knowing them improves every prompt
Pillar #5 is the game-changer for reasoning models
Show before/after examples of each pillar

# Example: SleepFM Paper

__Lazy Prompt__ Summarize this research paper.

__Engineered Prompt__

__ROLE: You are a medical education researcher.__

__CONTEXT: I need to present this sleep medicine paper to cardiology residents  __

__who have no machine learning background.__

__TASK: Distill the key clinical implications of the SleepFM model.__

__CONSTRAINTS:  __

__- Maximum 150 words  __

__- Avoid ML jargon (no "contrastive learning" or "C-index")  __

__- Focus on: What does this mean for patient care?__

__THOUGHT PROCESS: First, identify the main clinical finding. Then, explain  __

__why it matters in simple terms. Finally, suggest one practical application.__

# Prompting “Reasoning” Models

__The Reasoning Pause:__

GPT-5, Claude Extended Thinking, Gemini Deep Think

These models "pre-compute" logic before responding

You'll see a "Thinking..." indicator for 20+ seconds

__How to Prompt Reasoning Models:__

Give permission to think: "Take your time to reason through..."

Request the thought process: "Show your step-by-step thinking"

Use the magic phrase: "Let's think through this step-by-step"

__When to Use Reasoning Models:__

Complex mathematics

Ethical dilemmas

Multi-step logical problems

Extracting data from messy, conflicting sources

---

The pause feels awkward at first - resist urge to interrupt
The thinking process is WHERE quality happens
Demo: Same prompt on GPT-4o (fast) vs. GPT-5 (thinking)

# Demo: Directing the Chain of Thought

A 67-year-old woman presents to the ED with acute onset severe headache that began 2 hours ago while she was gardening. She describes it as 'the worst headache of my life.' Her vital signs show BP 178/95, HR 88, temp 37.1°C. She has mild photophobia but no focal neurological deficits on exam. Non-contrast head CT performed 90 minutes after symptom onset is reported as normal.

Walk me through your diagnostic reasoning. What is your differential diagnosis, how would you prioritize these possibilities, and what would be your next steps in management? Explain your reasoning at each decision point.

---

I’m using Gemini because it’s easier to expose the thinking process

# Managing Massive Context Windows

__The "Librarian" Workflow__

__The Challenge:__

You upload 1,000 pages (GPT-4.1 or Gemini 3)

AI needs "anchors" to navigate your content

Without structure, it gets lost

__Solution: Use __  __Delimiters__

### INSTRUCTIONS ###

[Your prompt goes here]

### SOURCE_DATA ###

[Your 1000-page document]

### GUIDELINES ###

Only use information from SOURCE_DATA section.

Cite page numbers for every claim.

---

Why This Works:

Creates clear boundaries
Helps AI know what to reference vs. what to generate
Prevents hallucinations from mixing with real data

Show example of with/without delimiters
Common delimiters: ###, ---, [TAGS], ===
This technique essential for Week 5's NotebookLM work

# Helpful Delimiters

| __Delimiter Type__ | __Best For...__ | __Why?__ |
| :-: | :-: | :-: |
| ### | Section Headers | Mimics Markdown hierarchy. |
| """ | Raw Text/Quotes | Signal for "Treat this as a string, not code." |
| === | Section Break | Shows a hard stop to a collection of information |
| <tag> | Complex Nesting | Allows you to put "Symptoms" inside of "Patient Note" without confusion. |

# Quick Hands-OnExplain a complex concept from your field to a non-expert

Write a “Lazy Prompt”

Apply the Five Pillars

Test Both

Iterate

Check In

__Five Pillars__

ROLE: Who should the AI be?

CONTEXT: Who's the audience? Why do they need this?

TASK: What specifically should be done?

CONSTRAINTS: Format, length, tone, negative constraints

THOUGHT PROCESS: How should the AI approach this?

---

Prompt Participants (5 min):

"Who wants to share a before/after comparison?"
"What surprised you about the difference?"
"Which pillar made the biggest impact?"
Capture Patterns:

Note which pillars participants found most valuable
Identify common mistakes
Celebrate creative constraint use
Key Observations to Highlight:

ROLE and CONSTRAINTS often have biggest impact
THOUGHT PROCESS is powerful for complex tasks
Iteration improved every prompt

Have 2-3 backup examples if participants are shy
Write down patterns to reference in future weeks
Build community through shared learning

# Your Constraint Toolkit

__Format Constraints:__

"Provide as bulleted list"

"Create a table with columns X, Y, Z"

"Use Markdown formatting"

__Length Constraints:__

"Maximum 100 words"

"Exactly 5 examples"

"3-sentence summary"

__Tone Constraints:__

"Professional but friendly"

"Technical precision, avoid marketing language"

"Explain to a 10-year-old"

__Negative Constraints:__

"Do NOT include generic advice"

"Do NOT mention specific drug brands"

"Do NOT make assumptions beyond the provided data"

# Advanced Example: Clinical Summarization

ROLE: You are a Clinical Guidelines Specialist.

CONTEXT: I need to create a treatment summary for physician reference.

TASK: Summarize treatment recommendations from the provided guideline text below.

CONSTRAINTS:

- Use ONLY the guideline text provided below (between the ### markers)

- Provide parenthetical citation (section/subsection) for every recommendation

- If guideline doesn't address a symptom, state: "Guideline does not address this symptom"

- Do NOT infer solutions beyond what's explicitly stated

- Maximum 300 words

THOUGHT PROCESS: For each recommendation:

1. Find exact guideline text that supports it

2. Note the section heading and page number

3. Copy key phrases directly from guideline

4. Only include if explicitly stated, not inferred

### ACP_COLORECTAL_SCREENING_GUIDELINES ###

[Copy and paste the relevant section of the guideline here - e.g., screening guidelines

from ACP]

### END_GUIDELINES ###

Why This Works:

Role sets clinical mindset

Context clarifies stakes

Task is specific action

CONSTRAINTS prevent creativity - this is crucial for clinical content

Thought process creates audit trail

Explicit sourcing prevents hallucinated recommendations

---

You have an example like this in your resources document

This is professional-grade medical prompting
The constraints create safety by preventing inference
Option A (copy-paste) is perfect for learning and occasional use
Option B (NotebookLM) is better for recurring tasks
Show output example if time permits
Emphasize the [SECTION/PAGE] requirement - this forces AI to ground answers
This directly connects to Week 4's verification (you can verify citations!)
Practical demo: Show actual guideline section copied into prompt, walk through one example recommendation with page citation

# More Advanced Constraints

First, generate a 50-word summary of the patient's current status.

Then, identify 3 'missing' technical entities (e.g., specific lab values)  and re-write the summary to include them while keeping the word count  under 60. Repeat until the summary is under 75 words but information-dense.

Process the [SOURCE_TEXT]. Provide two distinct summaries separated by ---:

Header: Resident Briefing

Focus on: ML architecture and C-index scores for clinical prediction

Header: Patient Education

Use a 'sleep-as-a-window' analogy

Avoid technical terms like 'leave-one-out contrastive learning'

# Common Prompting Mistakes

Mistake #1:  __Too Vague__

❌ "Write about patient safety"

✅ "Draft a 200-word patient safety protocol for fall prevention in elderly ICU patients"

Mistake #2: __ Asking for Opinion__

❌ "What do you think about this treatment?"

✅ "Based on the provided guidelines, list contraindications for this treatment"

Mistake #3:  __No Constraints__

❌ "Summarize this paper"

✅ "Create a 3-bullet summary of methodology suitable for a grant proposal"

Mistake #4:  __Forgetting Negative Constraints__

❌ "Explain statistics to beginners"

✅ "Explain statistics to beginners. Do NOT use mathematical notation or assume prior knowledge"

Mistake #5:  __Not Iterating__

First prompt rarely perfect

Review output, identify gaps, refine prompt

Prompting is a conversation with yourself

---

These mistakes are universal - everyone makes them
The fix is always: more specificity
Show before/after for each mistake if time permits

# Iterate Iterate Iterate …

__1. Initial Prompt → Output__

Explain machine learning for medical applications.

_Output: Too technical, too long_

__2. Refine Prompt → Better Output__

Explain machine learning for medical applications in 100 words,

avoiding technical jargon.

_Output: Better, but still generic_

__3. Refine Again → Best Output__

ROLE: Medical educator

TASK: Explain machine learning's role in diagnostics

CONSTRAINTS: 100 words, 8th-grade reading level, include 1 concrete example

AUDIENCE: Patients considering AI-assisted diagnosis

_Output: Clear, specific, appropriate_

# Build Your Prompt Library

__Why Have a Library?__

Recurring tasks deserve reusable prompts

Refinement over time improves quality

Consistency across your work

Training resource for colleagues

__What to Include:__

Purpose: What is this prompt for?

The Prompt: Full text with all five pillars

Notes: What works well, what to adjust

Examples: Sample outputs (good and bad)

__Format Suggestions:__

Document file with sections

Spreadsheet with columns

Note-taking app with tags

Custom GPT (Week 5!)

---

This week's assignment: Start your library
Starter in the resources document
You'll use this in Weeks 4-6
Sharing prompts with colleagues multiplies value

# Wrapping Up

__The Five Pillars:__

ROLE - Who is the AI?

CONTEXT - What's the situation?

TASK - What specific action?

CONSTRAINTS - What are the boundaries?

THOUGHT PROCESS - How should AI reason? ⭐

__Best Practices:__

Roles and Constraints are the most powerful levers for quality

Reasoning models need "permission" to take their time

Use delimiters for massive context windows

Iterate - first prompt is rarely best prompt

Build a library for recurring tasks

---

Connection to Next Week:

Week 4: We'll verify these prompts (red-team auditing)
The better your prompts, the easier verification becomes
Prompting + Verification = Professional AI use


Emphasize that prompting is a skill that improves with practice
No one writes perfect prompts immediately
The five pillars are a framework, not a rigid formula

# Assignment: Build your prompt library

__Part A: Create 3 Production-Ready Prompts__

__A Data Task:__  (e.g., Summarizing clinical notes)

__A Creative Task:__  (e.g., Drafting a department newsletter)

__A Logic Task:__  (e.g., Finding flaws in research methodology)

__Part B: Test & Refine__

Run each prompt

Document what works and what doesn't

Iterate at least once on each

Save both versions

__Part C: Comparison (Bonus)__

Run your "Logic Task" through a Predictive model (GPT-4o)

Run it through a Reasoning model (GPT-5)

Did the reasoning model catch something the predictive one missed?

How much "thinking time" did it take?

---

Emphasize this assignment builds their real toolkit
These prompts will be used in Weeks 4-6
Quality over quantity - 3 excellent prompts better than 10 mediocre ones

