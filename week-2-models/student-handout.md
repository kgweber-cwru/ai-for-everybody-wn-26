# Week 2: Model Differences and Selection
## Student Handout

---

## Core Concept: Prediction vs. Reasoning
Models now differ not just in *what* they know, but *how* they "think".

* **Prediction-Based (Pattern Matching):** These models (like GPT-4o) guess the next word based on probability. They are fast and excellent for creative brainstorming or simple summaries.
* **Reasoning-Based (Logic Simulation):** Models like **GPT-5** use internal "Chain of Thought." They may pause for 20 seconds to "think" before responding. Use these when accuracy, logic, and multi-step math are non-negotiable.

---

## Understanding "Context Windows" (Your Workspace)
The "Context Window" is the model's active memory. In 2026, these have grown massive:
* **128K (GPT-4o):** Enough for a single long research paper or a legal contract.
* **1 Million (GPT-4.1):** Enough for a decade of medical journals or an entire textbook library.
* **2 Million (Gemini 3):** Enough for 1 hour of native video or massive datasets.

---

## Agentic Workflows: From "Prompts" to "Goals"
We are moving away from simple "Chatting" to "Agentic" behavior.
* **Prompting (Old):** You give a specific command and get a specific answer.
* **Goal-Oriented (New):** You give a goal (e.g., "Review these 50 patient charts for risk factors and draft a summary report"). The model builds its own plan, checks its work, and executes the steps.

---

## Hands-On Exercise 1: The Logic vs. Speed Test
**Goal:** Compare a "Predictor" (GPT-4o) with a "Reasoner" (GPT-5).

1.  **Select a complex task:** Use the medical education paper provided.
2.  **Ask GPT-4o:** "Summarize the methodology of this paper in 3 bullets." (Note the speed).
3.  **Ask GPT-5:** "Critique the statistical validity of the Delphi methodology used here. What are the potential biases?" (Note the 'Thinking' time).
4.  **Reflect:** Which model gave a deeper, more reliable analysis?


---

#### Hands-On 2: Professional Writing
```
Draft a professional email to a colleague explaining that you need to 
reschedule next week's research meeting due to a scheduling conflict. 
Keep it under 100 words and maintain a friendly but professional tone.
```

**What to Compare:**
- Tone (too formal? too casual?)
- Length (follows 100-word limit?)
- Structure
- Natural language flow

---

#### Prompt 3: Video Summarization
```
Review this video

https://www.youtube.com/watch?v=SjdFn4ktmes

And identify

1) A short summary of the case presented, its challenges, and its solutions
2) The overall tone of the presentation of the case
3) Four or five instances when the presenter expresses uncertainty

Indicate the timepoints in the video for these highlighted moments of uncertainty
```

**What to Compare:**
- Clarity of explanation
- Quality of analysis
- Accuracy of sentiment detection
- Accessibility

---

#### Prompt 4: Creative Brainstorming
```
I need to teach medical students about the importance of patient empathy. 
Generate 5 creative, engaging activities or exercises I could use in a 
90-minute session.
```

**What to Compare:**
- Creativity and originality
- Practicality
- Variety of approaches
- Specific detail provided

---

### Comparison Template

Use this to track your findings:

**Prompt Tested:** _____________

| Aspect | ChatGPT | Claude | Gemini |
|--------|---------|--------|--------|
| **Response Length** | | | |
| **Tone/Style** | | | |
| **Accuracy** | | | |
| **Helpfulness** | | | |
| **Followed Instructions?** | | | |
| **Speed** | | | |
| **Reasoning vs Prediction** | | | |
| **Overall Rating (1-5)** | | | |

**Winner for this task:** _____________

**Why:** _____________

---

## Decision Framework: Which Model to Use?

### Choose ChatGPT when you need:
- Quick, concise answers
- Code help or technical tasks
- Structured outputs (tables, lists, formats)
- Math or logical reasoning
- Wide general knowledge
- Familiar, widely-used tool

### Choose Claude when you need:
- Analysis of long documents
- Nuanced, detailed writing
- Complex, multi-step instructions
- Careful, thoughtful responses
- Ethical considerations
- Very large context window

### Choose Gemini when you need:
- Integration with Google Workspace
- Current, real-time information
- Access to YouTube, Gmail, etc.
- Multilingual capabilities
- Largest context window

### Mix and Match!
**Many people use:**
- ChatGPT for quick questions and code
- Claude for writing and analysis
- Gemini for Google-integrated tasks

**There's no rule against using multiple models!**

---

## Advanced Features (Quick Overview)

### ChatGPT
**Custom GPTs** (paid tier):
- Pre-configured assistants
- Specialized for specific tasks
- Shareable with others

