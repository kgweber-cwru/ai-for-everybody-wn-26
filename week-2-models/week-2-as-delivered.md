# Model Architecture, Reasoning & Selection

# AI for Everybody Week w2

Link to seminar slides and handouts ->

![](img/wk2_0.png)

---

Quick Review:
- Last week: What are LLMs?
- Key concepts: prediction, tokens, limitations
- This week: Which model for which task?

Speaker Notes:
- Welcome back
- Quick discussion of Week 1 assignment
- Who found interesting differences?
- Set expectations for today's hands-on comparisons

# Quick Review

“AI” encompasses many ideas, but mostly people are talking about Large Language Models ( __LLMs__ )

LLMs are trained to predict the next  __token__  in a body of text

They are trained millions of times over as much information as possible

Different models have different styles, strengths and weaknesses

# Assignment Discussion

__What did you discover in your model comparison?__

Response Lengths

Tone/Style

Accuracy

What did you find most helpful?

Did any models pause or “think”?Did any fail outright?

---

- Spend 5-10 minutes on this
- Capture themes on board/screen
- Use their observations to intro today's content
- Validate their findings


# Today’s Goals

Major models in depth (GPT-5, 4.1, 4o, Claude, Gemini)

The shift from Prediction-Based to Reasoning-First AI

Context windows explained (Why 1M+ tokens matters)

Multimodal & Agentic capabilities

Hands-on comparative testing

# Reasoning vs Prediction

__The Shift:__

-  __Pre-2025__   Models are "Next-Token Predictors" (Patterns).

-  __2026__ : Latest Models use "Reinforcement Learning via Reasoning" (Logic).

__How it looks:__

-  __Prediction__  (GPT-4o): Responds in < 1 second. Great for brainstorming.

-  __Reasoning__  (GPT-5): May pause for 10-30 seconds. It is running internal simulations and "self-correcting" before you see a word.

---

Demo opening up the reasoning stages in a GPT-5 query

# Chat vs Agentic Workflows

__The Evolution__ :

Prompting: You give a specific command.

Agents: You give a goal (e.g., "Organize a symposium").

__What an Agent does:__

Breaks the goal into a task list,

Tool Use: Opens a browser, uses a Python tool for budget, drafts invites.

---

This is a complicated word in the CWRU context
Demo agentic behaviour in VS Code and/or Gemini

# The 2026 In-House Lineup

