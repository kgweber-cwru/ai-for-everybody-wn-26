# Week 1: Introduction to Generative AI
## Student Handout

---

## Welcome to the Series!

Over the next six weeks, you'll learn to effectively use generative AI tools in your work. No coding required - this series focuses on practical applications and smart usage patterns.

---

## What Are Large Language Models?

**Simple Definition:** AI systems trained on massive amounts of text that can generate human-like responses by predicting what comes next.

**Key Concept:** They're **prediction machines**, not knowledge databases or search engines.

**Think of it like:** Super-powered autocomplete that understands context and can write full paragraphs, not just suggest the next word.

---

## How LLMs Work (Conceptually)

### Tokens
- Not words - chunks of text
- Roughly 3-4 characters or 0.75 words
- "Hello world!" ≈ 3 tokens
- Why this matters: Models have token limits (context windows)

### Prediction
- Reads all previous tokens
- Predicts most likely next token
- Repeats billions of times
- Generates coherent text

### Temperature
- Controls randomness (0 = very predictable, 2 = very creative)
- Lower for factual tasks, higher for creative work
- Most interfaces use moderate default (~0.7)

---

## Major Models Available Today

| Model | Company | Free Tier | Best For |
|-------|---------|-----------|----------|
| **ChatGPT** | OpenAI | Yes (GPT-4o-mini) | General purpose, coding |
| **Claude** | Anthropic | Yes (limited) | Long documents, nuanced writing |
| **Gemini** | Google | Yes | Integration with Google services |
| **Copilot** | Microsoft | With M365 | Enterprise integration |

**Note:** Capabilities and pricing change frequently. Free tiers are sufficient for learning.

---

## What CAN LLMs Do?

✓ **Writing & Editing**
- Draft emails, reports, summaries
- Improve clarity and tone
- Expand bullet points into prose
- Condense long text

✓ **Research Support**
- Explain complex concepts
- Summarize information
- Generate research questions
- Brainstorm approaches