**Memory** (optional):
- Remembers preferences across chats
- Can be turned off
- User-controlled

**Plugins** (paid tier):
- Web browsing
- Code execution
- Third-party integrations

---

### Claude
**Projects**:
- Organize related conversations
- Share context across chats
- Add custom instructions

**Artifacts**:
- Generate documents, code
- Edit in-line
- Export easily

---

### Gemini
**Workspace Extensions**:
- Gmail integration
- Google Docs access
- Calendar integration
- Drive search

**YouTube Integration**:
- Summarize videos
- Answer questions about content
- Extract key points

---

## Tips for Model Selection

### Start with One
- Pick your "default" model
- Get comfortable with it
- Learn its strengths and limits

### Experiment with Others
- Try same tasks on different models
- Note when one outperforms
- Keep mental notes on strengths

### Develop Preferences
- It's okay to have a favorite
- Task-specific choices are smart
- Personal style matters

### Stay Flexible
- Models improve constantly
- New features added regularly
- What's true today may change

---

## Common Scenarios

**Scenario 1: I need to analyze a 50-page research paper**
→ **Claude** (large context window, good at analysis)

**Scenario 2: I need help debugging Python code**
→ **ChatGPT** (strongest at code)

**Scenario 3: I need to search my Gmail for something**
→ **Gemini** (Google integration)

**Scenario 4: I need to write a detailed grant proposal**
→ **Claude** (nuanced writing, detail-oriented)

**Scenario 5: I need a quick answer to a factual question**
→ **Any model** (all handle this well)

**Scenario 6: I need current information about recent events**
→ **Gemini** (access to current data) or web-enabled version of others

---

## Take-Home Exercise (Due Next Week)

### Assignment: Real-World Model Testing

**Part 1: Choose Your Default (30 minutes)**
Based on today's testing, choose which model you'll use as your primary tool.

**My choice:** _____________

**Why:** _____________

---

**Part 2: Use It For Real Tasks (This Week)**
Use your chosen model for at least 3 real tasks from your work:

**Task 1:**
- What you asked it to do: _____________
- How it performed: _____________
- What worked: _____________
- What didn't work: _____________

**Task 2:**
- What you asked it to do: _____________
- How it performed: _____________
- What worked: _____________
- What didn't work: _____________

**Task 3:**
- What you asked it to do: _____________
- How it performed: _____________
- What worked: _____________
- What didn't work: _____________

---

**Part 3: Try a Different Model (Bonus)**
Pick ONE task where your default model struggled. Try it on a different model.

**Original model:** _____________
**Alternate model:** _____________
**Task:** _____________
**Did the other model do better?:** _____________
**What did you learn?:** _____________

---

**Part 4: Reflection (Write 2-3 paragraphs)**

1. What surprised you most about the differences between models?
2. Do you think you'll stick with one model or use multiple? Why?
3. What tasks do you think AI could help you with regularly?
4. What are you still uncertain about or want to learn more about?

---

## Quick Reference: When Things Go Wrong

**Problem:** Model refuses my request
**Solutions:**
- Rephrase more clearly
- Try different model
- Be more specific about benign intent
- Remove potentially triggering words

**Problem:** Response is too long/short
**Solutions:**
- Add length requirements to prompt
- Ask it to expand or condense
- Use "in X words" or "in X sentences"

**Problem:** Wrong tone (too formal/informal)
**Solutions:**
- Specify desired tone in prompt
- Give examples of tone you want
- Ask it to revise with different tone

**Problem:** Inaccurate information
**Solutions:**
- Verify important facts independently
- Ask for sources (but verify those too!)
- Try more specific prompting
- Use model better suited to task

---

## Resources

### Official Documentation
- **ChatGPT:** help.openai.com
- **Claude:** support.anthropic.com
- **Gemini:** support.google.com/gemini

### Model Comparison Sites
- Artificial Analysis ([artificialanalysis.ai](https://artificialanalysis.ai/))
- LMSys Chatbot Arena ([various model comparisons](https://lmarena.ai/leaderboard))

### Stay Current
- Models update frequently
- Follow official blogs/announcements
- Check tech news sites
- Ask in communities

---

## Looking Ahead

**Next Week: Prompt Engineering Fundamentals**
We'll dive deep into writing effective prompts:
- Core principles
- Common patterns
- Getting better results
- Iterating and refining

**Come prepared with examples of prompts that didn't work well!**

---

## Notes & Observations

**Favorite model so far:** _____________

**Why:** _____________

**Most surprising discovery:** _____________

**Question for next week:** _____________

**Task I want to try:** _____________
