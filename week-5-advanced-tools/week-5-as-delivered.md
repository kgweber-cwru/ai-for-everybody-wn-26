# AI For Everybody

# Week 5: Advanced ToolsKate Weber, Ph.D.Faculty Director for AI in Medical Education, CWRU

# Building your personal information store

Understanding "grounded" AI and RAG (Retrieval-Augmented Generation)

NotebookLM for document-grounded responses

Custom GPTs with system instructions

Building knowledge agents that don't hallucinate outside your sources

Hands-on: Create your own grounded knowledge base

---

This is where Weeks 3-4 pay off
Prompting skills (Week 3) become system instructions
Verification skills (Week 4) become less necessary with grounding
We're building specialized tools, not just using general ones


# The Hallucination Problem (Recap)

__Type 1: Factual Hallucination__

Definition: Making up data that doesn't exist

Example: Inventing a lab value, fabricating a citation

Status in 2026: Rare in modern models with grounding

__Type 2: Logical Hallucination__  ⚠️

Definition: Using real data but reaching an unsound conclusion

Example: Correctly identifying a lab measurement value but recommending a contraindicated drug

Status in 2026:  __COMMON and critical to detect__

__The Question: Can we prevent hallucinations instead of just catching them?__

__The Answer: Yes! By grounding AI in your specific sources__

---

Verification is necessary but labor-intensive
Grounding reduces the need for verification
It's not perfect, but it's a huge improvement
This is the future of professional AI use

# Grounded AI:AI restricted to ONLY use your provided sources

<span style="color:#5e5e5e">Upload Documents</span>

__R__ etrieval  __A__ ugmented  __G__ eneration ( __RAG__ )

__Retrieval__ : finds relevant parts of your documents

__Augmented__ : Adds that information to the prompt

__Generation__ : Creates an answer based on that information

<span style="color:#5e5e5e">AI Searches ONLY these documents</span>

<span style="color:#5e5e5e">AI Cites its sources</span>

---

This is the biggest shift in practical AI use
General-purpose = convenient but risky
Grounded = slightly less convenient but much safer
Show diagram if possible: User Query → Document Search → Grounded Response

# Grounded AI vs General AI

| __Aspect__ | __General AI__ | __Grounded AI__ |
| :-: | :-: | :-: |
| __Knowledge Source__ | Entire Internet (training data) | Your uploaded documents |
| __Hallucination Risk__ | High for specifics | Low (can only cite what’s there) |
| __Citations__ | Unreliable* or fake | Direct Links to Source |
| __Customization__ | Generic Knowledge | Your specific domain |
| __Best for__ | Brainstorming, drafting | Analysis, verification, synthesis |

---

Both have their place
Week 1-4 taught general AI use
Week 5-6 teach specialized AI use
Professional workflows use both strategically

# NotebookLM: https://notebooklm.google.com/

__What is NotebookLM?__

Google's research-first AI tool

Upload up to 50 sources per notebook

Each source can be 500K+ words

2-million-token context window

__Key Features:__

__Source-Grounded Responses__ : Every answer includes citations

__Interactive Audio Overviews__ : AI generates podcast-style discussions

__Automatic Citation Linking__ : Click citation → see exact paragraph

__Multi-Source Synthesis__ : Finds connections across your documents

__Query Suggestions__ : AI suggests questions based on your sources

---

This is Google's answer to "how do we prevent hallucinations"
Built specifically for research and document analysis
Integrates with Gemini 3 Pro (reasoning model)
Show the interface live if possible

# NotebookLM: Best Practices

__DO:__

✅ Upload high-quality, authoritative sources

✅ Give your notebook a clear purpose/title

✅ Click citations to verify accuracy

✅ Use specific queries (apply Week 3 prompting skills!)

✅ Keep notebooks focused (one topic per notebook)

__DON'T:__

❌ Trust uncited statements

❌ Upload random internet articles without vetting

❌ Mix completely unrelated topics in one notebook

❌ Exceed source limits (quality > quantity)

❌ Forget that AI can still make logical errors

---

"Garbage in, garbage out" still applies
Grounding doesn't replace critical thinking
Week 4's verification skills still matter
But workload is greatly reduced

# Demo

Heart Failure NotebookLM

FCR Health NotebookLM

# Tool 2: Custom GPTS

__What is a Custom GPT?__

Specialized version of ChatGPT

Pre-loaded with instructions and knowledge

Reusable for specific tasks

Shareable with colleagues

__Why Create Custom GPTs?__

Consistency across repeated tasks

No need to re-type instructions every time

Can include your organization's specific guidelines

Can be shared with team for standardization

---

This is where Week 3's Five Pillars become permanent
Instead of crafting perfect prompt each time, build it once
Great for workflows that repeat weekly/daily
Show real examples if you have them

# Components of a custom GPT

<span style="color:#5e5e5e">Name</span>

<span style="color:#5e5e5e">Description</span>

---

Components of a Custom GPT:

1. Name & Description

What is this GPT for?
Who is it for?
2. Instructions (System Prompt)

This is your Week 3 Five Pillars!
ROLE, CONTEXT, TASK, CONSTRAINTS, THOUGHT PROCESS
Permanent instructions the GPT always follows
3. Knowledge Base

Upload files the GPT can reference
Your SOPs, templates, guidelines
Same concept as NotebookLM but integrated into ChatGPT
4. Capabilities

Web browsing: Can it search current information?
DALL-E: Can it generate images?
Code Interpreter: Can it run Python?
5. Actions (Advanced)

Connect to external APIs
Schedule emails, update calendars, etc.
Speaker Notes:

