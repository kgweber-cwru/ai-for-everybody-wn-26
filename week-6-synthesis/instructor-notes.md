# Week 6: Building Your 2026 AI Workflow
## Instructor Notes (Convert to Slides)

---

### Slide 1: Title & Celebration
**Title:** Building Your 2026 AI Workflow  
**Subtitle:** Week 6 - From Tools to Systems

**Welcome Back:**
- "Congratulations! You've made it to the final week."
- "You now have skills that 95% of healthcare professionals don't have yet"
- Quick reflection: What's changed in how you think about AI since Week 1?

**Speaker Notes:**
- This is a celebration as much as a learning session
- Acknowledge the journey from skepticism to confidence
- Set tone: Today is about integration, not new complexity
- Emphasize: They've already learned the hard parts

---

### Slide 2: Today's Goals
**What We'll Cover:**
- Orchestration: Building multi-tool workflows
- Scite.ai: The verification engine for 2026
- Clinical agents: The future already happening
- Live demo: Full pipeline in action
- Series synthesis: Your complete toolkit
- Final assignment: Personal workflow map

**Speaker Notes:**
- Today ties together everything from Weeks 1-5
- Less new content, more integration
- By end of session, they'll have a complete workflow system
- This is the transition from learning to implementation

---

### Slide 3: The Journey So Far
**Quick Recap:**

**Week 1-2: The Foundation**
- Model selection (GPT-5 vs GPT-4o vs Claude vs Gemini)
- Reasoning vs prediction tradeoffs
- Context windows and use cases

**Week 3: The Craft**
- Five Pillars of prompting
- Engineering vs chatting
- Your prompt libraries

**Week 4: The Safety Net**
- Chain-of-Verification (CoVe)
- Red-team auditing
- Understanding hallucinations

**Week 5: The Grounding**
- NotebookLM for your documents
- Custom GPTs for your workflows
- RAG (Retrieval-Augmented Generation)

**Today: The System**
- How do we combine all of this?

**Speaker Notes:**
- This should be quick (2-3 minutes)
- Each week built on the previous
- Now we orchestrate the complete toolkit
- Ask: "What's been most valuable so far?"

---

### Slide 4: What is Orchestration?
**Definition:** The systematic chaining of multiple AI tools to create a reliable, verifiable workflow

**Why Not Just Use One Tool?**
- **Single-point-of-failure:** One hallucination ruins everything
- **Lack of specialization:** General tools aren't optimized for verification
- **No audit trail:** Can't trace where information came from

**The Orchestration Principle:**
- Different tools for different stages
- Each tool's output becomes next tool's input
- Built-in verification at each handoff
- Human oversight at critical junctions

**The 2026 Difference:**
- 2024: "Ask ChatGPT"
- 2026: "Build a pipeline with verification stages"

**Speaker Notes:**
- This is the most important conceptual shift
- Professional AI use = multi-tool orchestration
- Medical analogy: Like using different specialists for different diagnoses
- Emphasize: This is the NEW skill for 2026

---

### Slide 5: The Three-Stage Pipeline
**Standard Workflow Architecture:**

**Stage 1: VERIFICATION (Evidence Finding)**
- Tools: Scite.ai, Consensus, PubMed
- Purpose: Find cited, peer-reviewed evidence
- Output: List of verified sources with citation context

**Stage 2: SYNTHESIS (Organization)**
- Tools: NotebookLM, Claude (long context)
- Purpose: Extract and organize information from YOUR documents
- Output: Structured summaries grounded in your sources

**Stage 3: DRAFTING (Production)**
- Tools: Custom GPTs, Claude, GPT-5
- Purpose: Create final deliverable with specific formatting
- Output: Polished document ready for human review

**The Critical Addition: RED-TEAM AUDIT**
- After Stage 3, before delivery
- Apply Week 4's audit techniques
- Human verification of key claims

