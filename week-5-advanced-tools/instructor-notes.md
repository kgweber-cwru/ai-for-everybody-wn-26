# Week 5: Knowledge Agents & Grounded AI
## Instructor Notes (Convert to Slides) - 2026 Updated

---

### Slide 1: Title & Welcome Back
**Title:** Knowledge Agents & Grounded AI  
**Subtitle:** Week 5 - Building Your Personal Brain

**Quick Check-In:**
- Review Week 4 homework: Did the Logic Audit catch anything surprising?
- Did anyone find a logical hallucination using red-team auditing?
- What verification techniques are you using now?

**Speaker Notes:**
- Acknowledge that Week 4 was intense - verification is hard work
- Today we make AI EASIER to verify by grounding it
- Moving from "trust but verify" to "verify by design"

---

### Slide 2: Today's Goals
**What We'll Cover:**
- Understanding "grounded" AI and RAG (Retrieval-Augmented Generation)
- NotebookLM for document-grounded responses
- Custom GPTs with system instructions
- Building knowledge agents that don't hallucinate outside your sources
- Hands-on: Create your own grounded knowledge base

**Speaker Notes:**
- This is where Weeks 3-4 pay off
- Prompting skills (Week 3) become system instructions
- Verification skills (Week 4) become less necessary with grounding
- We're building specialized tools, not just using general ones

---

### Slide 3: The Hallucination Problem (Recap)
**What We've Learned:**
- Week 1: LLMs can hallucinate
- Week 4: Logical hallucinations are the real danger
- Week 4: Verification (CoVe, red-team) catches errors

**The Question:**
*Can we prevent hallucinations instead of just catching them?*

**The Answer:**
Yes! By **grounding** AI in your specific sources

**Speaker Notes:**
- Verification is necessary but labor-intensive
- Grounding reduces the need for verification
- It's not perfect, but it's a huge improvement
- This is the future of professional AI use

---

### Slide 4: What is "Grounded" AI?
**Definition:** AI that is restricted to use ONLY your provided sources

**How It Works:**
1. You upload specific documents
2. AI searches those documents for relevant info
3. AI answers based ONLY on what it finds
4. AI cites exactly where information came from

**Technical Term:** RAG (Retrieval-Augmented Generation)
- **Retrieval:** Finding relevant parts of your documents
- **Augmented:** Adding that info to the prompt
- **Generation:** Creating answer based on retrieved info

**Why Grounding Matters in Medicine:**
- Follows YOUR department's SOPs
- Uses YOUR institution's guidelines
- References YOUR specific research
- Not random internet information from 2021

**Speaker Notes:**
- This is the biggest shift in practical AI use
- General-purpose = convenient but risky
- Grounded = slightly less convenient but much safer
- Show diagram if possible: User Query → Document Search → Grounded Response

---

### Slide 5: Grounded AI vs. General AI
**Comparison:**

