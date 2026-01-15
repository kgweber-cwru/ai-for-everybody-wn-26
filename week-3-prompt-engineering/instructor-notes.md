# Week 3: Prompt Engineering Fundamentals
## Instructor Notes (Convert to Slides)

---

### Slide 1: Title & Welcome Back
**Title:** Prompt Engineering Fundamentals  
**Subtitle:** Week 3 - From Chatting to Directing

**Quick Check-In:**
- From Week 2, who tried a "Reasoning" model (GPT-5) vs. a "Predictive" model (GPT-4o)?
- Did anyone notice the "Thinking" pause?
- Did the reasoning model change how you felt about the accuracy of the answer?

**Speaker Notes:**
- Acknowledge that in 2026, prompting isn't just about "words"—it's about managing the AI's "internal logic"
- Today we learn to be AI directors, not just AI users
- The skills learned today directly impact output quality

---

### Slide 2: Today's Goals
**What We'll Cover:**
- Master the Five Pillars of 2026 prompting
- Learn to "direct" reasoning-heavy models (GPT-5, Claude 4)
- Understand context management in massive windows (1M+ tokens)
- Practice the "Lazy vs. Engineered" workflow
- Build your personal prompt library

**Speaker Notes:**
- This is the most technical week - but no coding!
- Everything learned here will be used in Weeks 4-6
- By end of session, you'll write professional-grade prompts

---

### Slide 3: What is Prompt Engineering in 2026?
**Definition:** The systematic design of instructions to align an AI's logic with your desired outcome

**Why the "Engineering" Part Matters Now:**

**1. Context is King**
- With 2-million-token windows (Gemini 3), the prompt is the "search query" for massive data
- Poor prompts = AI gets lost in your documents

**2. Reasoning Costs Time**
- Good prompts help models reason efficiently
- Reduces "hallucinations in thought"

**3. Consistency**
- Professional-grade prompting ensures AI doesn't drift off-task during long operations
- Reproducible results

**Speaker Notes:**
- 2024 prompting: "Be nice to the AI"
- 2026 prompting: "Give the AI a clear specification"
- We're writing instructions, not having conversations

---

### Slide 4: The Five Pillars of a Modern Prompt

**1. ROLE (The Persona)**
- Don't just ask for an answer; ask for an expert
- Example: "You are a Senior NIH Grant Reviewer"
- Why: Activates relevant patterns in training data

**2. CONTEXT (The Background)**
- Give the "Why" and the "Who"
- Example: "We are reviewing a 500-page trial report for methodological rigor"
- Why: Helps AI understand stakes and audience

**3. TASK (The Action)**
- Use strong, singular verbs
- Examples: "Distill," "Critique," "Standardize," "Synthesize"
- Avoid: "Tell me about..." or "What do you think..."

**4. CONSTRAINTS (The Boundaries)**
- Format, length, tone, and "Negative Constraints" (what NOT to do)
- Example: "Maximum 200 words. Do not mention pharmaceutical brand names."
- Why: Prevents AI from taking shortcuts

**5. THOUGHT PROCESS (The Logic Path)** ⭐ NEW for 2026
- Tell the model HOW to step through the problem
- Example: "Before writing the summary, analyze the methodology for bias. Show your thinking."
- Why: Directs reasoning models' internal deliberation

**Speaker Notes:**
- All five aren't always needed, but knowing them improves every prompt
- Pillar #5 is the game-changer for reasoning models
- Show before/after examples of each pillar

---

### Slide 5: Live Example - Five Pillars in Action

**Lazy Prompt:**
```
Summarize this research paper.
```

**Engineered Prompt:**
```
ROLE: You are a medical education researcher.

CONTEXT: I need to present this sleep medicine paper to cardiology residents  
who have no machine learning background.

TASK: Distill the key clinical implications of the SleepFM model.

CONSTRAINTS:  
- Maximum 150 words  
- Avoid ML jargon (no "contrastive learning" or "C-index")  
- Focus on: What does this mean for patient care?

THOUGHT PROCESS: First, identify the main clinical finding. Then, explain  
why it matters in simple terms. Finally, suggest one practical application.
```

**Comparison:** Run both live and compare outputs