**Speaker Notes:**
- This is the template for professional AI workflows
- Not every task needs all three stages
- But understanding the architecture helps with any task
- Show example: Literature review uses all three

---

### Slide 6: Tool Spotlight - Scite.ai
**What Makes Scite Different in 2026?**

**1. Smart Citations (1.4 Billion+)**
- Not just "who cited this paper"
- Shows if citations are SUPPORTING or DISPUTING
- Tracks methodology controversies
- Identifies retracted papers automatically

**2. Reference Check**
- Upload your manuscript before submission
- Scite scans your bibliography
- Flags retracted, disputed, or controversial sources
- Prevents embarrassing citation errors

**3. GPT-5.2 Integration**
- Scite Assistant uses healthcare-optimized reasoning models
- Provides cited answers with smart citation context
- Shows consensus vs outlier papers
- Parallel database searching for speed

**4. Topic Notifications**
- Get alerts when your research area has new citations
- Track how your own papers are being cited
- Monitor disputed vs supported status

**Speaker Notes:**
- Scite is THE verification layer for 2026
- This is what separates amateur from professional AI use
- Free version available, premium for power users
- This tool alone prevents most hallucination problems

---

### Slide 7: Scite.ai Demo Setup
**Instructor Preparation:**

**Choose a Research Question:**
- Example: "What is the current consensus on GLP-1 agonists for neuroprotection?"
- Or: "Are there disputed findings on the use of metformin in gestational diabetes?"

**What You'll Demonstrate:**
1. Ask question in Scite Assistant
2. Show "Smart Citations" view
3. Identify supporting vs disputing papers
4. Show consensus meter
5. Export citation list

**Key Teaching Points:**
- Notice the citation context snippets
- See how Scite identifies methodology disputes
- Observe the speed (parallel searching)
- Emphasize the audit trail

**Speaker Notes:**
- Have this prepared and tested
- Know your question and expected results
- Be ready to explain consensus meter
- Show both supported and disputed examples

---

### Slide 8: Live Demo - Stage 1 (Verification)
**Instructor Activity: Scite.ai in Action**

**Part 1: Ask the Question**
```
In Scite Assistant:
"What is the consensus on GLP-1 agonists for neuroprotection in 
Parkinson's disease? Show me the evidence quality."
```

**Part 2: Analyze the Results**
- How many papers cited?
- Supporting vs disputing ratio?
- Are there recent high-quality RCTs?
- Any retracted papers flagged?

**Part 3: Select Top Sources**
- Choose 3-5 highest quality papers
- Note the citation context
- Export to reference manager or copy citations

**Part 4: Discuss**
- "What did we just accomplish?"
- "How is this different from Google Scholar?"
- "What verification did Scite provide that ChatGPT couldn't?"

**Speaker Notes:**
- Take your time - this is critical demonstration
- Encourage questions during demo
- Highlight the verification features explicitly
- Connect to Week 4's verification techniques

---

### Slide 9: Live Demo - Stage 2 (Synthesis)
**Instructor Activity: NotebookLM for Organization**

**Setup:**
- Take the 3-5 papers from Stage 1
- Upload PDFs to NotebookLM
- Create a new notebook

**Part 1: Ask Synthesis Question**
```
Based on these papers, create a table comparing:
- Study design
- Patient population
- Dosage protocol
- Primary outcomes
- Limitations

Only use information from the uploaded papers. Cite page numbers.
```

**Part 2: Review Output**
- Is everything cited?
- Are there contradictions between papers?
- What gaps exist in the evidence?

**Part 3: Generate Audio Overview (Optional)**
- Show the "Deep Dive Conversation" feature
- Play 30 seconds of the podcast
- Discuss: When is this useful?

**Speaker Notes:**
- This demonstrates grounding from Week 5
- Emphasize the citation requirement
- Show how this prevents hallucinations
- NotebookLM only uses uploaded documents
- Connect to Week 5's RAG concepts

---