__At __  _[ai.case.edu](http://ai.case.edu)_ , with and without Internet queries

__GPT-5__ : The "Pro Reasoning" flagship for autonomous research.

__GPT-4.1__ : The "High-Context" Librarian (1-Million-Token window).

__GPT-4o__ : The "Daily Communicator" for fast, low-latency chat.

__Claude 4 Sonnet__ : The "Creative Logician"—ideal for nuanced writing and instruction following.

__At __  _[gemini.google.com](http://gemini.google.com)_

__Gemini 3__ : Accessible via gemini.google.com for Google Workspace integration and video analysis.

---

We now offer four native models directly. Gemini is also fully available to you through the Google portal.
Match the model to the task: GPT for logic/data, Claude for nuance/writing.


# Claude 4 Sonnet (Anthropic)

__Best For:__

Narrative consistency and human-like "voice."

Complex instruction following (nuanced editing).

__In their native UI:__

"Computer Use" tasks (automating UI interactions).

The Artifacts Advantage: Excellent UI for live-coding and document previews.

---

(Kate’s daily driver)
Consider popping out to native Claude and demonstrate a MCP agent

# Gemini 3: The Ecosystem Power

__Access__ : Visit  _[gemini.google.com](http://gemini.google.com)_  using your CWRU credentials

__Google Workspace Integration__ : Best for pulling data from your Drive, Docs, and Gmail.

__Video Analysis__ : Can "watch" and summarize long video files natively.

__STEM Excellence__ : High performance in technical and mathematical reasoning.

# Context Windows & Working Memory

__Huge Expansion__

__2024: __ 128,000 Tokens was “immense.”

__2026: __ 1-2 Million tokens for flagship research models

__Our Models__

__GPT-4.1__ : 1 Million Tokens (~1,500 pages) — Our "Deep Memory" leader.

__Claude 4 Sonnet__ : 500k Tokens — Excellent for medium-to-long manuscripts.

__Gemini 3 Pro__ : 2 Million Tokens — The "Infinite" library.

---

If you are analyzing a single book, Claude 4 is plenty. If you are analyzing a decade of research, use GPT-4.1 or Gemini.

# Multimodal Capabilities*

| <span style="color:#1f1f1f"> __Capability__ </span> | <span style="color:#1f1f1f"> __GPT-4o / GPT-5__ </span> | <span style="color:#1f1f1f"> __GPT-4.1 (Librarian)__ </span> | <span style="color:#1f1f1f"> __Claude 4 Sonnet__ </span> | <span style="color:#1f1f1f"> __Gemini 3 (Pro/Flash)__ </span> |
| :-: | :-: | :-: | :-: | :-: |
| <span style="color:#1f1f1f"> __Primary Use__ </span> | <span style="color:#1f1f1f"> __Real-time Interaction__ </span> | <span style="color:#1f1f1f"> __Bulk Document Logic__ </span> | <span style="color:#1f1f1f"> __Creative Precision__ </span> | <span style="color:#1f1f1f"> __Video & Workspace__ </span> |
| <span style="color:#1f1f1f"> __Vision__ </span> | <span style="color:#1f1f1f">Instant object/UI recognition.</span> | <span style="color:#1f1f1f">High-volume PDF/OCR extraction.</span> | <span style="color:#1f1f1f">Precise UI analysis & code replication.</span> | <span style="color:#1f1f1f"> __Spatial reasoning__ </span>  <span style="color:#1f1f1f"> & pixel coordinates.</span> |
| <span style="color:#1f1f1f"> __Audio/Voice__ </span> | <span style="color:#1f1f1f"> __Full duplex voice__ </span>  <span style="color:#1f1f1f"> (Standard).</span> | <span style="color:#1f1f1f">Not emphasized (API focus).</span> | <span style="color:#1f1f1f">Clean, literal transcriptions.</span> | <span style="color:#1f1f1f">Best for </span>  <span style="color:#1f1f1f"> __multilingual__ </span>  <span style="color:#1f1f1f"> meetings & calls.</span> |
| <span style="color:#1f1f1f"> __Video__ </span> | <span style="color:#1f1f1f">Frame-by-frame analysis.</span> | <span style="color:#1f1f1f">Limited to document frames.</span> | <span style="color:#1f1f1f">Static frame inspection.</span> | <span style="color:#1f1f1f"> __Native Video reasoning__ </span>  <span style="color:#1f1f1f"> (up to 1 hour).</span> |
| <span style="color:#1f1f1f"> __Best Feature__ </span> | <span style="color:#1f1f1f"> __Advanced Voice Mode:__ </span>  <span style="color:#1f1f1f"> Low-latency, emotive speech.</span> | <span style="color:#1f1f1f"> __Deep Parsing:__ </span>  <span style="color:#1f1f1f"> Extracts tables/charts from 1k+ pages.</span> | <span style="color:#1f1f1f"> __Artifacts:__ </span>  <span style="color:#1f1f1f"> Side-by-side visual code previews.</span> | <span style="color:#1f1f1f"> __Video-to-Action:__ </span>  <span style="color:#1f1f1f"> Can watch a clip & write code to replicate it.</span> |

---

In the full versions of the models

# Model “Personalities”

| ChatGPT | Claude | Gemini |
| :-: | :-: | :-: |
| ProfessionalConciseStructuredConfident | ThoughtfulVerboseNuancedCautiousEngaging | InformativeIntegratedGoogle-Flavored |

---

- These are generalizations
- Can be adjusted with prompting
- Personality matters for user experience
- Some prefer one over others for style alone

# Speed and Responsiveness

__Factors__

- Model size (larger = slower)

- Server load

- Response length

- Complexity of task

__Generally:__

- Mini/small models: Fastest

- Standard models: Moderate

- Reasoning  models: Slower but more capable

__Trade-Offs__

Speed vs. capability vs. cost

# When to Use Which Model

| __Goal__ | __Model__ |
| :-: | :-: |
| Quick Email/Drafting | GPT-4o |
| Massive Document Review | GPT-4.1 |
| Complex Logic/Hard Math | GPT-5 |
| Creative/Nuanced Writing | Claude 4 Sonnet |
| Video / Workspace Integration | Gemini 3 |

# Hands-ON!

Four Exercises

Try one or all

Try different models and experiment with reasoning on/off

Details for these exercises in The Handouts

![](img/wk2_1.png)

# Hands-On 1:

Summarize this paper in 2-3 sentences for a general audience.

? Just the abstract? Whole thing?

Try different models

Note:

Clarity

Accuracy

Accessibility

![](img/wk2_2.png)

# Hands-On 2

Draft a professional email to [a colleague] explaining why your research meeting needs to be rescheduled. Keep it under 100 words

Try different models

Note:

Tone

Length

Structure

Politeness

# Hands-On 3

Review this video

https://www.youtube.com/watch?v=SjdFn4ktmes

And identify

A short summary of the case presented, its challenges, and its solutions

The overall tone of the presentation of the case

Four or five instances when the presenter expresses uncertainty

Indicate the timepoints in the video for these highlighted moments of uncertainty

Probably Best with Gemini

Note:

Clarity of explanation

Quality of Analysis

Accuracy of sentiment detection

Accessibility

# Hands-On 4

Generate 5 creative ideas for teaching medical students about empathy in patient cart

Compare:

Creativity

Practicality

Variety

Inspiration

# Discussion

What models performed best for each task?

Does “best” change from task to task or person to person?

Did you get surprising results?

Did you see patterns?

Any clear winners/losers?

