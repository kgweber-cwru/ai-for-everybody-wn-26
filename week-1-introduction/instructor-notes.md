# Week 1: Introduction to Generative AI
## Instructor Notes (Convert to Slides)

---

### Slide 1: Title & Welcome
**Title:** Understanding and Using Generative AI  
**Subtitle:** Week 1 - Introduction to Generative AI  
**Your Name & Affiliation**

**Speaker Notes:**
- Welcome participants
- Quick poll: Who has used ChatGPT? Claude? Other AI tools?
- Set expectations: hands-on, practical focus
- No coding required!

---

### Slide 2: What We'll Cover Today
**Bullet Points:**
- What are large language models (LLMs)?
- How do they work? (conceptual overview)
- Current landscape: Major players
- Hands-on: First experiments

**Speaker Notes:**
- This is a foundation week - concepts, not technical details
- We'll get hands-on in about 20 minutes
- Questions welcome throughout

---

### Slide 3: What is a Large Language Model?
**Key Points:**
- AI systems trained on vast amounts of text
- Learn patterns in language
- Generate human-like text by predicting what comes next
- NOT search engines - they're prediction machines
- NO real-time information or internet access (without tools)

**Visual Suggestion:** Simple diagram showing text input → model → text output

**Speaker Notes:**
- Analogy: Like autocomplete on steroids
- They don't "know" things - they predict statistically likely continuations
- This is important for understanding their limitations
- Knowledge cutoff dates vary by model

---

### Slide 4: How Do LLMs Work? (Simplified)
**Concepts to Cover:**
- **Tokens:** Not words - chunks of text (roughly 3-4 characters)
  - "Hello world" ≈ 2-3 tokens
  - This matters for context limits and costs