### Slide 10: Live Demo - Stage 3 (Drafting)
**Instructor Activity: Custom GPT for Final Output**

**Setup:**
- Have a Custom GPT ready (or use Claude/GPT-5 with good prompt)
- Input: The synthesis table from NotebookLM

**Part 1: Draft Request**
```
ROLE: You are a clinical research summarizer

CONTEXT: I need to brief my department on GLP-1 neuroprotection evidence

TASK: Write a 250-word summary suitable for clinicians

CONSTRAINTS:
- Use only the provided synthesis table
- Include citation to specific papers for each claim
- Identify consensus and areas of uncertainty
- Professional but accessible tone

THOUGHT PROCESS: First identify consensus findings, then note 
disagreements, finally highlight clinical implications
```

**Part 2: Review Draft**
- Does it follow constraints?
- Are citations present?
- Is it clinically useful?
- What needs refinement?

**Part 3: Red-Team Audit**
- Apply Week 4 techniques
- Check one claim against original paper
- Verify no hallucinated details
- Confirm uncertainty is acknowledged

**Speaker Notes:**
- This brings together Weeks 3, 4, and 5
- Show the complete pipeline in action
- Emphasize the audit step is non-negotiable
- Discuss when to iterate vs when it's ready

---

### Slide 11: The Complete Pipeline Workflow
**Summary of What We Just Did:**

```
QUESTION: What's the consensus on GLP-1 neuroprotection?
    ↓
STAGE 1 - VERIFICATION (Scite.ai)
→ Found 47 papers, 12 high-quality RCTs
→ Consensus meter: 78% supporting
→ Selected top 5 papers, no retractions
    ↓
STAGE 2 - SYNTHESIS (NotebookLM)
→ Uploaded 5 PDFs
→ Created comparison table with citations
→ Identified 2 methodological conflicts
    ↓
STAGE 3 - DRAFTING (Custom GPT/Claude)
→ Generated 250-word clinical summary
→ All claims cited to specific papers
→ Uncertainties clearly marked
    ↓
AUDIT (Red-Team from Week 4)
→ Verified 3 random claims against sources
→ Checked for hallucinated statistics
→ Confirmed appropriate hedging language
    ↓
FINAL OUTPUT: Department briefing ready for use
```

**Time Investment:** 25 minutes for verified, professional output

**Speaker Notes:**
- This is the model for professional AI workflows
- Each stage has a specific purpose
- Verification is built in at multiple points
- Human oversight at critical junctions
- Compare to 2024: "Ask ChatGPT" → hope it's right

---

### Slide 12: Real-World Orchestration Examples
**Clinical Use Cases:**

**1. Weekly Literature Review**
- Verification: Scite topic notifications + manual search
- Synthesis: NotebookLM for relevant papers
- Drafting: Custom GPT for standardized summary format
- Audit: Cross-check key claims

**2. Grant Proposal Preparation**
- Verification: Consensus.app for background evidence
- Synthesis: Claude (1M context) for related work section
- Drafting: Custom GPT with your institution's format
- Audit: Verify all statistics against original papers

**3. Patient Education Material**
- Verification: Scite for current clinical guidelines
- Synthesis: NotebookLM for guideline extraction
- Drafting: GPT-4o (fast) for patient-friendly language
- Audit: Medical review for accuracy and appropriateness

**4. IRB Submission**
- Verification: PubMed for protocol precedents
- Synthesis: NotebookLM for similar study designs
- Drafting: Custom GPT with IRB template
- Audit: Legal/compliance review layer

**Speaker Notes:**
- These are real workflows participants can use Monday
- Each adapts the three-stage pipeline
- Different tools may be swapped based on needs
- The architecture remains consistent

---

### Slide 13: The Rise of Clinical Agents
**What is an "Agent"?**
- AI that takes actions, not just answers questions
- Can access multiple tools autonomously
- Makes decisions within guardrails
- Requires human oversight at critical points

**2026 Clinical Agents:**