**Speaker Notes:**
- The engineered prompt takes longer to write
- But the output is dramatically better
- For recurring tasks, save the engineered prompt as a template

---

### Slide 6: Prompting "Reasoning" Models
**Concept:** Directing the "Chain of Thought"

**The Reasoning Pause:**
- GPT-5, Claude Extended Thinking, Gemini Deep Think
- These models "pre-compute" logic before responding
- You'll see a "Thinking..." indicator for 20+ seconds

**How to Prompt Reasoning Models:**
- **Give permission to think:** "Take your time to reason through..."
- **Request the thought process:** "Show your step-by-step thinking"
- **Use the magic phrase:** "Let's think through this step-by-step"

**When to Use Reasoning Models:**
- Complex mathematics
- Ethical dilemmas
- Multi-step logical problems
- Extracting data from messy, conflicting sources

**Speaker Notes:**
- The pause feels awkward at first - resist urge to interrupt
- The thinking process is WHERE quality happens
- Demo: Same prompt on GPT-4o (fast) vs. GPT-5 (thinking)

---

### Slide 7: Managing Massive Context Windows
**The "Librarian" Workflow**

**The Challenge:**
- You upload 1,000 pages (GPT-4.1 or Gemini 3)
- AI needs "anchors" to navigate your content
- Without structure, it gets lost

**Solution: Use Delimiters**
```
### INSTRUCTIONS ###
[Your prompt goes here]

### SOURCE_DATA ###
[Your 1000-page document]

### GUIDELINES ###
Only use information from SOURCE_DATA section.  
Cite page numbers for every claim.
```

**Why This Works:**
- Creates clear boundaries
- Helps AI know what to reference vs. what to generate
- Prevents hallucinations from mixing with real data

**Speaker Notes:**
- Show example of with/without delimiters
- Common delimiters: ###, ---, [TAGS], ===
- This technique essential for Week 5's NotebookLM work

---

### Slide 8: Live Demo - Reasoning vs. Prediction
**Instructor Activity:**

**Setup:** Choose a complex medical ethics question or logic puzzle

**Part 1: Predictive Model (GPT-4o)**
- Enter prompt
- Note: Fast response (2-5 seconds)
- Read output

**Part 2: Reasoning Model (GPT-5)**
- Enter SAME prompt
- Note: "Thinking..." pause (20+ seconds)
- Watch the thinking process reveal itself
- Read output

**Part 3: Compare**
- Where did GPT-5 catch nuances GPT-4o missed?
- Was the thinking process revealing?
- When would you choose speed vs. depth?

**Speaker Notes:**
- Have this prepared with known good example
- Emphasize: Both models are good, different use cases
- Speed for drafting, reasoning for critical decisions

---

### Slide 9: The "Prompt Lab" (Hands-On Activity - 20 min)
**Exercise:** Transform a lazy prompt into an engineered prompt

**Scenario:** You need to explain a complex concept from your field to a non-expert

**Step 1: Write a "Lazy Prompt"**
```
Explain [your complex concept].
```

**Step 2: Apply the Five Pillars**
- ROLE: Who should the AI be?
- CONTEXT: Who's the audience? Why do they need this?
- TASK: What specifically should be done?
- CONSTRAINTS: Format, length, tone, negative constraints
- THOUGHT PROCESS: How should the AI approach this?

**Step 3: Test Both**
- Run the lazy prompt
- Run the engineered prompt
- Compare outputs

**Step 4: Iterate**
- What worked? What didn't?
- Refine your engineered prompt
- Test again

**Speaker Notes:**
- Circulate and provide feedback
- Share examples of good prompts from participants
- Normalize iteration - first attempt rarely perfect

---

### Slide 10: Group Sharing & Discussion
**Prompt Participants (5 min):**
- "Who wants to share a before/after comparison?"
- "What surprised you about the difference?"
- "Which pillar made the biggest impact?"

**Capture Patterns:**
- Note which pillars participants found most valuable
- Identify common mistakes
- Celebrate creative constraint use

**Key Observations to Highlight:**
- ROLE and CONSTRAINTS often have biggest impact
- THOUGHT PROCESS is powerful for complex tasks
- Iteration improved every prompt