✓ **Learning & Explanation**
- ELI5 (Explain Like I'm 5) complex topics
- Create analogies and examples
- Answer questions
- Tutor on subjects

✓ **Data Interpretation**
- Suggest analysis approaches
- Explain statistical concepts
- Help interpret results
- Generate hypotheses

✓ **Creative Tasks**
- Brainstorming ideas
- Writing different perspectives
- Creating examples and scenarios
- Generating variations

---

## What CAN'T LLMs Do? (Critical Limitations)

✗ **Access Real-Time Information**
- Knowledge has cutoff dates
- Can't browse the internet (without tools)
- Won't know today's news or recent events

✗ **Guarantee Factual Accuracy**
- Can "hallucinate" - create plausible but false information
- May confidently state wrong facts
- Always verify important information

✗ **True Reasoning**
- No logical reasoning in traditional sense
- Pattern matching, not understanding
- Can miss obvious logical flaws

✗ **Remember Everything**
- Context window limits (though large)
- Can't reference things from previous conversations
- Needs context provided in each chat

✗ **Math & Counting**
- Often struggles with arithmetic
- May miscount items or words
- Use calculator for important calculations

✗ **Cite Sources Reliably**
- May generate fake citations
- Can't properly attribute information
- Use specialized tools for citation

---

## Example Prompts to Try

### 1. Explanation Tasks
```
Explain [complex concept] in simple terms for someone with 
no background in [field].
```
**Example:** "Explain CRISPR gene editing in simple terms for someone with no biology background."

### 2. Summarization
```
Summarize the following in 3 sentences: [text]
```

### 3. Perspective-Taking
```
What are the potential advantages and disadvantages of [topic] 
from the perspective of [stakeholder]?
```
**Example:** "What are potential advantages and disadvantages of telemedicine from a patient perspective?"

### 4. Brainstorming
```
Generate 5 creative ideas for [goal].
```
**Example:** "Generate 5 creative ideas for explaining informed consent to pediatric patients."

### 5. Format Transformation
```
Convert these bullet points into a professional email: [points]
```

### 6. Learning Aid
```
I'm studying [topic]. Can you create a simple quiz with 5 questions 
and provide the answers separately?
```

---

## Hands-On Exercises

### Exercise 1: Account Setup (Do During Session)
1. Go to chat.openai.com
2. Sign up with email
3. Verify email
4. Log in and explore interface

Repeat for:
- Claude.ai
- (Optional) Gemini.google.com

### Exercise 2: First Prompts (Do During Session)
Try these three prompts and notice the differences:

**Prompt 1:** "What is photosynthesis?"

**Prompt 2:** "Explain photosynthesis to a 10-year-old."

**Prompt 3:** "Explain photosynthesis to a 10-year-old using a cooking analogy."

**Reflection:** How did the responses differ? Which was most helpful?

### Exercise 3: Real-World Application
Think of a task from YOUR work. Try prompting the AI to help with it. Examples:
- Explain a concept to a patient
- Summarize a research article abstract
- Draft an email
- Brainstorm research questions
- Create teaching materials

**Note what works and what doesn't.**

---

## Take-Home Exercise (Due Next Week)

### Assignment: Model Comparison

**Task:** Test the same prompt on both ChatGPT and Claude, then compare.

**Your Prompt:** Choose something relevant to your work. Examples:
- "Summarize current treatment guidelines for [condition]"
- "Explain [statistical concept] in simple terms"
- "Generate 5 potential research questions about [topic]"
- "Draft a patient education handout about [topic]"

**Instructions:**
1. Write your prompt clearly
2. Enter the EXACT same prompt in ChatGPT (chat.openai.com)
3. Enter the EXACT same prompt in Claude (claude.ai)
4. Save or screenshot both responses

**Compare:**
- Which response was more helpful? Why?
- How did the responses differ in:
  - Length?
  - Tone?
  - Accuracy (if you can verify)?
  - Organization?
  - Usefulness?
- Did either hallucinate or make errors?

**Write 2-3 paragraphs** about your observations. Bring to next session.

**Bonus:** Try a third model (Gemini) for additional comparison.

---

## Common Questions

**Q: Is my data safe?**
A: Assume conversations may be used for training (check privacy policies). Don't share:
- Patient information (PHI)
- Proprietary data
- Confidential information
- Personal identifiers

**Q: Can I use AI-generated text in my work?**
A: Depends on context:
- Check your institution's AI policy
- For academic work: disclose AI use
- For patient care: review and verify everything
- For research: follow journal guidelines
- Always review and edit AI output

**Q: Why did it refuse my request?**
A: Safety guardrails prevent harmful content. If legitimate request refused:
- Rephrase more clearly
- Remove potentially triggering words
- Be more specific about benign intent
- Try different model

**Q: It got something wrong. Should I tell it?**
A: Yes! You can correct it in the conversation:
- "Actually, that's incorrect because..."
- "Let me clarify..."
- It will adjust its responses

**Q: How do I know if it's hallucinating?**
A: Warning signs:
- Overly confident about obscure facts
- Provides citations you can't verify
- Claims specific dates/numbers without caveat
- Contradicts known information
**Always verify important claims**

---

## Tips for Success

**DO:**
- ✓ Experiment freely
- ✓ Iterate on prompts
- ✓ Verify important information
- ✓ Use as starting point, not final answer
- ✓ Learn from "failures"
- ✓ Ask for clarification or revision

**DON'T:**
- ✗ Trust blindly
- ✗ Share sensitive information
- ✗ Expect perfection
- ✗ Use for critical decisions without verification
- ✗ Assume it knows current events
- ✗ Treat it as a search engine

---

## Resources

### Official Documentation
- **OpenAI Help:** help.openai.com
- **Anthropic Docs:** docs.anthropic.com
- **Google Gemini:** support.google.com/gemini

### Learning More
- Check your institution's AI guidelines
- Join discussions with colleagues
- Follow AI news (landscape changes rapidly)
- Practice regularly

---

## Looking Ahead

**Next Week: Model Differences and Selection**
- Deep comparison of major models
- When to use which model
- Understanding capabilities
- Hands-on testing

**Bring your comparison assignment and questions!**

---

## Notes & Observations

Use this space to jot down notes during the session:

**Things that worked well:**


**Questions I have:**


**Ideas for using this in my work:**


**Challenges or concerns:**

---

## Quick Reference Card

**Getting Started:**
1. Go to model website
2. Sign up with email
3. Start new chat
4. Type prompt
5. Review response
6. Iterate as needed

**Remember:**
- Clear, specific prompts work best
- You can ask it to revise
- Always verify important facts
- Experimentation is key
- It's okay to start simple

---

*Questions? Bring them to next week's session or email [your contact]*
