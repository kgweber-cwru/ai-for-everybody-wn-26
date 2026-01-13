# Week 2: Model Differences and Selection
## Instructor Notes (Convert to Slides)

---

### Slide 1: Title & Review
**Title:** Understanding and Using Generative AI  
**Subtitle:** Week 2 - Model Differences and Selection

**Quick Review:**
- Last week: What are LLMs?
- Key concepts: prediction, tokens, limitations
- This week: Which model for which task?

**Speaker Notes:**
- Welcome back
- Quick discussion of Week 1 assignment
- Who found interesting differences?
- Set expectations for today's hands-on comparisons

---

### Slide 2: Assignment Discussion
**Prompt:**
What did you discover in your model comparisons?

**Discussion Points:**
- Length differences
- Tone/style variations
- Accuracy differences
- Which felt more helpful?

**Speaker Notes:**
- Spend 5-10 minutes on this
- Capture themes on board/screen
- Use their observations to intro today's content
- Validate their findings

---

### Slide 3: Today's Goals
**We'll Cover:**
- Major models in depth
- Key differences and strengths
- When to use which model
- Context windows explained
- Multimodal capabilities
- Hands-on comparative testing

---
### Slide 4: The Main Players (Updated Landscape)
**OpenAI - The GPT-5 & O-Series**

- GPT-5: The flagship general-purpose agent. Unifies high-speed interaction with deep reasoning.
- GPT-4.1: The "High-Context" Specialist (1M tokens). Ideal for massive document analysis.
- GPT-4o: The "Interface" model. Optimized for real-time voice and low-latency chat.

**Anthropic - Claude 4.5 Family**

- Claude 4.5 Opus: The frontier model for "Computer Use" and autonomous coding.
- Claude 4.5 Sonnet: The industry standard for "Vibe Coding" and nuanced writing.
- Extended Thinking: A new native toggle allowing models to "pause and reason" for minutes on complex logic.

**Google - Gemini 3 Series**

- Gemini 3 Pro: The reasoning leader. Features "Deep Think" mode for PhD-level science/math.
- Gemini 3 Flash: Now the default "fast" model, outperforming 2024-era flagship models.
- Gemini Agent: A dedicated interface for multi-step tasks across Workspace (Gmail/Docs/Calendar).

---

### Slide 5: GPT-5 vs. 4.1 vs. 4o (In-House Comparison)

**GPT-5: The "Digital Employee"**

- Best For: Strategic planning, multi-step research, and autonomous tasks.
- Key Strength: Integrated "Thinking" engine that significantly reduces hallucinations in technical work.

**GPT-4.1: The "Librarian"**

- Best For: Analyzing 500+ page PDFs, entire legal case files, or large codebases.
- Key Strength: A 1-million-token context window—it rarely "forgets" details from the beginning of a massive file.

**GPT-4o: The "Communicator"**

- Best For: Quick Q&A, drafting emails, and real-time voice collaboration.
- Key Strength: Most "human-like" voice and fastest response time for low-stakes tasks.

**Speaker Notes:**
- Most widely known
- Strengths in technical tasks
- Good "default" choice
- Paid tier adds many features

---

### Slide 6: Claude (Anthropic) - Strengths

**Best For:**
- Long document analysis
- Nuanced writing and editing
- Complex instructions
- Maintaining conversation flow
- Careful, thoughtful responses

**Characteristics:**
- Often more verbose
- Tends toward safer/more cautious responses
- Excellent at maintaining context
- Strong ethical reasoning
- Very good at following complex instructions

**Context Window:** 200K tokens (Claude 3.5 Sonnet)

**Speaker Notes:**
- Newer player, rapidly improving
- Very large context window (important!)
- Often preferred for writing tasks
- More conversational tone

---

### Slide 7: Gemini (Google) - Strengths

**Best For:**
- Google Workspace integration
- Real-time information needs
- Multilingual tasks
- Video/multimodal inputs
- Research across Google services

**Characteristics:**
- Integrated with Google services
- Can access current information
- Strong at summarization
- Multimodal from the start

**Context Window:** Up to 1M tokens (Gemini 1.5)

**Speaker Notes:**
- Advantage: Google ecosystem
- Can work with Gmail, Docs, etc.
- Massive context window
- Less commonly used standalone

