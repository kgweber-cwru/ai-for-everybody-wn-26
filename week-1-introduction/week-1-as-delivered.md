# AI For Everybody

Markdown version of https://docs.google.com/presentation/d/1mfxxFAans-Tla_iMEjkx8Fm-vPrIKKNs8sEXM1LNtSo/edit?usp=sharing

# Week 1: Introduction to Generative AIKate Weber, Ph.D.Faculty Director for AI in Medical Education, CWRU

---

- Welcome participants
- Quick poll: Who has used ChatGPT? Claude? Other AI tools?
- Set expectations: hands-on, practical focus
- No coding required!

# What We’ll Cover Today

What is Artificial Intelligence?

What are Large Language Models (LLMs)?

How do they work?

Current landscape: Major Players

Hands-on: First Experiments

Slides and Handouts:https://drive.google.com/drive/folders/1zz9904yxp4vRXJ7MymSB6BXXWaAGr8nc

---

- This is a foundation week - concepts, not technical details
- We'll get hands-on in about 20 minutes
- Questions welcome throughout

# “Artificial Intelligence” is a bit vague

<span style="color:#ffffff"> __Machine Learning__ </span>

<span style="color:#ffffff"> __Rules / Expert Systems__ </span>

<span style="color:#ffffff">Statistical Methods to teach an algorithm to predict patterns</span>

<span style="color:#ffffff">Decision Trees, Logical rules</span>

<span style="color:#5e5e5e">Generative models that can take in images, text, audio, etc., and respond with the like</span>

<span style="color:#5e5e5e">Specialized Deep Learning tools first designed for Natural Language Processing</span>

<span style="color:#ffffff">Highly-Complex neural networks launched by access to GPUs</span>

# Tech under the “AI” Umbrella Today

Chatbots

Speech Recognition and Translation

Image Generation

Document Generation, Summarization

Video Production

Software Generation

Research Support

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_0.png)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_1.png)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_2.png)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_3.png)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_4.png)

# What is a Large Language Model (LLM)?

- AI systems trained on vast amounts of text

- Learn patterns in language

- Generate human-like text by predicting what comes next

- NOT search engines - they're prediction machines

- NO real-time information or internet access (without tools)

---

- Analogy: Like autocomplete on steroids
- They don't "know" things - they predict statistically likely continuations
- This is important for understanding their limitations
- Knowledge cutoff dates vary by model
- They need guardrails - the training data can be pretty toxic

# How do they work?

__Tokens__  - chunks of text

__Prediction__  - predicts next token based on all previous tokens

__Probability__  - Many possible tokens - what’s most likely?

__Temperature__  - Adds randomness

_[https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer)_

---

- Don't get too technical - focus on "prediction machine" concept
- The token concept helps explain why they sometimes struggle with spelling/counting
- This prediction process happens billions of times

# A Probability Machine at Work

The quick brown fox jumps over the lazy ___

The quick brown fox jumps over the lazy  <span style="color:#a64d79">horse</span>  [0.76]

The quick brown fox jumps over the lazy  <span style="color:#a64d79">tomato</span>  [0.55]

The quick brown <span style="color:#741b47"> </span> fox <span style="color:#741b47"> </span> jumps over the lazy  <span style="color:#a64d79">dog</span>  [0.99]

# The current landscape

__Major Players:__

__OpenAI__  (ChatGPT)

__Anthropic__  (Claude)

__Google__  (Gemini)

__Others__  - Microsoft Copilot, Perplexity, etc

Each has different strengths, capabilities, and pricing

---

- Landscape changes rapidly
- We'll compare these in detail next week
- Most offer free tiers for experimentation
- Different use cases may favor different models
- Experiment and find one that works with your style

# What can LLMs Do?

- Writing assistance (drafting, editing, summarizing)

- Research support (literature review, synthesis)

- Data analysis and interpretation

- Brainstorming and ideation

- Learning and explanation

- Translation and transformation

- Code generation (for those who want it)

---

- Ask audience: What do you hope to use AI for?
- In medical/academic context: patient education, research summaries, grant writing
- Important: AI as assistant, not replacement

-  __No real-time data__  (unless specifically connected)

-  __Hallucinations__ : Can confidently state false information

-  __No reasoning in traditional sense__  - pattern matching

-  __Context limits__ : Can't remember everything forever

-  __Biases__ : Reflect biases in training data

-  __Math/counting__ : Often struggle with arithmetic

-  __Cannot cite sources__  reliably (without RAG systems)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_5.png)

---

- This is crucial to understand
- "Hallucinations" = plausible-sounding but wrong
- Always verify critical information
- These limitations are being actively worked on
- The Connections Test

