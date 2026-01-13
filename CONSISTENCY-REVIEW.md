# Series 1: Content Consistency Review
## Completed January 2026

### Executive Summary
Review of all six weeks of materials completed to ensure internal consistency and progression. Key updates made to align student and instructor materials with 2026 AI landscape.

---

## Week-by-Week Consistency Analysis

### Week 1: Introduction to Generative AI
**Status:** ✅ **CONSISTENT**

- Student handout and instructor notes are well-aligned
- Both cover core concepts: tokens, prediction, temperature, major models
- Hands-on exercises match between materials
- Assignment (model comparison) clearly defined in both

**Key Content:**
- Week 1 introduces: What are LLMs? How do they work? What can/can't they do?
- Foundation for all subsequent weeks
- Sets up Week 2's model comparison assignment

---

### Week 2: Model Differences and Selection
**Status:** ✅ **FIXED** (Updated for 2026 consistency)

**Issue Found:**
- Student handout was heavily updated to 2026 models (GPT-5, Claude 4.5, Gemini 3 with reasoning)
- Instructor notes referenced older model descriptions
- Mismatch in understanding what models are available to participants

**Changes Made:**
- Updated Slide 4 in instructor notes to align with 2026 model landscape
- Added distinction between **Prediction-Based** (GPT-4o, immediate) vs. **Reasoning-Based** (GPT-5, takes time) models
- Updated Slide 11 (Speed and Responsiveness) to explain reasoning pause in GPT-5/Deep Think
- Clarified that extended thinking is a feature, not a bug (takes longer but more accurate)

**Key Content After Update:**
- **GPT-5:** Reasoning-first, internal thinking, for complex logic
- **GPT-4.1:** Context-first, 1M tokens, for massive documents
- **GPT-4o:** Speed-first, immediate responses, for quick tasks
- **Claude 4.5 Sonnet:** Extended thinking option for reasoning tasks
- **Gemini 3 Pro:** "Deep Think" mode for PhD-level problems

**Critical Progression Note:**
This model understanding is essential for Week 3 prompting because:
- Reasoning models need "permission" to think (phrase: "Let's think step-by-step")
- Prediction models are faster for routine tasks
- Context is now king with 1M+ token windows

---

### Week 3: Prompt Engineering Fundamentals
**Status:** ✅ **CONSISTENT**

- Instructor notes and student handout are well-aligned
- Both cover the Five Pillars: ROLE, CONTEXT, TASK, CONSTRAINTS, THOUGHT PROCESS
- Hands-on exercise (SleepFM explanation) is identical in both materials
- Assignment (create 3 production-ready prompts) clearly defined

**Key Progression:**
- Builds on Week 2's understanding of reasoning vs. prediction models
- "Thought Process" pillar is NEW for 2026 (tells model how to think for reasoning models)
- Large context windows mean delimiters/anchors are critical
- Sets up Week 4's verification techniques

**Connection to Week 4:**
The prompts students create in Week 3 will be verified/audited in Week 4 using red-team techniques

---

### Week 4: Advanced Prompting and Responsible Use
**Status:** ✅ **FIXED** (Reorganized for logical flow)

**Issues Found:**
- Title was "Advanced Prompting and Responsible Use" but primarily focused on red-team auditing
- Missing connection between advanced prompting techniques and red-team auditing
- Needed to scaffold: Prompting Techniques → Understanding Errors → Verification Methods → Red Team Auditing

**Changes Made:**
- Restructured student handout into four clear parts:
  1. **Part A:** Advanced Prompting Techniques (Chain-of-Thought, Self-Consistency, Verification)
  2. **Part B:** Understanding AI Errors and Hallucinations (Factual vs. Logical)
  3. **Part C:** Chain-of-Verification (CoVe) Pattern (Four-step verification process)
  4. **Part D:** Red Team Auditing & Adversarial Testing (Three-step critical analysis)
- This scaffolding helps students understand WHY red-teaming matters (to catch logical hallucinations)

**Key Distinction (2026):**
- **Factual Hallucinations** (making up facts): Rare in modern models
- **Logical Hallucinations** (right data, wrong conclusion): COMMON and critical to catch
- Example: Model correctly identifies high potassium but still recommends a contraindicated medication

**Verification Pipeline:**
1. **Extraction:** Identify every claim the AI made
2. **Evidence Anchor:** Prove each claim with source text
3. **Adversarial Review:** Find reasons the AI's suggestion might be wrong
4. **Final Audit:** Did the adversarial step change the recommendation?