---

### Slide 8: Context Windows Explained

**What is Context?**
- Everything the model can "see" at once
- Your prompt + conversation history + its responses
- Measured in tokens

**Why It Matters:**
- Long documents need large context
- Long conversations hit limits
- Summarization might be needed

**Comparison:**
- GPT-4o: ~128K tokens (~96K words)
- Claude 3.5: ~200K tokens (~150K words)
- Gemini 1.5: ~1M tokens (~750K words)

**Speaker Notes:**
- Analogy: Model's "working memory"
- Bigger = can handle longer inputs
- Most users rarely hit these limits
- Matters for long document analysis

---

### Slide 9: Multimodal Capabilities

**Text + Images:**
- GPT-4o: ✓ (upload images, describe, analyze)
- Claude 3.5: ✓ (upload images, PDFs)
- Gemini: ✓ (images, video)

**Text + Voice:**
- ChatGPT: ✓ (voice mode on mobile)
- Claude: ✗ (text only currently)
- Gemini: ✓ (some integration)

**Image Generation:**
- ChatGPT: ✓ (DALL-E 3, paid tier)
- Claude: ✗
- Gemini: Limited (Imagen)

**Speaker Notes:**
- Show examples if possible
- Demonstrate image upload
- Note: capabilities expanding rapidly
- Different models better at different modalities

---

### Slide 10: Model "Personalities"

**ChatGPT:**
- Professional
- Concise
- Structured
- Confident

**Claude:**
- Thoughtful
- Verbose
- Nuanced
- Careful/cautious

**Gemini:**
- Informative
- Integrated
- Current
- Google-flavored

**Speaker Notes:**
- These are generalizations
- Can be adjusted with prompting
- Personality matters for user experience
- Some prefer one over others for style alone

---

### Slide 11: Speed and Responsiveness

**Factors:**
- Model size (larger = slower)
- Server load
- Response length
- Complexity of task

**Generally:**
- Mini/small models: Fastest
- Standard models: Moderate
- Large models: Slower but more capable

**Trade-off:** Speed vs. capability

**Speaker Notes:**
- Test real-time if possible
- For most uses, all fast enough
- Matters more for high-volume use
- Can select smaller models when speed critical

---

### Slide 12: Cost Considerations

**Free Tiers:**
- ChatGPT: Yes (GPT-4o-mini)
- Claude: Yes (with limits)
- Gemini: Yes

**Paid Options (~$20/month):**
- ChatGPT Plus: GPT-4o unlimited
- Claude Pro: Higher limits, priority access
- Gemini Advanced: Best model, integration

**For API Use:**
- Pricing per token
- GPT-4o-mini: Cheapest
- Varies by model

**Speaker Notes:**
- Free tiers sufficient for learning/light use
- Paid worth it for heavy users
- API costs matter for developers
- Price competition benefits users

---

### Slide 13: When to Use Which Model?

**Decision Matrix:**


If your task is...,Use this Model,Why?
Analyzing 20 legal contracts,GPT-4.1,Highest context window; won't lose details.
Solving a complex physics problem,Gemini 3 (Deep Think),"Highest ""thinking"" benchmarks for STEM."
"Writing a 2,000-word blog post",Claude 4.5 Sonnet,"Best narrative flow and human-like ""voice."""
Building a multi-file Python app,GPT-5 or Claude 4.5 Opus,"Elite at ""Agentic"" coding and debugging."
Quickly checking a grammar rule,GPT-4o or 3 Flash,"Instant speed; low ""compute"" cost."

---

### Slide 14: Hands-On Comparative Testing

**Activity (20 minutes):**

Test the same prompts across models and compare:

**Test Prompts:**
1. Summarization task
2. Writing task
3. Explanation task
4. Creative task

**What to Compare:**
- Response quality
- Length and detail
- Accuracy
- Tone and style
- Speed

**Speaker Notes:**
- Provide specific test prompts (on handout)
- Participants work individually
- Capture observations for discussion
- Circulate and help

---

### Slide 15: Test Prompt 1 - Summarization

**Prompt:**
```
Summarize this abstract in 2-3 sentences for a general audience:

[Provide a sample medical/research abstract]
```