-  __No real-time data__  (unless specifically connected)

-  __Hallucinations__ : Can confidently state false information

-  __No reasoning in traditional sense__  - pattern matching

-  __Context limits__ : Can't remember everything forever

-  __Biases__ : Reflect biases in training data

-  __Math/counting__ : Often struggle with arithmetic

-  __Cannot cite sources__  reliably (without RAG systems)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_6.png)

---

- This is crucial to understand
- "Hallucinations" = plausible-sounding but wrong
- Always verify critical information
- These limitations are being actively worked on
- The Connections Test

# Hallucination: Confidently Incorrect

__Queries about specific numbers/statistics without clear sources:__

"What percentage of doctors in Ohio use AI tools daily?"

"How many medical students graduated from CWRU in 2023?"

__Queries combining real entities with fabricated details:__

"What did the 2024 AAMC report say about AI competency frameworks for year 2 medical students?"

"Which specific modules in Epic's EHR system support GPT-4 integration?"

__Requests for very specific technical details__

"What are the exact hyperparameters used in PubMedBERT's final training run?"

"List all 47 features in the latest version of Med-PaLM"

__Queries about niche intersections:__

"What Python libraries were specifically developed for analyzing USMLE Step 1 performance data?"

"Which medical schools have published AI ethics guidelines specifically for radiology education?"

---

- It’s getting harder to trigger these on purpose as models get better
- Have a real example ready
- This is why we need critical evaluation
- More reliable with proper prompting (Week 3-4)

# A Chatbot isn’t a One-and-done Q&A

Refine

Correct

Insist

Probe

*although the bot will happily make another error

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_7.png)

# Getting Started



* __Available at __  _[ai.case.edu](http://ai.case.edu)_
* ChatGPT 4o, 4.1, 5
  * With/Without Internet Search
* Claude Sonnet 4
  * With/Without Internet Search
* Meta Llama
  * Lightweight, open source LLM
* __Available at __  _[gemini.google.com](http://gemini.google.com)_
* Gemini
  * Writing tools
  * Image generation
  * Integration with Google Apps
  * Chat
  * Enterprise data protections apply  __if__  you log in as your @ _[case.edu](http://case.edu)_  self.
---

Talk about the privacy thing



# Using the Chat Interface

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_8.png)

![](img/AI%20For%20Everybody_%20Week%201%20-%20Introduction%20to%20GenAI_9.png)

# Your first Prompts

__Let’s Try__

1. "Explain quantum computing to a 10-year-old"

2. "Summarize the concept of homeostasis"

3. "Write a haiku about research"

__Let’s Notice__

- How quickly it responds

- The style and tone

- Level of detail

- Any limitations or errors

---

- Type these live
- Show real-time responses
- Discuss what worked, what didn't
- Different models may respond differently

# Hands-On

1. Connect to  _[ai.case.edu](http://ai.case.edu)_  and  _[gemini.google.com](http://gemini.google.com)_

2. Try 3-5 prompts related to YOUR work

3. Experiment with:

- Questions

- Writing requests

- Explanations

4. Try it on a few different models

5. Note what surprises you (good or bad)

20 minutes

We’ll reconvene and discuss

Questions? Use the chat if on zoom

# Discussion

What did you notice?

__- What worked well?__

__- What was surprising?__

__- Any frustrations or limitations?__

__- Ideas for how you might use this?__

---

- Capture common themes
- Address misconceptions
- Build on successes
- Validate frustrations
- Segue to next week's topics

# Week 1: Key Takeaways

__Remember__

- LLMs predict text, don't "know" facts

- They can hallucinate - always verify

- Different models have different strengths

- Experimentation is key to learning

- Start with simple, clear prompts

# Looking Ahead - Week 2

__Next Week__ :

- Deep dive into model differences

- When to use which model

- Comparative testing

- Understanding capabilities and limitations

__Your Task:__

- Experiment with the same task on ChatGPT, Claude, and/or Gemini

- Document differences

- Bring questions!

# Questions and Resources

__Helpful Resources__

_[OpenAI Help Center](https://help.openai.com/en/collections/3742473-chatgpt)_

_[Anthropic Documentation](https://support.claude.com/en/collections/4078531-claude)_

_[Google Gemini Help Center](http://support.google.com/gemini)_

_[Case AI Resources](https://case.edu/utech/help/knowledge-base/ai-artificial-intelligence)_

_[CWRU AI Playground](https://case0.sharepoint.com/sites/CWRUAIPlayground/SitePages/ITHelpdeskHome.aspx)_

__Contact__

Kate Weber

_[kate-weber@case.edu](mailto:kate-weber@case.edu)_