**Connection:**
- Uses prompting skills from Week 3 to build verification prompts
- Introduces concepts that enable Week 5 (grounded AI needs verification)
- Essential for Week 6's professional workflows

---

### Week 5: Knowledge Agents & Grounded AI
**Status:** ✅ **CONSISTENT**

- Student handout and instructor notes are aligned
- Both cover: NotebookLM (grounded to your documents), Custom GPTs (specialized workflows)
- Practical exercises match (Guideline Reconciliation activity)
- Assignment (create clinical protocol agent) is clear

**Key Content:**
- **Grounded AI:** Restricting AI to use only your provided sources
- **RAG (Retrieval-Augmented Generation):** Technical term for this approach
- **Direct Citation:** Every answer includes citations to source material
- **The Goal:** Reduce hallucinations by limiting AI's "world" to verified sources

**Why This Matters (Week 5 Role in Series):**
- Week 1-4 teach how to use general-purpose AI
- Week 5 teaches how to build specialized AI for your specific context
- NotebookLM prevents the "I made up information outside my training data" problem
- Custom GPTs with system instructions (Five Pillars) create consistent, reliable assistants

**Assignment Connection:**
Students build a "Clinical Protocol Agent" using Week 3's Five Pillars as system instructions

---

### Week 6: Orchestration & Building Your AI Workflow
**Status:** ✅ **FIXED** (Clarified orchestration concept)

**Issue Found:**
- Materials jump to "Scite.ai" without explaining why it's important
- Missing context about "orchestration" - connecting all weeks together
- Unclear how this synthesizes Weeks 1-5

**Changes Made:**
- Added "The Big Picture" section explaining progression
- Added "Orchestration" concept BEFORE Scite introduction
- Clarified the **Three-Stage Pipeline:**
  1. **Verification Stage (Scite):** Find evidence, check for retractions
  2. **Synthesis Stage (NotebookLM):** Organize your documents
  3. **Drafting Stage (Custom GPT/Claude):** Produce final output

**Why This Matters:**
Rather than trusting any single tool, professional 2026 workflows use:
- Scite to verify citations and find retractions
- NotebookLM to ground AI in your specific documents
- Custom GPT to format output according to organizational standards

This eliminates the "hallucination risk" by having each tool specialize

**Final Assignment:**
Students create a "Workflow Map" for a recurring task, showing:
- Which tools are used at each stage
- Where the "Red Team" audit happens
- How outputs are verified before use

---

## Root-Level Reference Materials Updates

### README.md
**Updated:** Week descriptions now match actual content

**Specific Changes:**
- Week 2: Added mention of "agentic workflows" 
- Week 3: Clarified "Five Pillars" focus
- Week 4: Added "red-team auditing" and "CoVe pattern" to description
- Week 5: Added "RAG" explanation
- Week 6: Changed from "Scite and Building Your AI Workflow" to "Orchestration & Building Your AI Workflow" to reflect focus on multi-tool integration

### FLIER-COPY.md
**Updated:** Marketing copy now reflects 2026 model updates and actual content

**Specific Changes:**
- Week 2: Added emphasis on "reasoning models vs. prediction models"
- Week 3: Clarified "5 pillars" (not 4) and added 1M+ token context mention
- Week 4: Added "Chain-of-Verification" and "red-team auditing"
- Week 5: Added "RAG (Retrieval-Augmented Generation)" explanation
- Week 6: Clarified "orchestration" and "multi-tool workflows"

---

## 2026 AI Landscape - Consistent Throughout Series

### Models Mentioned:
**OpenAI:**
- GPT-5: Reasoning-first, internal thinking for complex logic
- GPT-4.1: High-context specialist (1M tokens)
- GPT-4o: Interface model, real-time voice and low-latency chat

**Anthropic:**
- Claude 4.5 Sonnet: Industry standard for writing and analysis
- Claude 4.5 Opus: For computer use and autonomous coding
- Extended Thinking: Native toggle for deep reasoning

**Google:**
- Gemini 3 Pro: Reasoning leader with "Deep Think" mode
- Gemini 3 Flash: Fast model for quick tasks
- Gemini Agent: For multi-step Workspace tasks

### Tools Introduced by Week:
- **Week 1-2:** Chat interfaces (ChatGPT, Claude.ai, Gemini)
- **Week 3-4:** Prompting techniques (no new tools, just better usage)
- **Week 5:** NotebookLM (Google), Custom GPTs (OpenAI)
- **Week 6:** Scite.ai, plus integration of previous tools

---

## Key Pedagogical Progressions Verified