**Speaker Notes:**
- Have 2-3 backup examples if participants are shy
- Write down patterns to reference in future weeks
- Build community through shared learning

---

### Slide 11: The Constraint Toolkit
**Types of Constraints:**

**Format Constraints:**
- "Provide as bulleted list"
- "Create a table with columns X, Y, Z"
- "Use Markdown formatting"

**Length Constraints:**
- "Maximum 100 words"
- "Exactly 5 examples"
- "3-sentence summary"

**Tone Constraints:**
- "Professional but friendly"
- "Technical precision, avoid marketing language"
- "Explain to a 10-year-old"

**Negative Constraints:**  
- "Do NOT include generic advice"
- "Do NOT mention specific drug brands"
- "Do NOT make assumptions beyond the provided data"

**Speaker Notes:**
- Negative constraints are often more powerful than positive ones
- They prevent AI from falling back on generic responses
- Combine multiple constraint types for precision

---

### Slide 12: Advanced Example - Clinical Summarization
**The "Guidelines-Anchored" Summary**

**Goal:** Prevent AI from giving "creative" medical advice

**Engineered Prompt:**
```
ROLE: You are a Clinical Guidelines Specialist.

CONTEXT: I need to create a treatment summary for physician reference.

TASK: Summarize treatment recommendations from the provided guideline.

CONSTRAINTS:
- Use the [NCCN_GUIDELINES] block as the EXCLUSIVE source
- Provide parenthetical citation (section/page) for every recommendation
- If guideline doesn't address a symptom, state: "Guideline does not address  
  this symptom" - do NOT infer solutions
- Maximum 300 words

THOUGHT PROCESS: For each recommendation:
1. Find exact guideline text
2. Note the section/page
3. Only include if explicitly stated
```

**Why This Works:**
- Role sets clinical mindset
- Context clarifies stakes
- Task is specific action
- Constraints prevent creativity (good here!)
- Thought process creates audit trail

**Speaker Notes:**
- This is professional-grade medical prompting
- The constraints create safety
- Show output example if time permits
- This connects to Week 4's verification techniques

---

### Slide 13: More Advanced Constraint Examples

**The "Chain-of-Density" Summary:**
```
First, generate a 50-word summary of the patient's current status.  
Then, identify 3 'missing' technical entities (e.g., specific lab values)  
and re-write the summary to include them while keeping the word count  
under 60. Repeat until the summary is under 75 words but information-dense.
```

**The "Multi-Audience" Delimiter:**
```
Process the [SOURCE_TEXT]. Provide two distinct summaries separated by ---:

Header: Resident Briefing  
Focus on: ML architecture and C-index scores for clinical prediction

Header: Patient Education  
Use a 'sleep-as-a-window' analogy  
Avoid technical terms like 'leave-one-out contrastive learning'
```

**Speaker Notes:**
- These are advanced patterns for later use
- Students don't need to master these today
- But good to know what's possible
- Can return to these as they gain experience

---

### Slide 14: Common Prompting Mistakes

**Mistake #1: Too Vague**
- ❌ "Write about patient safety"
- ✅ "Draft a 200-word patient safety protocol for fall prevention in elderly ICU patients"

**Mistake #2: Asking for Opinion**
- ❌ "What do you think about this treatment?"
- ✅ "Based on the provided guidelines, list contraindications for this treatment"

**Mistake #3: No Constraints**
- ❌ "Summarize this paper"
- ✅ "Create a 3-bullet summary of methodology suitable for a grant proposal"

**Mistake #4: Forgetting Negative Constraints**
- ❌ "Explain statistics to beginners"
- ✅ "Explain statistics to beginners. Do NOT use mathematical notation or assume prior knowledge"

**Mistake #5: Not Iterating**
- First prompt rarely perfect
- Review output, identify gaps, refine prompt
- Prompting is a conversation with yourself

**Speaker Notes:**
- These mistakes are universal - everyone makes them
- The fix is always: more specificity
- Show before/after for each mistake if time permits

---

### Slide 15: Iteration: The Secret to Great Prompts
**The Iteration Cycle:**

**1. Initial Prompt → Output**
```
Explain machine learning for medical applications.
```
*Output: Too technical, too long*

