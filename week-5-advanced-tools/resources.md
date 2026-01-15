# Week 5: Grounded AI & Knowledge Agents - Supplemental Resources
## NotebookLM, Custom GPTs & RAG Implementation Materials

---

## 🔗 Essential Links

### Primary Tools
- **NotebookLM:** [notebooklm.google.com](https://notebooklm.google.com) - Free access, Google account required
- **Custom GPTs:** [chat.openai.com](https://chat.openai.com) - ChatGPT Plus required ($20/month)
- **Claude Projects:** [claude.ai](https://claude.ai) - Pro tier for project knowledge ($20/month)

### Tool Documentation
- **NotebookLM Help Center:** [support.google.com/notebooklm](https://support.google.com/notebooklm)
- **OpenAI Custom GPT Guide:** [help.openai.com/en/articles/8554397-creating-a-gpt](https://help.openai.com/en/articles/8554397-creating-a-gpt)
- **Claude Projects Documentation:** [support.anthropic.com](https://support.anthropic.com) (search "Projects")

### RAG & Vector Databases (Advanced)
- **Pinecone Vector Database:** [www.pinecone.io](https://www.pinecone.io) - For technical implementations
- **LangChain Documentation:** [python.langchain.com](https://python.langchain.com) - For developers building RAG systems
- **Weaviate Open Source:** [weaviate.io](https://weaviate.io) - Self-hosted vector database option

---

## 📚 Sample Documents for Practice

### Clinical Guidelines (Download These for NotebookLM Practice)

**Freely Available:**
1. **AHA/ACC Heart Failure Guidelines** 
   - Source: [professional.heart.org/guidelines](https://professional.heart.org/guidelines)
   - Use case: Extract specific device therapy criteria

2. **ADA Standards of Medical Care in Diabetes**
   - Source: [diabetesjournals.org/care/issue/47/Supplement_1](https://diabetesjournals.org/care/issue/47/Supplement_1)
   - Use case: Compare screening recommendations across age groups

3. **IDSA Antimicrobial Stewardship Guidelines**
   - Source: [www.idsociety.org/practice-guideline/antimicrobial-stewardship](https://www.idsociety.org/practice-guideline/antimicrobial-stewardship)
   - Use case: Build antibiotic selection reference

4. **NCCN Guidelines** (Registration Required)
   - Source: [www.nccn.org/professionals/physician_gls](https://www.nccn.org/professionals/physician_gls)
   - Use case: Oncology treatment pathways

### Research Papers for NotebookLM Practice

**Suggested Workflow:**
1. Pick a topic relevant to your practice
2. Search PubMed for 5-10 recent papers
3. Download PDFs
4. Upload to NotebookLM
5. Practice the exercises below

**Example Topics:**
- GLP-1 agonists in cardiovascular disease
- AI in radiology interpretation
- Long COVID management strategies
- Newer anticoagulants in atrial fibrillation
- Immunotherapy in melanoma

---

## 🧪 NotebookLM Exercises

### Exercise 1: Conflict Detection
**Goal:** Find contradictions across guidelines

**Setup:**
1. Upload 2-3 different clinical guidelines for the same condition (e.g., AHA vs ESC heart failure guidelines)
2. Use this prompt:

```
Compare the recommendations across these guidelines. Create a table with 
three columns:
- Topic Area
- [Guideline 1] Recommendation (with page citation)
- [Guideline 2] Recommendation (with page citation)

Focus on areas where recommendations differ in:
- Medication dosages
- Diagnostic thresholds
- Timing of interventions
```

**Expected Outcome:**
- Table highlighting differences
- Citations to specific pages
- Ability to click and verify discrepancies

**Teaching Point:** Different guidelines may conflict - NotebookLM helps surface these systematically.

---

### Exercise 2: Audio Overview + Interruption
**Goal:** Learn to use AI podcast feature

**Setup:**
1. Upload 3-5 papers on one topic
2. Generate Audio Overview (button in NotebookLM)
3. Listen for 2-3 minutes
4. Use "Interrupt" feature to ask:
   - "What were the sample sizes across these studies?"
   - "Were there any pediatric populations studied?"
   - "Which paper had the strongest methodology?"

**Expected Outcome:**
- Understanding of how audio synthesis works
- Practice with interactive Q&A during playback
- Identification of gaps in literature

**Teaching Point:** Audio overviews good for initial synthesis, interactive Q&A for deep dives.

---

### Exercise 3: Study Design Comparison
**Goal:** Systematic methodology review

**Setup:**
1. Upload 5-7 papers on same clinical question
2. Use this prompt:

```
Create a comprehensive comparison table with these columns:
- First Author & Year
- Study Design (RCT, observational, meta-analysis, etc.)
- Sample Size
- Primary Outcome Measure
- Key Finding (1 sentence)
- Major Limitation (1 sentence)
- Citation (page number of methods section)

Sort by study quality (RCTs first, then cohort, then case series).
```

**Expected Outcome:**
- Structured literature review table
- Quick assessment of evidence quality
- Identification of research gaps

**Use Case:** Grant proposals, systematic reviews, teaching materials

---

### Exercise 4: Citation Verification Workflow
**Goal:** Build trust in AI-generated summaries

**Setup:**
1. Upload a complex clinical guideline (>100 pages)
2. Ask for summary of specific section
3. For every claim in summary, click the citation number
4. Verify the AI correctly interpreted the source

**Prompt:**
```
Summarize the diagnostic criteria for [CONDITION] from this guideline. 
For each criterion, provide the specific page number and section heading.
```

**Check:**
- Does each citation link to the correct page?
- Did AI accurately represent the guideline text?
- Are there any inferences not directly stated?

**Teaching Point:** Even grounded AI needs verification - but citations make this efficient.

---

## 🤖 Custom GPT Exercises

### Exercise 1: Building Your First GPT
**Goal:** Create a simple, reusable workflow assistant

**Scenario:** Grant abstract formatter

**Instructions to Put in Custom GPT:**
```
You are the NIH Grant Abstract Specialist. Your job is to help format 
research abstracts for NIH grant submissions.

**Your Role:**
- Format abstracts to NIH specifications
- Ensure all required sections are present
- Keep within character limits
- Use precise, formal academic language

**Required Sections (in order):**
1. Specific Aims (What question?)
2. Background & Significance (Why important?)
3. Innovation (What's new?)
4. Approach (How will you do it?)
5. Impact (Why does it matter?)

**Constraints:**
- Specific Aims: Maximum 500 characters
- Full abstract: Maximum 2,000 characters
- Use active voice
- No jargon without definition
- Emphasize clinical relevance

**When user provides draft:**
1. Identify which sections are present
2. Note missing sections
3. Check character counts
4. Provide formatted version
5. Suggest improvements for clarity/impact

**Do NOT:**
- Change the scientific content or claims
- Add citations (user provides these)
- Make claims beyond the user's data
```

**Knowledge Files to Upload:**
- NIH abstract formatting guide (download from grants.nih.gov)
- 2-3 successful grant abstracts from your field (de-identified)

**Test Prompts:**
```
[Paste a rough draft abstract]
Format this for NIH submission and identify any missing sections.
```

---

### Exercise 2: Clinical Protocol Assistant
**Goal:** Build a reference tool for your specific protocols

**Setup:**
1. Collect your department's SOPs, protocols, or clinical pathways
2. De-identify if needed
3. Upload to Custom GPT as knowledge files

**Instructions:**
```
You are the [Department Name] Clinical Protocol Assistant. You help staff 
quickly find and apply our department's specific protocols and SOPs.

**Your Knowledge Base:**
- Department SOPs (uploaded files)
- Clinical pathways
- Order sets

**Your Role:**
1. Answer questions about department-specific protocols
2. Cite the specific protocol name and section
3. Highlight any recent updates (if noted in documents)
4. Never improvise - only reference uploaded documents

**Response Format:**
- Protocol Name: [Name]
- Section: [Section number/title]
- Recommendation: [Quote or close paraphrase]
- Last Updated: [Date from document]
- Note: [Any special circumstances]

**If Information Not in Protocols:**
"I don't see this specific scenario covered in our uploaded protocols. 
I recommend consulting [appropriate person/committee] or checking 
[relevant external guideline]."

**Do NOT:**
- Make up protocols not in your knowledge base
- Provide general medical advice
- Override clinical judgment
```

**Test Scenarios:**
- "What's our protocol for pediatric sedation?"
- "How do we handle contrast allergies?"
- "What are the steps for code blue in the OR?"

---

### Exercise 3: Patient Education Generator
**Goal:** Consistent, health-literacy-appropriate materials

**Instructions:**
```
You are a Patient Education Specialist creating materials at 6th-8th grade 
reading level for [Specialty] patients.

**Style Guide:**
- Use short sentences (max 15 words)
- One idea per sentence
- Active voice preferred
- Define medical terms immediately
- Use analogies from everyday life
- Friendly but professional tone

**Required Sections:**
1. What is [Condition/Procedure]? (50-75 words)
2. Why does this matter? (50-75 words)
3. What will happen? (100-150 words)
4. What should I expect? (75-100 words)
5. When should I call the doctor? (50-75 words)
6. Questions to ask my doctor (5 questions)

**Safety Rules:**
- No specific medical advice
- Include "Ask your doctor" for personalization
- Avoid alarming language while being truthful
- Include when to seek emergency care
- Note that materials are educational, not prescriptive

**After Drafting:**
Check reading level at https://readable.com (aim for 6th-8th grade).
```

**Knowledge Files:**
- Your institution's patient education style guide
- 3-5 examples of excellent patient materials from your specialty

**Test:**
```
Create a patient education handout explaining: [Your topic]
Patient context: [Age, background, specific concerns if any]
```

---

## 📊 NotebookLM vs Custom GPT Decision Matrix

| Scenario | Best Tool | Why |
|----------|-----------|-----|
| **Analyzing 10+ research papers** | NotebookLM | Better source management, citations, audio overviews |
| **Recurring formatting task** | Custom GPT | Persistent instructions, no re-uploading |
| **Finding contradictions in guidelines** | NotebookLM | Superior multi-document comparison |
| **Department-specific Q&A** | Custom GPT | Can be shared with team, consistent answers |
| **Literature review for grant** | NotebookLM | Source tracking, export citations |
| **Patient education materials** | Custom GPT | Style consistency, reusable templates |
| **Complex multi-step workflow** | Custom GPT | Can encode detailed processes |
| **One-time deep document analysis** | NotebookLM | No setup needed, free |
| **Teaching clinical reasoning** | Custom GPT | Can encode pedagogical approach |
| **Comparing treatment protocols** | NotebookLM | Better at finding specific differences |

---

## 🔬 Understanding RAG (Retrieval-Augmented Generation)

### What Happens Behind the Scenes

**Traditional AI (No RAG):**
```
User: "What does our protocol say about X?"
↓
AI: Generates answer from training data (may hallucinate)
```

**RAG-Based AI (NotebookLM/Custom GPTs):**
```
User: "What does our protocol say about X?"
↓
Step 1: Search your uploaded documents for relevant chunks
Step 2: Retrieve the most relevant passages
Step 3: Provide those passages as context to AI
Step 4: AI generates answer USING those passages
↓
AI: Cites specific sections from your documents
```

**Key Benefit:** AI can only "see" what you uploaded, dramatically reducing hallucinations.

**Limitation:** AI can't answer questions outside your uploaded content (which is a good thing for accuracy).

---

### When RAG Fails (And What to Do)

**Problem 1: Document Too Long**
- NotebookLM limit: 500k words per source
- Solution: Break into logical sections (by chapter, topic, etc.)

**Problem 2: Poor Source Quality**
- Scanned PDFs with bad OCR
- Solution: Re-scan or use text extraction tools first

**Problem 3: Context Span**
- Answer requires connecting information across many documents
- Solution: Ask AI to create synthesis document first, then ask questions

**Problem 4: Outdated Information**
- AI uses old version of guideline
- Solution: Check document dates, remove old versions

---

## 💡 Advanced Techniques

### Multi-Notebook Strategy (NotebookLM)

Create separate notebooks for different purposes:

**Notebook 1: Current Clinical Guidelines**
- Upload latest versions only
- Review quarterly for updates
- Use for evidence-based decision support

**Notebook 2: Research Literature by Topic**
- Organize by clinical question
- Include meta-analyses and systematic reviews
- Use for grant writing and teaching

**Notebook 3: Department Protocols**
- SOPs, order sets, clinical pathways
- Team reference
- Update as protocols change

**Notebook 4: Patient Education Sources**
- Trusted patient-facing materials
- Health literacy best practices
- Use to ensure consistent messaging

---

### Prompt Chaining with Custom GPTs

**Technique:** Use output from one prompt as input to next

**Example Workflow:**
```
Prompt 1: "Extract the 5 most important clinical pearls from these papers."
[Copy output]

Prompt 2: "Convert these clinical pearls into 5 multiple-choice questions 
for medical students, with detailed explanations."
[Copy output]

Prompt 3: "Create a 1-page study guide summarizing the pearls and including 
the practice questions."
```

**Use Case:** Creating teaching materials, case conferences, board review

---

### Version Control for Knowledge Bases

**Best Practice:** Track what's in your GPT knowledge base

**Maintain a log:**
```
Custom GPT: "Grant Abstract Formatter"
Knowledge Base Contents:
- NIH_abstract_guidelines_2026.pdf (Updated Jan 2026)
- Sample_abstract_cardiology_2025.pdf
- Sample_abstract_oncology_2024.pdf
- Department_writing_style_guide.pdf (v3.2)

Last Updated: January 15, 2026
Next Review: April 15, 2026
```

**Why This Matters:**
- Know when guidelines are outdated
- Understand what GPT can/can't reference
- Share configuration with colleagues
- Troubleshoot unexpected responses

---

## 🎯 Weekly Practice Plan

### Days 1-2: NotebookLM Mastery
- Create first notebook with 5 papers from your field
- Practice all 4 exercises above
- Generate audio overview
- Verify at least 10 citations

### Days 3-4: Custom GPT Building
- Build first Custom GPT for a recurring task
- Test with 5 different inputs
- Refine instructions based on outputs
- Share with one colleague for feedback

### Day 5: Comparison Testing
- Take same task
- Do it in NotebookLM
- Do it with Custom GPT
- Which was better? Why?
- Document decision criteria

### Days 6-7: Integration with Weeks 1-4
- Take Week 3 best prompt
- Add Week 4 verification
- Implement with Week 5 grounding (NotebookLM or Custom GPT)
- Document the complete workflow

---

## ⚠️ Common Mistakes & Solutions

### Mistake 1: Uploading Too Many Unrelated Documents
**Problem:** NotebookLM gets confused when documents span unrelated topics.

**Solution:** Keep notebooks focused. One notebook per project or clinical question.

---

### Mistake 2: Not Verifying Citations
**Problem:** Trusting that citation links are accurate.

**Solution:** Spot-check 25% of citations, especially for high-stakes decisions.

---

### Mistake 3: Over-Complicated Custom GPT Instructions
**Problem:** 2000-word instructions that contradict themselves.

**Solution:** Start simple. Add complexity only when needed. Test after each addition.

---

### Mistake 4: No Update Schedule
**Problem:** Knowledge base becomes outdated, GPT gives old guidance.

**Solution:** Calendar reminder every 3-6 months to review and update sources.

---

### Mistake 5: Sharing GPTs with PHI
**Problem:** Creating Custom GPT with patient data, then sharing link.

**Solution:** Never upload PHI to Custom GPT knowledge files. Use de-identified examples only.

---

## 📚 Recommended Advanced Reading

### Technical Deep Dives
- **"Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"** (Lewis et al.) - Original RAG paper
- **LangChain Documentation** - If you want to build your own RAG system
- **Pinecone Vector Database Guide** - Understanding how semantic search works

### Clinical Applications
- **"Grounded AI in Clinical Decision Support"** - Search Google Scholar for 2025-2026 publications
- **"Custom Large Language Models for Healthcare"** - Emerging literature on domain-specific LLMs

### Best Practices
- **OpenAI GPT Best Practices Guide** - Continually updated
- **Anthropic's Constitutional AI Papers** - How Claude is trained for safety

---

## ✅ Week 5 Checklist

Before Week 6, you should have:
- [ ] Created NotebookLM account and first notebook
- [ ] Uploaded at least 5 documents and practiced querying
- [ ] Generated and listened to at least one Audio Overview
- [ ] Verified citations for accuracy (spot-check 10+)
- [ ] Built at least one Custom GPT (or planned one if no Plus account)
- [ ] Tested your Custom GPT with 5 different inputs
- [ ] Compared NotebookLM vs Custom GPT for one task
- [ ] Documented which tool works better for which scenarios
- [ ] Integrated grounding techniques with Week 3 prompts and Week 4 verification

---

## 🆘 Help & Support

**NotebookLM:**
- Help Center: [support.google.com/notebooklm](https://support.google.com/notebooklm)
- Known Issues: Check Google Workspace updates
- Community: Reddit r/NotebookLM

**Custom GPTs:**
- OpenAI Help: [help.openai.com](https://help.openai.com)
- Community: OpenAI Community Forums
- Examples: ChatGPT GPT Store (browse others' GPTs for inspiration)

**General RAG Questions:**
- LangChain Discord Community
- Pinecone Documentation & Community

**Institutional Support:**
- Check if your institution has enterprise agreements (may unlock additional features)

---

## 🔗 Quick Reference Links

### Free Tools
- NotebookLM: [notebooklm.google.com](https://notebooklm.google.com)
- Claude (Free tier): [claude.ai](https://claude.ai)
- ChatGPT (Free tier): [chat.openai.com](https://chat.openai.com)

### Paid Tools ($20/month tier)
- ChatGPT Plus (for Custom GPTs): [chat.openai.com/plus](https://chat.openai.com)
- Claude Pro (for Projects): [claude.ai/upgrade](https://claude.ai)

### Clinical Guidelines
- ACC Guidelines: [professional.heart.org/guidelines](https://professional.heart.org/guidelines)
- ADA Standards: [diabetesjournals.org/care](https://diabetesjournals.org/care)
- NCCN (Registration): [www.nccn.org](https://www.nccn.org)

### Literature Search
- PubMed: [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov)
- Google Scholar: [scholar.google.com](https://scholar.google.com)
- Cochrane Library: [www.cochranelibrary.com](https://www.cochranelibrary.com)

---

*These resources supplement Week 5 instructor notes and student handout. Grounding techniques learned this week are critical for Week 6's orchestration workflows.*