### 1. Model Understanding Progression
```
Week 1: All models are LLMs
  ↓
Week 2: Different models have different strengths
  ↓
Week 3: Reasoning models need special prompting (THOUGHT PROCESS pillar)
  ↓
Week 4: Understanding model errors helps with prompting
  ↓
Week 5: Grounding AI in your documents reduces errors
  ↓
Week 6: Professional workflows use specialized tools for each stage
```

### 2. Prompting Sophistication Progression
```
Week 1: "Try your first prompts"
  ↓
Week 2: "Choose which model for which task"
  ↓
Week 3: "Master the Five Pillars and direct complex reasoning"
  ↓
Week 4: "Verify and audit prompts with advanced techniques"
  ↓
Week 5: "Build specialized prompts into Custom GPTs"
  ↓
Week 6: "Orchestrate prompts across multiple specialized tools"
```

### 3. Verification Sophistication Progression
```
Week 1: "Verify important facts"
  ↓
Week 2: (No verification focus)
  ↓
Week 3: "Ask for sources in prompts"
  ↓
Week 4: "Chain-of-Verification and red-team auditing"
  ↓
Week 5: "Grounding in documents provides automatic verification"
  ↓
Week 6: "Multi-tool orchestration with Scite for final verification"
```

---

## Consistency Issues RESOLVED

| Week | Issue | Resolution |
|------|-------|-----------|
| 2 | Instructor notes outdated model landscape | Updated to 2026 models with reasoning capabilities |
| 2 | No mention of extended thinking/reasoning pause | Added Slide 11 update explaining speed tradeoffs |
| 4 | Missing advanced prompting foundation | Added Part A with CoT, Self-Consistency, Verification |
| 4 | Unclear connection to Week 3 Five Pillars | Added context showing how prompts are then verified |
| 6 | Vague "Scite introduction" | Added orchestration framework and three-stage pipeline |
| README | Week descriptions didn't match content | Updated all 6 week descriptions for accuracy |
| FLIER | Marketing copy outdated | Updated to reflect 2026 content and focus |

---

## Quality Checks Performed

✅ **Internal Consistency:** Student and instructor materials match within each week
✅ **Progression:** Each week builds logically on previous weeks
✅ **Model Landscape:** Consistent 2026 AI model descriptions throughout
✅ **Assignment Flow:** Each week's assignment flows into next week's content
✅ **Tool Introduction:** Tools introduced in logical order with clear purpose
✅ **Skill Building:** Prompting, verification, and workflow skills build progressively
✅ **Marketing Materials:** FLIER and README accurately reflect actual content

---

## Recommendations for Instructors

### Before Teaching:
1. Review the **progression summaries** above to understand how weeks connect
2. Note that Week 2 instructor notes now emphasize **reasoning vs. prediction** models
3. In Week 3, emphasize that "THOUGHT PROCESS" pillar is new for reasoning models
4. Week 4's four-part structure helps students understand the "why" behind red-teaming
5. Week 5 builds directly on Week 4's verification techniques
6. Week 6 assumes students understand all previous concepts - it's integration, not new content

### Teaching Adjustments:
- **Week 2:** Spend extra time on "reasoning pause" - it's counter-intuitive but critical
- **Week 3:** Explicitly connect "THOUGHT PROCESS" pillar to Week 2's reasoning models
- **Week 4:** Guide students through the four-part scaffold before starting red-team activity
- **Week 5:** Remind that grounding prevents logical hallucinations (from Week 4)
- **Week 6:** Have students bring their Week 5 custom GPTs to integrate into final workflows

### Assignment Continuity:
- Week 1 → Week 2: Model comparison teaches which tool is best
- Week 2 → Week 3: Understanding models informs prompting strategy
- Week 3 → Week 4: Prompts created in Week 3 are verified in Week 4
- Week 4 → Week 5: Verification techniques ensure Custom GPT instructions are solid
- Week 5 → Week 6: Custom GPTs are integrated into final orchestrated workflows

---

## Summary

All materials are now **internally consistent** and **properly sequenced** to build a comprehensive understanding of AI tools in professional contexts. The 2026 AI landscape (reasoning models, extended context windows, grounded AI) is consistently reflected throughout.

Students completing this series will be able to:
- Choose appropriate models for different tasks
- Write sophisticated, multi-component prompts
- Verify and audit AI outputs for correctness
- Build personalized AI agents grounded in their own knowledge
- Orchestrate multiple AI tools into professional workflows

---

*Prepared: January 2026*
*Next Review: June 2026 (or after significant tool updates)*