**Chart Hero (Penn Medicine)**
- Analyzes patient records automatically
- Suggests diagnostic pathways with source citations
- Flags potential drug interactions
- One-click access to evidence in EHR

**Ambient Scribes (Sunoh.ai, Abridge)**
- 320% adoption increase in 2025
- Converts patient conversations to structured notes
- Real-time documentation during visits
- Human physician approves/edits before finalizing

**Clinical Decision Support (Epic integration)**
- GPT-5 embedded in EHR workflows
- Proactive care suggestions based on guidelines
- Transparent citation to source guidelines
- Physician retains final decision authority

**Speaker Notes:**
- This is the future already happening
- Agents = next evolution beyond chat
- Critical difference: Transparent sourcing and human oversight
- Still experimental but growing fast
- Participants should be aware even if not using yet

---

### Slide 14: Agent Safety & Oversight
**The "Human Escape Hatch" Principle**

**As workflows become more autonomous, human oversight becomes MORE critical, not less.**

**Required Safeguards:**
1. **Transparent Sourcing:** Every agent recommendation must cite source
2. **Confidence Scoring:** Agent must indicate certainty level
3. **Human Approval:** No autonomous execution of critical actions
4. **Audit Trail:** Complete record of agent's reasoning process
5. **Fail-Safe Defaults:** When uncertain, escalate to human

**Red Flags to Watch:**
- Agent making recommendations without citations
- No confidence scores provided
- Pressure to accept suggestions without review
- Missing audit trail
- Claims of "human-level" or "superhuman" performance

**The Professional Standard:**
- Use agents as research assistants, not decision makers
- Always verify critical claims
- Maintain your clinical judgment
- Document your decision-making process

**Speaker Notes:**
- This connects to Week 4's ethics discussion
- Agents are powerful but require discipline
- The human clinician's role is more important, not less
- Professional responsibility cannot be delegated to AI

---

### Slide 15: Hands-On Activity - Workflow Design (20 min)
**Exercise:** Design Your Personal AI Workflow

**Step 1: Choose Your Task (5 min)**
- Select something you do at least weekly
- Examples: Literature review, case prep, teaching materials, admin reports
- Should have clear input and output

**Step 2: Map the Three Stages (10 min)**
- **Verification:** What tool will you use to find/verify evidence?
- **Synthesis:** What tool will organize your specific information?
- **Drafting:** What tool will create the final output?
- **Audit:** What will you check manually?

**Step 3: Identify Pain Points (5 min)**
- Where might hallucinations occur?
- What verification steps are critical?
- What human judgment is non-negotiable?
- How will you document the process?

**Template Provided:**
```
TASK: [What you're accomplishing]
INPUT: [What you start with]
OUTPUT: [What you need to deliver]

STAGE 1 - VERIFICATION:
Tool: [Scite/Consensus/PubMed]
Action: [What verification happens]
Output: [What moves to Stage 2]

STAGE 2 - SYNTHESIS:
Tool: [NotebookLM/Claude/Custom GPT]
Action: [How information is organized]
Output: [What moves to Stage 3]

STAGE 3 - DRAFTING:
Tool: [Custom GPT/Claude/GPT-5]
Action: [How final product is created]
Output: [Draft for audit]

AUDIT:
What I'll verify manually: [Specific checks]
Red flags to watch for: [Potential errors]

HUMAN ESCAPE HATCH:
Decision points requiring my judgment: [Critical junctions]
```

**Speaker Notes:**
- Circulate and provide feedback
- Encourage realistic, implementable workflows
- Help identify where verification is most critical
- Celebrate creative solutions

---

### Slide 16: Group Sharing - Workflow Gallery
**Prompt Participants:**
- "Who wants to share their workflow design?"
- "What verification stage felt most critical for your task?"
- "Where will you apply human judgment?"

**Capture Patterns:**
- Note common tasks across participants
- Identify shared pain points
- Celebrate innovative tool combinations
- Build shared workflow library