**2. Refine Prompt → Better Output**
```
Explain machine learning for medical applications in 100 words,  
avoiding technical jargon.
```
*Output: Better, but still generic*

**3. Refine Again → Best Output**
```
ROLE: Medical educator  
TASK: Explain machine learning's role in diagnostics  
CONSTRAINTS: 100 words, 8th-grade reading level, include 1 concrete example  
AUDIENCE: Patients considering AI-assisted diagnosis
```
*Output: Clear, specific, appropriate*

**Key Point:** Iteration is expected and encouraged

**Speaker Notes:**
- Professional prompt engineers iterate 3-5 times
- Each iteration teaches you about the model
- Save your iterations to learn patterns

---

### Slide 16: Building Your Prompt Library
**Why Have a Library?**
- Recurring tasks deserve reusable prompts
- Refinement over time improves quality
- Consistency across your work
- Training resource for colleagues

**What to Include:**
1. **Purpose:** What is this prompt for?
2. **The Prompt:** Full text with all five pillars
3. **Notes:** What works well, what to adjust
4. **Examples:** Sample outputs (good and bad)

**Format Suggestions:**
- Document file with sections
- Spreadsheet with columns
- Note-taking app with tags
- Custom GPT (Week 5!)

**Speaker Notes:**
- This week's assignment: Start your library
- You'll use this in Weeks 4-6
- Sharing prompts with colleagues multiplies value

---

### Slide 17: Prompting for Different Models
**Model-Specific Considerations:**

**GPT-5 (Reasoning-First):**
- Add: "Take your time to think through this"
- Expect: Longer responses with visible reasoning
- Best for: Complex logic, math, critical analysis

**GPT-4o (Speed-First):**
- Add: "Provide a concise answer"
- Expect: Fast, streamlined responses
- Best for: Quick drafts, simple questions

**Claude (Nuance-First):**
- Add: "Consider multiple perspectives"
- Expect: Detailed, careful responses
- Best for: Analysis, long documents

**Gemini (Context-First):**
- Add: "Reference specific sections of the provided document"
- Expect: Well-cited, sourced responses
- Best for: Large document analysis

**Speaker Notes:**
- Same prompt works across models, but optimization helps
- This connects back to Week 2's model selection
- You can have model-specific versions in your prompt library

---

### Slide 18: Special Technique - The "Reverse Prompt"
**What is it?**
- Take high-quality writing
- Ask AI: "What prompt would have generated this?"
- Learn from the model's decomposition

**Example:**
```
[Paste excellent patient education handout]

Analyze this text and create a detailed prompt that would generate  
similar content. Include the role, context, task, constraints, and  
thought process that would be needed.
```

**What You Learn:**
- Hidden constraints you didn't notice
- Structural patterns
- Tone calibration techniques
- Audience adaptation strategies

**Speaker Notes:**
- This is an advanced technique
- Great for backup activity if students finish early
- Helps understand "implicit" prompting elements
- Can be homework bonus activity

---

### Slide 19: Key Takeaways
**Remember:**

**The Five Pillars:**
1. ROLE - Who is the AI?
2. CONTEXT - What's the situation?
3. TASK - What specific action?
4. CONSTRAINTS - What are the boundaries?
5. THOUGHT PROCESS - How should AI reason? ⭐

**Best Practices:**
- Roles and Constraints are the most powerful levers for quality
- Reasoning models need "permission" to take their time
- Use delimiters for massive context windows
- Iterate - first prompt is rarely best prompt
- Build a library for recurring tasks

**Connection to Next Week:**
- Week 4: We'll verify these prompts (red-team auditing)
- The better your prompts, the easier verification becomes
- Prompting + Verification = Professional AI use

**Speaker Notes:**
- Emphasize that prompting is a skill that improves with practice
- No one writes perfect prompts immediately
- The five pillars are a framework, not a rigid formula

---

### Slide 20: Looking Ahead - Week 4
**Next Week: Advanced Prompting and Responsible Use**
- Chain-of-Verification (CoVe) pattern
- Red-team auditing
- Identifying logical hallucinations
- Ethics, bias, and privacy

**How This Connects:**
- The prompts you build this week will be verified next week
- Good prompts reduce hallucinations
- But verification is always necessary
- Week 4 adds the "trust but verify" layer