**Test Across:**
- ChatGPT
- Claude
- (Optional) Gemini

**Note:**
- Clarity
- Accuracy
- Accessibility

---

### Slide 16: Test Prompt 2 - Writing

**Prompt:**
```
Draft a professional email to a colleague explaining why our 
research meeting needs to be rescheduled. Keep it under 100 words.
```

**Compare:**
- Tone
- Length
- Structure
- Politeness

---

### Slide 17: Test Prompt 3 - Explanation

**Prompt:**
```
Explain the concept of statistical significance to someone with 
no statistics background. Use an analogy.
```

**Compare:**
- Clarity
- Analogy quality
- Accuracy
- Helpfulness

---

### Slide 18: Test Prompt 4 - Creative/Brainstorming

**Prompt:**
```
Generate 5 creative ideas for teaching medical students about 
empathy in patient care.
```

**Compare:**
- Creativity
- Practicality
- Variety
- Inspiration

---

### Slide 19: Group Discussion

**Share Findings:**
- Which model performed best for each task?
- Did results surprise you?
- Did you notice patterns?
- Any clear winners or losers?

**Key Point:** Different models excel at different tasks

**Speaker Notes:**
- Facilitate discussion
- Summarize patterns observed
- No wrong answers
- Build on their observations

---

### Slide 20: Advanced Features Overview

**Quick Tour of Special Features:**

**ChatGPT:**
- Custom GPTs (paid)
- Memory (optional)
- Plugins (paid)
- Canvas mode

**Claude:**
- Projects (organize conversations)
- Artifacts (structured outputs)
- Large document handling

**Gemini:**
- Google Workspace extensions
- Real-time search
- YouTube integration

**Speaker Notes:**
- Brief overview only
- Will cover some in Week 5
- Many features require paid tiers
- Landscape constantly evolving

---

### Slide 21: Key Takeaways

**Remember:**
- No single "best" model - depends on task
- Experiment to find what works for you
- Consider: accuracy, style, speed, cost
- You can use different models for different purposes
- Capabilities constantly improving

---

### Slide 22: Looking Ahead - Week 3

**Next Week: Prompt Engineering Fundamentals**
- How to write effective prompts
- Getting better results
- Common patterns and techniques
- Iterating and improving

**Assignment:**
- Choose your "default" model
- Use it for 3-5 real tasks this week
- Document what works and what doesn't
- Note where you wish it performed better

---

### Slide 23: Questions & Discussion

**Q&A**

---

## Teaching Tips

### Time Management (50 min)
- Review/Discussion: 10 min
- Slides 3-13: Concepts (15 min)
- Slides 14-18: Hands-on (20 min)
- Slides 19-23: Discussion & wrap-up (5 min)

### Demonstrations

**Have Ready:**
- Same prompt in multiple models
- Screenshots or live demos
- Examples of successes and failures
- Multimodal examples (if available)

### Common Questions

**Q: Which model should I pay for?**
A: Depends on usage patterns. Most can start with free tiers. If hitting limits, choose based on primary use case.

**Q: Can I use multiple models?**
A: Absolutely! Many people use different models for different tasks.

**Q: Why does one model refuse what another allows?**
A: Different safety policies and training. Can rephrase or try different model.

**Q: Do they get better over time?**
A: Yes! Models are regularly updated. What's true today may change.

### Adaptation Tips

**If Participants Favor One Model:**
- Acknowledge preference is fine
- Show where others excel
- Encourage occasional experimentation

**If Technical Issues:**
- Have backup screenshots
- Can do group demonstrations
- Pair participants

**For Advanced Users:**
- Discuss API differences
- Cover advanced features more
- Touch on fine-tuning concepts

### Keep It Practical

**Emphasize:**
- Real-world task selection
- Personal workflow integration
- It's okay to have favorites
- Experimentation over perfection

---

## Additional Resources for You

**Model Documentation:**
- OpenAI: platform.openai.com/docs
- Anthropic: docs.anthropic.com
- Google: ai.google.dev

**Comparison Resources:**
- Artificial Analysis (benchmarks)
- User communities (Reddit, etc.)
- Tech news coverage

**Stay Updated:**
- Models update frequently
- New features added regularly
- Pricing changes occasionally
- Competition drives improvement