**Discussion Questions:**
- Which stage do you think will save you the most time?
- Where are you most worried about errors?
- How will you know if your workflow is working?
- What support do you need to implement this?

**Speaker Notes:**
- Have 2-3 backup examples if participants are shy
- Encourage peer learning
- Note workflows that could be shared department-wide
- Offer to help refine workflows after session

---

### Slide 17: Beyond the Basics - Advanced Orchestration
**For Those Ready to Go Deeper:**

**Multi-Model Consensus:**
- Run same prompt through GPT-5, Claude, and Gemini
- Compare outputs
- Identify consensus vs outlier responses
- Use for critical decisions

**Automated Audit Pipelines:**
- Use one model to generate
- Use another model to critique (with CoVe from Week 4)
- Human reviews discrepancies
- Reduces cognitive load on human reviewer

**Version Control for Prompts:**
- Track prompt iterations
- A/B test different approaches
- Build institutional prompt libraries
- Share best practices across teams

**Integration with Existing Systems:**
- API connections to your tools
- Automated workflows triggered by events
- Custom dashboards for oversight
- Institutional governance frameworks

**Speaker Notes:**
- This is optional advanced content
- For participants who want to push boundaries
- Acknowledge this requires technical support
- Point to resources for further learning

---

### Slide 18: Staying Current in 2026
**The Landscape Changes Monthly**

**Essential Resources:**

**Model Performance:**
- **Artificial Analysis:** Independent model benchmarks updated weekly
- **LMSYS Chatbot Arena:** Community voting on model quality
- Compare reasoning, speed, context handling

**Research Tools:**
- **Scite Topic Notifications:** Stay alerted to new citations
- **Consensus Weekly Digest:** Curated research summaries
- **PubMed AI Updates:** New AI-assisted search features

**Professional Development:**
- **CWRU AI Community:** Monthly updates and case studies
- **Healthcare AI Ethics Board:** Guidance on emerging issues
- **Vendor Roadmaps:** Track what's coming from OpenAI, Anthropic, Google

**Red Flags:**
- Overhyped "breakthrough" claims
- Tools without transparent sourcing
- Pressure to adopt without evaluation period
- Missing safety documentation

**Speaker Notes:**
- Landscape evolves faster than any curriculum
- Continuous learning is essential
- Community support helps filter signal from noise
- Skepticism and verification remain critical

---

### Slide 19: Series Synthesis - Your Complete Toolkit
**What You've Accomplished:**

**Week 1: Foundation**
- Understand the 2026 AI landscape
- Know what generative AI can and cannot do
- Recognize when to use AI vs traditional tools

**Week 2: Model Selection**
- Choose GPT-5 for reasoning, GPT-4o for speed
- Understand Claude's strengths with documents
- Leverage Gemini's massive context windows
- Navigate tradeoffs intelligently

**Week 3: Professional Prompting**
- Master the Five Pillars framework
- Engineer prompts, not just chat
- Build reusable prompt libraries
- Direct reasoning models effectively

**Week 4: Verification & Ethics**
- Apply Chain-of-Verification (CoVe)
- Conduct red-team audits
- Identify hallucinations
- Maintain ethical standards

**Week 5: Grounding & Agents**
- Use NotebookLM for document grounding
- Build Custom GPTs for workflows
- Understand RAG architecture
- Prevent hallucinations through grounding

**Week 6: Orchestration**
- Build multi-tool verification pipelines
- Use Scite for evidence verification
- Design professional workflows
- Maintain human oversight

**You now have a complete professional AI toolkit.**

**Speaker Notes:**
- This is a significant accomplishment
- Most healthcare professionals don't have this training
- Emphasize the systematic approach learned
- Acknowledge the commitment to complete the series

---

### Slide 20: Key Takeaways & Implementation
**Remember:**