| Aspect | General AI (ChatGPT) | Grounded AI (NotebookLM) |
|--------|----------------------|--------------------------|
| **Knowledge Source** | Entire internet (training data) | Only your uploaded documents |
| **Hallucination Risk** | High for specifics | Low (can only cite what's there) |
| **Citations** | Unreliable or fake | Direct links to source |
| **Customization** | Generic knowledge | Your specific domain |
| **Best For** | Brainstorming, drafting | Analysis, verification, synthesis |

**Speaker Notes:**
- Both have their place
- Week 1-4 taught general AI use
- Week 5-6 teach specialized AI use
- Professional workflows use both strategically

---

### Slide 6: Tool #1 - NotebookLM
**What is NotebookLM?**
- Google's research-first AI tool
- Upload up to 50 sources per notebook
- Each source can be 500K+ words
- 2-million-token context window

**Key Features (2026):**
1. **Source-Grounded Responses:** Every answer includes citations
2. **Interactive Audio Overviews:** AI generates podcast-style discussions
3. **Automatic Citation Linking:** Click citation → see exact paragraph
4. **Multi-Source Synthesis:** Finds connections across your documents
5. **Query Suggestions:** AI suggests questions based on your sources

**Access:** notebooklm.google.com (free!)

**Speaker Notes:**
- This is Google's answer to "how do we prevent hallucinations"
- Built specifically for research and document analysis
- Integrates with Gemini 3 Pro (reasoning model)
- Show the interface live if possible

---

### Slide 7: NotebookLM Demo - Setup
**Instructor Live Demo:**

**Step 1: Create New Notebook**
- Show creating a notebook with a specific purpose
- Example: "Clinical Guideline Comparison - Heart Failure"

**Step 2: Upload Sources**
- Upload 3-5 clinical guidelines or research papers
- Show supported formats: PDF, Google Docs, websites, YouTube videos
- Note the source limits and file sizes

**Step 3: Wait for Processing**
- AI analyzes and indexes your documents
- Usually takes 1-3 minutes depending on size
- Show the progress indicator

**Speaker Notes:**
- Have these documents prepared beforehand
- Use real clinical materials if possible
- Good examples: Conflicting guidelines, protocol updates
- Point out that video/YouTube transcripts are now sources

---

### Slide 8: NotebookLM Demo - Querying
**Instructor Live Demo (Continued):**

**Example Query 1: Basic Synthesis**
```
What do these guidelines say about ACE inhibitor dosing in elderly patients?
```
- Show how NotebookLM searches across all sources
- Point out the citation numbers
- Click a citation to show the exact source location

**Example Query 2: Finding Conflicts**
```
Where do these guidelines disagree on treatment approaches?
```
- Demonstrate NotebookLM comparing sources
- Show how it identifies conflicts
- Note: This would be tedious to do manually!

**Example Query 3: Specific Data**
```
List all mentioned contraindications for beta blockers across these documents.
```
- Show comprehensive aggregation
- Each item should have citations
- Verify one citation by clicking through

**Speaker Notes:**
- The citations are the killer feature
- Every claim is traceable
- If no citation → treat as hallucination
- Demo clicking through to verify accuracy

---

### Slide 9: NotebookLM - Audio Overview Feature
**What is an Audio Overview?**
- AI generates a podcast-style discussion of your sources
- Two AI "hosts" discuss key points
- 5-15 minutes depending on content
- Can be downloaded as MP3

**When to Use:**
- Quick overview of new literature
- Preparing for meetings
- Learning new topics
- Alternative to reading summaries

**2026 Update: Interactive Audio**
- Can now interrupt and ask questions
- AI hosts respond in real-time
- Like having a conversation about your research

**Demo (if time):**
- Generate audio overview
- Play 30-60 seconds
- Note the conversational tone
- Emphasize: This is from YOUR sources only

**Speaker Notes:**
- Students often love or hate this feature
- Great for auditory learners
- Helpful for commute/exercise learning
- But it's optional - text summaries work too

---

### Slide 10: NotebookLM - Best Practices
**DO:**
- ✓ Upload high-quality, authoritative sources
- ✓ Give your notebook a clear purpose/title
- ✓ Click citations to verify accuracy
- ✓ Use specific queries (apply Week 3 prompting skills!)
- ✓ Keep notebooks focused (one topic per notebook)

**DON'T:**
- ✗ Trust uncited statements
- ✗ Upload random internet articles without vetting
- ✗ Mix completely unrelated topics in one notebook
- ✗ Exceed source limits (quality > quantity)
- ✗ Forget that AI can still make logical errors

**Speaker Notes:**
- "Garbage in, garbage out" still applies
- Grounding doesn't replace critical thinking
- Week 4's verification skills still matter
- But workload is greatly reduced

---

### Slide 11: Tool #2 - Custom GPTs
**What is a Custom GPT?**
- Specialized version of ChatGPT
- Pre-loaded with instructions and knowledge
- Reusable for specific tasks
- Shareable with colleagues

**Why Create Custom GPTs?**
- Consistency across repeated tasks
- No need to re-type instructions every time
- Can include your organization's specific guidelines
- Can be shared with team for standardization

**Requirements:**
- ChatGPT Plus subscription ($20/month)
- OR institutional access (check if your org has it)

**Speaker Notes:**
- This is where Week 3's Five Pillars become permanent
- Instead of crafting perfect prompt each time, build it once
- Great for workflows that repeat weekly/daily
- Show real examples if you have them

---

### Slide 12: Custom GPT Architecture
**Components of a Custom GPT:**

**1. Name & Description**
- What is this GPT for?
- Who is it for?

**2. Instructions (System Prompt)**
- This is your Week 3 Five Pillars!
- ROLE, CONTEXT, TASK, CONSTRAINTS, THOUGHT PROCESS
- Permanent instructions the GPT always follows

**3. Knowledge Base**
- Upload files the GPT can reference
- Your SOPs, templates, guidelines
- Same concept as NotebookLM but integrated into ChatGPT

**4. Capabilities**
- Web browsing: Can it search current information?
- DALL-E: Can it generate images?
- Code Interpreter: Can it run Python?

**5. Actions (Advanced)**
- Connect to external APIs
- Schedule emails, update calendars, etc.

**Speaker Notes:**
- #2 (Instructions) is what most people use
- #3 (Knowledge) turns it into grounded AI
- #4 and #5 are advanced - optional
- We'll focus on #2 and #3 today

---

### Slide 13: Custom GPT Demo - Creation
**Instructor Live Demo:**

**Example: "Grant Proposal Reviewer"**

**Step 1: Name & Description**
- Name: "NIH Grant Proposal Reviewer"
- Description: "Reviews R01 proposals for common issues before submission"

**Step 2: Write Instructions**
```
You are a Senior NIH Grant Reviewer with 15 years of experience.

Your role is to review R01 proposals and provide critical feedback.

For each proposal section:
1. Check adherence to NIH guidelines
2. Identify common rejection reasons
3. Suggest specific improvements
4. Note any missing elements

Constraints:
- Be direct but constructive
- Focus on high-impact issues first
- Cite specific NIH guidelines when applicable
- Maximum 300 words per section review

Thought Process:
Before reviewing, identify the specific aim. Then evaluate  
each section against NIH scoring criteria. Prioritize issues  
that would affect fundability.
```

**Step 3: Add Knowledge (Optional)**
- Upload NIH guidelines
- Upload successful grant examples
- Upload institution's requirements

**Step 4: Test**
- Try a sample query
- Refine instructions based on output

**Speaker Notes:**
- This demo should feel familiar - it's Week 3's Five Pillars!
- The instructions persist across all conversations
- Knowledge base makes it grounded like NotebookLM
- Once built, anyone can use it consistently

---

### Slide 14: Custom GPT vs. NotebookLM
**When to Use Each:**

**NotebookLM:**
- ✓ Exploring new literature
- ✓ Finding conflicts/agreements across sources
- ✓ One-time deep dives
- ✓ Research synthesis
- ✓ Generating audio overviews

**Custom GPT:**
- ✓ Recurring workflows
- ✓ Standardized processes
- ✓ Team collaboration (shareable)
- ✓ Integration with other tools
- ✓ Combining grounding with general knowledge

**Can Use Both:**
- Research in NotebookLM → Draft in Custom GPT
- Literature review in NotebookLM → Write-up in Custom GPT
- They complement each other!

**Speaker Notes:**
- These aren't competing tools
- Professional workflows use both
- Week 6 will show orchestration between tools
- Choose based on task and frequency

---

### Slide 15: Hands-On Exercise (25 min)
**Activity: Build Your First Grounded Knowledge Base**

**Option A: NotebookLM (Recommended for Beginners)**
1. Go to notebooklm.google.com
2. Create a new notebook for your domain
3. Upload 3-5 relevant documents (papers, guidelines, SOPs)
4. Try the "Guideline Reconciliation" task:
   - Query: "Where do these documents provide different advice?"
   - Check citations
   - Verify one citation by clicking through

**Option B: Custom GPT (If you have ChatGPT Plus)**
1. Go to ChatGPT → "Explore GPTs" → "Create"
2. Design a GPT for a recurring task in your work
3. Write system instructions using Five Pillars
4. Upload 1-2 knowledge files
5. Test with a sample query

**Group Discussion After:**
- What worked well?
- What surprised you?
- Where could you use this in your work?

**Speaker Notes:**
- Circulate and help with technical issues
- NotebookLM is easier for first-timers
- Custom GPTs require more upfront thought
- Both are valuable skills
- Capture use cases participants discover

---

### Slide 16: Real-World Use Cases
**Medical/Clinical:**
- **Protocol Assistant:** Upload all department protocols → instant reference
- **Literature Reviewer:** Upload papers on specific topic → synthesis
- **Guidelines Comparator:** Upload multiple guidelines → find differences
- **Case Study Analyzer:** Upload teaching cases → generate discussion questions

**Research:**
- **Methods Consultant:** Upload methodology papers → answer methods questions
- **Grant Reviewer:** Upload successful grants + guidelines → review drafts
- **Data Interpretation:** Upload analysis results → help explain findings

**Administrative:**
- **Policy Navigator:** Upload institutional policies → quick answers
- **Meeting Prep:** Upload agendas + background docs → briefing summaries
- **Communication Drafter:** Upload templates + style guides → consistent messaging

**Speaker Notes:**
- Ask: What use cases do participants envision?
- Real adoption comes from solving real problems
- Start small: One recurring task
- Expand as you gain confidence

---

### Slide 17: Limitations & Cautions
**What Grounded AI Can't Do:**
- ✗ Access information outside your documents
- ✗ Guarantee perfect accuracy (verification still needed)
- ✗ Update automatically when sources change
- ✗ Replace human expertise and judgment
- ✗ Handle highly ambiguous or contradictory sources perfectly

**Best Practices:**
- Still verify critical outputs (Week 4 skills!)
- Update knowledge bases regularly
- Don't over-trust just because it's grounded
- Use for assistance, not autonomous decision-making
- Combine with human review for high-stakes work

**Speaker Notes:**
- Grounding reduces hallucinations, doesn't eliminate them
- Logical errors still possible (Week 4)
- Quality of sources matters enormously
- This is augmentation, not replacement

---

### Slide 18: Privacy & Institutional Considerations
**NotebookLM:**
- Google's standard privacy policies apply
- Check if approved by your institution
- Don't upload PHI without de-identification
- Data may be used to improve Google services

**Custom GPTs:**
- OpenAI's privacy policies apply
- ChatGPT Plus: Conversations not used for training (by default)
- Enterprise: Can have stricter controls
- Check institutional agreements

**Best Practice:**
- Use institutional AI instances when available
- De-identify sensitive data
- Follow your organization's AI policies
- When in doubt, ask IT/compliance

**Speaker Notes:**
- Privacy is non-negotiable (Week 4 reminder)
- Institutional tools often have better protections
- Check if your org has enterprise agreements
- Never compromise patient privacy for convenience

---

### Slide 19: Key Takeaways
**Major Concepts:**
- **Grounded AI** limits responses to your specific sources
- **RAG** (Retrieval-Augmented Generation) is the technical approach
- **NotebookLM**: Google's tool for document-grounded research
- **Custom GPTs**: ChatGPT specialized with your instructions and knowledge

**Why Grounding Matters:**
- Reduces hallucinations dramatically
- Provides verifiable citations
- Customizes AI to your specific domain
- Makes verification easier (Week 4 → Week 5 connection)

**Skills Applied:**
- Week 3 prompting → Custom GPT instructions
- Week 4 verification → Now easier with citations
- Week 1-2 model knowledge → Choosing right tool

**Speaker Notes:**
- This is a milestone week
- Moving from general tools to specialized agents
- Week 6 will tie everything together
- The professional AI workflow is taking shape

---

### Slide 20: Looking Ahead - Week 6
**Next Week: Orchestration & Building Your AI Workflow**
- Scite.ai for research verification
- Multi-tool workflows (orchestration)
- Combining: Verification (Scite) → Synthesis (NotebookLM) → Drafting (Custom GPT)
- Building your complete, verifiable AI pipeline
- Series wrap-up and implementation planning

**Connection:**
- Week 1-2: Choose tools
- Week 3: Prompt effectively
- Week 4: Verify rigorously
- Week 5: Ground in your sources ← Today
- Week 6: Orchestrate everything into workflows

**Assignment for Next Week:**
**Build a "Clinical Protocol Agent"**

**Option A (NotebookLM):**
1. Create a notebook with your 5 most-referenced resources
2. Generate an Audio Overview
3. Listen and note one "connection" the AI made that you hadn't considered
4. Write 2-3 paragraphs about its usefulness

**Option B (Custom GPT):**
1. Design a GPT for a specific recurring task
2. Write system instructions using the Five Pillars
3. Test with 3 different queries
4. Refine instructions based on outputs
5. Write 2-3 paragraphs about how this could save time

**Both Options:**
- Document what worked and what didn't
- Bring examples to share in Week 6

**Speaker Notes:**
- This assignment builds a real tool they'll use
- Next week they'll integrate it into larger workflows
- Encourage ambition but start simple
- Remind: Iteration is expected

---

### Slide 21: Questions & Discussion
**Open Floor:**
- What excites you about grounded AI?
- What concerns do you have?
- What will you build first?
- How does this change your AI usage?

**Encourage Sharing:**
- Use case ideas
- Collaboration opportunities
- Technical questions
- Implementation planning

---

## Teaching Tips

### Time Management (50 min)
- Slides 1-5: Welcome & Grounding Concepts (8 min)
- Slides 6-10: NotebookLM Demo & Best Practices (12 min)
- Slides 11-14: Custom GPTs & Comparison (8 min)
- Slide 15: Hands-On Exercise (20 min)
- Slides 16-21: Use Cases, Wrap-up, Q&A (2 min)

### Critical Preparations
**Must Have Ready:**
1. **NotebookLM Demo:**
   - Pre-loaded notebook with 3-5 clinical papers
   - Know your example queries
   - Have audio overview pre-generated (in case of lag)

2. **Custom GPT Demo:**
   - Have example GPT already created
   - Or be ready to create one live (riskier)
   - Test beforehand

3. **Backup Plan:**
   - Screenshots of both tools in action
   - Pre-recorded demos if live fails
   - Written examples if can't show live

### Common Questions

**Q: "Can I use NotebookLM with patient data?"**
A: Not unless you have institutional approval and proper de-identification. When in doubt, use synthetic/example data or published cases.

**Q: "Do Custom GPTs cost extra?"**
A: Yes, requires ChatGPT Plus ($20/month) OR your institution may have enterprise access. Check with IT.

**Q: "Can I share my Custom GPT?"**
A: Yes! You can share a link. Recipients need ChatGPT Plus to use it. Great for team standardization.

**Q: "Is NotebookLM really free?"**
A: Yes (as of 2026). Google offers it free, likely using data to improve Gemini. Check current terms.

**Q: "Which is better, NotebookLM or Custom GPT?"**
A: Different purposes! NotebookLM for research/exploration, Custom GPT for recurring workflows. Use both.

**Q: "How many sources can I upload?"**
A: NotebookLM: 50 sources. Custom GPT: Varies, but typically 10-20 files depending on size.

### Adaptation Notes

**If Short on Time:**
- Focus on NotebookLM only (more accessible)
- Assign Custom GPT as optional homework
- Skip audio overview demo

**If Students Struggle:**
- Do hands-on as guided group activity
- Share screen and walk through together
- Provide step-by-step written guide
- Schedule office hours for 1-on-1 help

**If Students Are Advanced:**
- Show Custom GPT "Actions" (API integrations)
- Discuss fine-tuning vs. RAG
- Preview vector databases and embeddings
- Introduce multi-agent systems concept

### Backup Activities

**If Technology Fails:**
- Group discussion: "Design your ideal knowledge agent"
- Paper exercise: Write Custom GPT instructions
- Case study analysis: When would grounding help vs. hurt?
- Video demo (pre-recorded backup)

**If Students Finish Early:**
- Explore NotebookLM's "query suggestions" feature
- Try uploading a YouTube video as a source
- Experiment with audio overview customization
- Share and critique each other's Custom GPT instructions

---

*Week 5 Complete - Ready for Week 6: Orchestration & Final Workflow Integration*