- **Prediction:** Model predicts next token based on all previous tokens
- **Probability:** Many possible next tokens, picks based on likelihood
- **Temperature:** Controls randomness (we'll explore this more)

**Visual Suggestion:** Simple flowchart or animation concept

**Speaker Notes:**
- Don't get too technical - focus on "prediction machine" concept
- The token concept helps explain why they sometimes struggle with spelling/counting
- This prediction process happens billions of times

---

### Slide 5: The Current Landscape
**Major Players:**
- **OpenAI:** ChatGPT (GPT-4o, GPT-4o-mini)
- **Anthropic:** Claude (Sonnet, Opus)
- **Google:** Gemini
- **Others:** Microsoft Copilot, Perplexity, etc.

**Key Point:** Each has different strengths, capabilities, and pricing

**Speaker Notes:**
- Landscape changes rapidly
- We'll compare these in detail next week
- Most offer free tiers for experimentation
- Different use cases may favor different models

---

### Slide 6: What Can LLMs Do?
**Applications:**
- Writing assistance (drafting, editing, summarizing)
- Research support (literature review, synthesis)
- Data analysis and interpretation
- Brainstorming and ideation
- Learning and explanation
- Translation and transformation
- Code generation (for those who want it)

**Speaker Notes:**
- Ask audience: What do you hope to use AI for?
- In medical/academic context: patient education, research summaries, grant writing
- Important: AI as assistant, not replacement

---

### Slide 7: What Can't LLMs Do? (Limitations)
**Key Limitations:**
- **No real-time data** (unless specifically connected)
- **Hallucinations:** Can confidently state false information
- **No reasoning** in traditional sense - pattern matching
- **Context limits:** Can't remember everything forever
- **Biases:** Reflect biases in training data
- **Math/counting:** Often struggle with arithmetic
- **Cannot cite sources** reliably (without RAG systems)

**Speaker Notes:**
- This is crucial to understand
- "Hallucinations" = plausible-sounding but wrong
- Always verify critical information
- These limitations are being actively worked on

---

### Slide 8: Real Example - Hallucination
**Show actual example:**
- Prompt: "Tell me about the 2024 Nobel Prize in Medicine"
- Response might include plausible but fictional winners
- Or accurate info if in training data

**Key Point:** Always verify important facts

**Speaker Notes:**
- Have a real example ready
- This is why we need critical evaluation
- More reliable with proper prompting (Week 3-4)

---

### Slide 9: Getting Started - Account Setup
**What You Need:**
- Email address
- Internet access
- That's it!

**Today's Activity:**
- Create ChatGPT account (free tier)
- Create Claude account (free tier)
- Optional: Gemini

**Speaker Notes:**
- Walk through signup process together
- Mention: Free tiers sufficient for this course
- Some features require paid tiers (note which)
- Privacy note: Don't share sensitive data

---

### Slide 10: The Interface Tour
**Key Elements:**
- Chat window
- Conversation history
- New chat button
- Model selection (if available)
- Settings/preferences

**Speaker Notes:**
- Live demonstration
- Show on both ChatGPT and Claude
- Point out differences in interfaces
- Mention: conversation history helpful but not required

---

### Slide 11: Your First Prompts
**Demonstration Prompts:**
1. "Explain quantum computing to a 10-year-old"
2. "Summarize the concept of homeostasis"
3. "Write a haiku about research"

**What to Notice:**
- How quickly it responds
- The style and tone
- Level of detail
- Any limitations or errors

**Speaker Notes:**
- Type these live
- Show real-time responses
- Discuss what worked, what didn't
- Different models may respond differently

---

### Slide 12: Hands-On Exercise (20 min)
**Individual Exploration:**
1. Create your accounts
2. Try 3-5 prompts related to YOUR work
3. Experiment with:
   - Questions
   - Writing requests
   - Explanations
4. Note what surprises you (good or bad)

**We'll Reconvene to Discuss**

**Speaker Notes:**
- Circulate and help
- Encourage experimentation
- Remind: no "wrong" prompts
- Help troubleshoot account issues

---

### Slide 13: Discussion - What Did You Notice?
**Prompting Questions:**
- What worked well?
- What was surprising?
- Any frustrations or limitations?
- Ideas for how you might use this?

**Speaker Notes:**
- Capture common themes
- Address misconceptions
- Build on successes
- Validate frustrations
- Segue to next week's topics

---

### Slide 14: Week 1 Key Takeaways
**Remember:**
- LLMs predict text, don't "know" facts
- They can hallucinate - always verify
- Different models have different strengths
- Experimentation is key to learning
- Start with simple, clear prompts

---

### Slide 15: Looking Ahead - Week 2
**Next Week:**
- Deep dive into model differences
- When to use which model
- Comparative testing
- Understanding capabilities and limitations

**Assignment:**
- Experiment with the same task on ChatGPT and Claude
- Document differences
- Bring questions!

---

### Slide 16: Questions & Resources
**Resources:**
- OpenAI Help Center
- Anthropic Documentation
- This week's handout (examples and exercises)

**Q&A Time**

**Speaker Notes:**
- Leave 5-10 minutes for questions
- Collect questions you can't answer for next time
- Encourage ongoing experimentation

---

## Teaching Tips

### Time Management (50 min total)
- Slides 1-8: Concepts (20 min)
- Slides 9-11: Demo (10 min)
- Slide 12: Hands-on (15 min)
- Slides 13-16: Discussion & wrap-up (5 min)

### Common Questions & Answers

**Q: Is AI going to replace my job?**
A: These tools augment human capabilities, not replace human judgment. Think assistant, not replacement. In your field, domain expertise remains critical.

**Q: Can I trust the information it gives me?**
A: Always verify important information. These tools are best for drafts, brainstorming, and starting points - not final answers.

**Q: Why does it sometimes refuse requests?**
A: Safety guardrails prevent harmful content. Sometimes overly cautious. You can usually rephrase.

**Q: Does it remember our previous conversations?**
A: Within a chat session, yes. Across sessions, no (unless features like "memory" enabled).

**Q: How much does this cost?**
A: Free tiers sufficient for learning. Paid tiers: ~$20/month for unlimited access.

### Troubleshooting

**Account Creation Issues:**
- Email verification delays: Check spam
- Phone verification: Use real number
- Geographic restrictions: Rare but possible

**Access Issues:**
- Server overload: Try different time
- Browser issues: Try incognito/different browser
- Network blocks: Some institutions block AI tools

### Adaptations

**For Different Audiences:**
- **Clinicians:** Emphasize patient education, documentation
- **Researchers:** Focus on literature review, writing support
- **Administrators:** Highlight communication, reporting
- **Mixed:** Use examples from multiple domains

**If Running Short on Time:**
- Reduce hands-on to 10 min
- Skip some demonstration prompts
- Assign extra exploration for homework

**If Running Long:**
- More comparative demonstrations
- Deeper discussion of limitations
- Preview more advanced features

### Energy & Engagement

**Keep It Interactive:**
- Frequent check-ins: "Has anyone tried X?"
- Show failures too - they're instructive
- Encourage questions throughout
- Celebrate discoveries

**Make It Relevant:**
- Use examples from participants' domains
- Ask about their use cases
- Connect to real work challenges
- Build on their expertise

### Assessment (Informal)

**By End of Session, Participants Should:**
- Have active accounts
- Understand basic concept of LLMs
- Know key limitations
- Have tried 3-5 prompts
- Be curious to explore more

---

## Backup Plans

**If Technology Fails:**
- Have screenshots/videos of interface
- Use your own account to demonstrate
- Can do group demo if individual access issues
- Send handout via email if can't print

**If Participants Are Very Advanced:**
- Move faster through basics
- Go deeper on limitations/architecture
- Preview advanced topics
- Focus on edge cases

**If Participants Are Struggling:**
- Slow down demonstrations
- More step-by-step guidance
- Pair up participants
- Schedule optional office hours