**The Three-Stage Pipeline:**
1. VERIFICATION (Find evidence)
2. SYNTHESIS (Organize information)
3. DRAFTING (Create output)
Plus: RED-TEAM AUDIT before delivery

**Critical Principles:**
- Never use un-cited AI for clinical decisions
- Verification is non-negotiable
- Human oversight at critical junctions
- Continuous learning required
- Community support accelerates adoption

**Next Steps:**
1. **This Week:** Design one workflow for immediate use
2. **This Month:** Test and refine your workflow
3. **This Quarter:** Share with colleagues, build institutional library
4. **Ongoing:** Stay current, contribute to community

**Connection to Your Practice:**
- Start small: One workflow, used consistently
- Track time saved and quality improvements
- Document what works and what doesn't
- Share successes and failures with peers

**Speaker Notes:**
- Emphasize incremental implementation
- Perfection is not required, progress is
- Community learning accelerates everyone
- Offer ongoing support channels

---

### Slide 21: Final Assignment & Celebration
**Take-Home Assignment: "The 2026 Workflow Map"**

**Part A: Design Your Workflow**
- Choose a weekly task from your practice
- Map the three-stage pipeline
- Identify verification and audit points
- Document human decision points

**Part B: Test & Refine**
- Run your workflow at least twice
- Note what works and what breaks
- Iterate and improve
- Track time/quality metrics

**Part C: Share & Contribute**
- Bring your workflow map to next department meeting
- Share what you learned
- Help colleagues adapt for their needs
- Contribute to institutional knowledge base

**Bonus Challenge:**
- Build a Custom GPT for your most common task
- Create a reusable prompt template library
- Train a colleague on one tool you've mastered

**Closing Thoughts:**
- You're now in the top 5% of AI-literate healthcare professionals
- The skills you've learned will only become more valuable
- The community we've built continues beyond this series
- Your contributions will help others on this journey

**Thank you for your commitment, curiosity, and professional excellence.**

---

### Slide 22: Questions, Reflections & Next Steps
**Open Floor:**
- What are you most excited to implement?
- What concerns remain?
- What support do you need?
- What would you add to this series?

**Reflections:**
- How has your view of AI changed since Week 1?
- What surprised you most?
- What skill will you use first?

**Staying Connected:**
- Join the CWRU AI Community
- Opt in to monthly updates
- Access the ongoing resource library
- Participate in case study sessions

**Final Encouragement:**
- Start small, learn continuously
- Share generously, ask freely
- Maintain professional standards
- Trust the verification process

**Congratulations on completing the 2026 Clinical AI Excellence Series!**

---

## Teaching Tips

### Time Management (50 min)
- Slides 1-5: Welcome, Recap & Orchestration Concept (8 min)
- Slides 6-11: Scite Demo & Complete Pipeline (18 min)
- Slides 12-14: Clinical Agents & Safety (7 min)
- Slide 15-16: Hands-On Workflow Design & Sharing (15 min)
- Slides 17-22: Advanced Topics, Synthesis & Closing (7 min)

### Critical Demonstrations
**Must Prepare:**
1. **Scite.ai Demo:** Have research question ready, know expected results
2. **NotebookLM Demo:** Have PDFs pre-selected and ready to upload
3. **Complete Pipeline:** Practice the full workflow before class
4. **Workflow Template:** Have printed copies or digital template ready

### Common Student Questions

**Q: "This seems like a lot of work. Why not just use ChatGPT?"**
A: "For casual questions, ChatGPT is fine. But for clinical or research decisions, the verification pipeline prevents errors that could have serious consequences. The 25 minutes invested in proper orchestration saves hours of fixing errors or rebuilding trust."

**Q: "How do I know which tool to use for which stage?"**
A: "Start with the template: Scite/Consensus for verification, NotebookLM for your documents, Custom GPT for formatting. As you gain experience, you'll develop intuition for tool selection based on your specific needs."