**Assignment for This Week:**
**Build Your Prompt Library**

**Part A: Create 3 Production-Ready Prompts**
1. **A Data Task:** (e.g., Summarizing clinical notes)
2. **A Creative Task:** (e.g., Drafting a department newsletter)
3. **A Logic Task:** (e.g., Finding flaws in research methodology)

**Part B: Test & Refine**
- Run each prompt
- Document what works and what doesn't
- Iterate at least once on each
- Save both versions

**Part C: Comparison (Bonus)**
- Run your "Logic Task" through a Predictive model (GPT-4o)
- Run it through a Reasoning model (GPT-5)
- Did the reasoning model catch something the predictive one missed?
- How much "thinking time" did it take?

**Bring your library to next week's session!**

**Speaker Notes:**
- Emphasize this assignment builds their real toolkit
- These prompts will be used in Weeks 4-6
- Quality over quantity - 3 excellent prompts better than 10 mediocre ones

---

### Slide 21: Questions & Experimentation
**Open Floor:**
- What questions do you have?
- What use cases are you most excited to try?
- What's still confusing?

**Encourage:**
- Experiment this week
- Share discoveries with each other
- Don't be afraid to "fail" - every bad output teaches you something

---

## Teaching Tips

### Time Management (50 min)
- Slides 1-3: Welcome & Intro (5 min)
- Slides 4-8: Five Pillars & Techniques (12 min)
- Slide 9-10: Hands-On Prompt Lab & Discussion (20 min)
- Slides 11-18: Advanced Techniques & Best Practices (10 min)
- Slides 19-21: Wrap-up & Assignment (3 min)

### Critical Demonstrations
**Must Prepare:**
1. Five Pillars example (Slide 5) - have both prompts ready to run live
2. Reasoning vs. Prediction demo (Slide 8) - know your example
3. Delimiter example (Slide 7) - show with/without

### Common Student Questions

**Q: "If the model is so smart, why do I need to be so specific?"**
A: "Think of it like directing a very talented intern. They have the skills, but they need to know YOUR standards and YOUR priorities. A smart intern still needs a clear project brief."

**Q: "How long should my prompts be?"**
A: "As long as necessary, as short as possible. For complex tasks, 200-300 words is normal for professional prompts. For simple tasks, 50 words might suffice. Clarity matters more than brevity."

**Q: "Should I always use all five pillars?"**
A: "No! They're a toolkit, not a requirement. Quick questions might only need a TASK. Complex work benefits from all five. Use judgment."

**Q: "Can I save prompts and reuse them?"**
A: "Absolutely! That's the whole point of a prompt library. For recurring tasks, reusable prompts save time and ensure consistency."

**Q: "Do different models need different prompts?"**
A: "Same prompt usually works, but optimization helps. Reasoning models benefit from explicit permission to think. Fast models benefit from brevity cues. Start universal, optimize if needed."

### Backup Activities

**If Students Finish Early:**
1. **Reverse Prompt Exercise:** Give them excellent writing, ask them to deduce the prompt
2. **Peer Review:** Have students swap prompts and suggest improvements
3. **Challenge Prompts:** Provide difficult scenarios to prompt for

**If Running Behind:**
- Skip Slides 16-18 (advanced content)
- Reduce Prompt Lab to 15 minutes
- Assign more exploration as homework

**If Technical Issues:**
- Have screenshots of good/bad prompt outputs
- Can do prompting exercise on paper, test later
- Peer discussion can continue without live demos

### Adaptation Notes

**For Advanced Participants:**
- Introduce "few-shot prompting" (providing examples)
- Discuss "system prompts" vs. "user prompts"
- Preview Custom GPTs (Week 5) where prompts become persistent
- Challenge: Create prompts for edge cases

**For Struggling Participants:**
- Provide prompt templates to fill in
- Do first prompt lab example as guided group activity
- Pair with more advanced participants
- Reduce assignment to 2 prompts instead of 3

**For Different Domains:**
- Have domain-specific examples ready (clinical, research, admin)
- Ask participants to share their domain challenges
- Crowdsource prompt solutions
- Build discipline-specific prompt libraries

---

*Week 3 Complete - Ready for Week 4: Verification & Red-Teaming*