#2 (Instructions) is what most people use
#3 (Knowledge) turns it into grounded AI
#4 and #5 are advanced - optional
We'll focus on #2 and #3 today

# DEMO: FlatCoatedRetrieverBot

![](img/wk5_0.png)

![](img/wk5_1.png)

![](img/wk5_2.png)

---

t

![](img/wk5_3.png)

![](img/wk5_4.png)

![](img/wk5_5.png)

---

Using gemini/gem - but show the ai.case.edu options as well

Name / description / highlight the system prompt expressing tone and information
Adding knowledge from specific articles AND my FCR health notebooklm
Sample query
Available for anyone you share it with

# Custom GPT/Gem vs NotebookLM

__NotebookLM__

Explore new literature

Find conflicts/agreements across sources

Deep dives

Research synthesis

Building overviews/summaries

__Custom GPT/Gem__

Standardized processes

Recurring workflows

Team collaboration

Tool integration

Combines grounding and general knowledge

---

Can Use Both:

Research in NotebookLM → Draft in Custom GPT
Literature review in NotebookLM → Write-up in Custom GPT
They complement each other!
Speaker Notes:

These aren't competing tools
Professional workflows use both
Week 6 will show orchestration between tools
Choose based on task and frequency

<span style="color:#5e5e5e"> __Medical/Clinical:__ </span>

<span style="color:#5e5e5e">Protocol Assistant: Upload all department protocols → instant reference</span>

<span style="color:#5e5e5e">Literature Reviewer: Upload papers on specific topic → synthesis</span>

<span style="color:#5e5e5e">Guidelines Comparator: Upload multiple guidelines → find differences</span>

<span style="color:#5e5e5e">Case Study Analyzer: Upload teaching cases → generate discussion questions</span>

<span style="color:#5e5e5e"> __Research:__ </span>

<span style="color:#5e5e5e">Methods Consultant: Upload methodology papers → answer methods questions</span>

<span style="color:#5e5e5e">Grant Reviewer: Upload successful grants + guidelines → review drafts</span>

<span style="color:#5e5e5e">Data Interpretation: Upload analysis results → help explain findings</span>

<span style="color:#5e5e5e"> __Administrative:__ </span>

<span style="color:#5e5e5e">Policy Navigator: Upload institutional policies → quick answers</span>

<span style="color:#5e5e5e">Meeting Prep: Upload agendas + background docs → briefing summaries</span>

<span style="color:#5e5e5e">Communication Drafter: Upload templates + style guides → consistent messaging</span>

# Use Cases

---

Ask: What use cases do participants envision?
Real adoption comes from solving real problems
Start small: One recurring task
Expand as you gain confidence 

# Hands On!



* __Option A: NotebookLM__
* Go to  _[notebooklm.google.com](http://notebooklm.google.com)_  as your CWRU self
* Create a new notebook for your domain
* Upload 3-5 relevant documents (papers, guidelines, SOPs)
* Try the "Guideline Reconciliation" task:
  * Query: "Where do these documents provide different advice?"
  * Check citations
  * Verify one citation by clicking through


__Option B: Custom GPT/Gem__

Start at  _[https://ai.case.edu/chat/agents](https://ai.case.edu/chat/agents)_  or  _[https://gemini.google.com/gems/view](https://gemini.google.com/gems/view)_

Design a bot for a recurring task

Write a system prompt using the  __Five Pillars__

Upload some knowledge files

Test

# The Five Prompting Pillars (recap)

<span style="color:#737373"> __ROLE__ </span>  <span style="color:#737373"> (Persona)</span>

<span style="color:#737373"> __CONTEXT__ </span>  <span style="color:#737373"> (The Background)</span>

<span style="color:#737373"> __TASK__ </span>  <span style="color:#737373"> (The Action)</span>

<span style="color:#737373"> __CONSTRAINTS__ </span>  <span style="color:#737373"> (The Boundaries)</span>

<span style="color:#737373"> __THOUGHT PROCESS__ </span>  <span style="color:#737373"> (The Logic Path)</span>

Be Specific

Be ready to iterate

# Limitations and Cautions

__What Grounded AI Can't Do:__

❌ Guarantee perfect accuracy (verification still needed)

❌ Update automatically when sources change

❌ Replace human expertise and judgment

❌ Handle highly ambiguous or contradictory sources perfectly

__Best Practices:__

Still verify critical outputs

Update knowledge bases regularly

Don't over-trust just because it's grounded

Use for assistance, not autonomous decision-making

Combine with human review for high-stakes work

# Key Takeaways

__Major Concepts:__

Grounded AI  __limits responses to your specific sources__

__RAG__  (Retrieval-Augmented Generation) is the technical approach

__NotebookLM__ : Google's tool for document-grounded research

__Custom GPTs__ : Chat services specialized with your instructions and knowledge

__Why Grounding Matters:__

Reduces hallucinations dramatically

Provides verifiable citations

Customizes AI to your specific domain

Makes verification easier

# Looking Ahead

Next Week: Orchestration & Building Your AI Workflow

Scite.ai for research verification

Multi-tool workflows (orchestration)

Combining: Verification (Scite) → Synthesis (NotebookLM) → Drafting (Custom GPT)

Building your complete, verifiable AI pipeline

Wrap-up and implementation planning

# Suggested Exercise for You

Option A (NotebookLM):

Create a notebook with your 5 most-referenced resources

Generate an Audio Overview

Listen for and note one "connection" the AI made that you hadn't considered - was there one? Was it interesting?

Option B (Custom GPT/GEM):

Design a GPT for a specific recurring task

Write system instructions using the Five Pillars

Test with 3 different queries

Refine instructions based on outputs