**Q: "What if my institution doesn't have access to these tools?"**
A: "The principles work with free tools too. Use Google Scholar with careful verification instead of Scite. Use Claude's free tier instead of NotebookLM. The architecture matters more than the specific tools."

**Q: "How do I convince my colleagues to adopt these workflows?"**
A: "Start by using them yourself. Document time saved and quality improvements. Share your workflow maps. Offer to help one colleague at a time. Institutional adoption happens through demonstration, not declaration."

**Q: "What happens when these tools change or new ones emerge?"**
A: "The principles remain constant: verification, synthesis, drafting, audit. Tools will change, but the architecture of professional AI workflows stays the same. That's why we teach principles, not just tools."

**Q: "Is it safe to put patient data into these tools?"**
A: "That depends on your institution's data governance policies and the tool's compliance certifications. Many tools now have HIPAA-compliant enterprise versions. Always check with your compliance office before using AI with PHI."

### Backup Activities

**If Students Finish Workflow Design Early:**
1. **Peer Review:** Swap workflows with partner, suggest improvements
2. **Advanced Challenge:** Design multi-model consensus workflow
3. **Prompt Library:** Start building institutional prompt library
4. **Case Study:** Apply workflow to complex real-world scenario

**If Running Behind:**
- Skip Slides 17-18 (advanced content)
- Reduce workflow design to 15 minutes
- Assign workflow completion as homework
- Focus on core pipeline demonstration

**If Demo Technical Issues:**
- Have screenshots/screen recordings as backup
- Can walk through workflow conceptually
- Use participant's successful workflow as example
- Emphasize principles over specific tool mechanics

### Celebration & Closure

**Recognition:**
- Acknowledge the commitment to complete all six weeks
- Highlight growth from Week 1 to Week 6
- Celebrate specific participant breakthroughs
- Provide certificates or completion recognition

**Continuing Community:**
- Set up communication channel (Slack, email list)
- Schedule optional follow-up sessions
- Create shared resource repository
- Invite participants to present case studies

**Institutional Impact:**
- Offer to present findings to leadership
- Provide aggregated metrics if tracked
- Support department-level implementation
- Connect early adopters across institution

### Adaptation Notes

**For Advanced Participants:**
- Introduce API-based automation
- Discuss institutional governance frameworks
- Preview upcoming AI capabilities
- Challenge them to teach colleagues

**For Struggling Participants:**
- Provide simplified workflow template
- Pair with more advanced participants
- Focus on one tool at a time
- Offer individual follow-up support

**For Different Roles:**
- **Clinicians:** Focus on clinical decision support workflows
- **Researchers:** Emphasize literature review and grant workflows
- **Administrators:** Highlight reporting and communication workflows
- **Educators:** Showcase teaching material development workflows

### Post-Series Support

**Resource Pack Contents:**
1. Complete prompt library from all six weeks
2. Tool comparison guide with 2026 updates
3. Workflow templates for common tasks
4. Red-team audit checklist
5. One-page quick reference guides
6. Links to ongoing learning resources

**Follow-Up Opportunities:**
- Monthly "Office Hours" for Q&A
- Quarterly case study presentations
- Annual refresher on new tools/models
- Peer mentoring program
- Institutional AI community of practice

---

## Final Instructor Notes

**This Has Been a Journey:**
- From skepticism to competence
- From casual use to professional practice
- From individual tools to integrated systems
- From learners to teachers

**Your Role:**
- You've guided them through a fundamental transformation
- You've built a community, not just taught a class
- You've empowered professional excellence
- You've helped future-proof careers

**Looking Forward:**
- These participants will teach others
- Their workflows will become institutional standards
- Their questions will drive next version of this series
- Their success validates this investment

**Thank You for Teaching This Series.**

The healthcare professionals you've trained will make better decisions, save time on routine work, and have more capacity for the human elements of care that AI can never replace.

That's the ultimate goal: **AI as a tool for human excellence, not a replacement for human judgment.**

---

*Series Complete - Congratulations to All Participants!*
