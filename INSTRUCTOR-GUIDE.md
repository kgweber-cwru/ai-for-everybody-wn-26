# Series 1: Instructor Guide
## Understanding and Using Generative AI

---

## Overview for Instructors

This guide provides essential information for instructors teaching the 6-week "Understanding and Using Generative AI" series. Each week's specific content is contained in the `instructor-notes.md` file within that week's subdirectory.

---

## Series Structure

### Format
- **Duration:** 6 weeks
- **Session Length:** 50 minutes per week
- **Delivery:** In-person preferred; hybrid possible
- **Audience:** Faculty, staff, students - all backgrounds
- **Prerequisites:** None (no coding required)

### Teaching Philosophy
- **Hands-on focus:** Participants experiment with tools, not just learn about them
- **Progressive learning:** Each week builds on previous content
- **Practical applications:** Real-world use cases from healthcare, research, and academia
- **Responsible use:** Ethics, bias, and privacy integrated throughout

---

## Week-by-Week Overview

### Week 1: Introduction to Generative AI
**Learning Objectives:**
- Understand how large language models work conceptually
- Create accounts and try first prompts
- Identify capabilities and limitations

**Key Deliverables:** Account setup, first experiments, model comparison assignment

**Instructor Prep:**
- Test all tool logins beforehand
- Have backup demonstrations ready
- Prepare troubleshooting resources for account setup

---

### Week 2: Model Differences and Selection
**Learning Objectives:**
- Compare ChatGPT, Claude, and Gemini
- Understand reasoning vs. prediction models
- Choose appropriate tools for different tasks

**Key Deliverables:** Comparative testing across models, real-world application

**Instructor Prep:**
- Demo same prompt across multiple models
- Emphasize "reasoning pause" in GPT-5/Deep Think models
- Prepare examples of when each model excels

---

### Week 3: Prompt Engineering Fundamentals
**Learning Objectives:**
- Master the Five Pillars of effective prompting (ROLE, CONTEXT, TASK, CONSTRAINTS, THOUGHT PROCESS)
- Direct reasoning models effectively
- Handle large context windows (1M+ tokens)

**Key Deliverables:** Build personal prompt library, practice advanced patterns

**Instructor Prep:**
- Show "lazy" vs. "engineered" prompt comparisons
- Demonstrate delimiter use for massive context
- Connect to Week 2's reasoning models

---

### Week 4: Advanced Prompting and Responsible Use
**Learning Objectives:**
- Use Chain-of-Thought and Chain-of-Verification patterns
- Identify factual and logical hallucinations
- Perform red-team auditing of AI outputs
- Understand ethical considerations and privacy requirements

**Key Deliverables:** Verification strategies, logic audit assignment

**Instructor Prep:**
- Prepare clinical case study demonstrating logical hallucination
- Have real examples of AI making dangerous recommendations
- Emphasize institutional AI policies (PHI protection)

---

### Week 5: Knowledge Agents & Grounded AI
**Learning Objectives:**
- Use NotebookLM for document-grounded analysis
- Create Custom GPTs with system instructions
- Understand RAG (Retrieval-Augmented Generation)

**Key Deliverables:** NotebookLM project, Custom GPT design

**Instructor Prep:**
- Pre-load NotebookLM with sample conflicting guidelines
- Generate Audio Overview to demonstrate feature
- Show citation tracing in action

---

### Week 6: Orchestration & Building Your AI Workflow
**Learning Objectives:**
- Integrate multi-tool workflows
- Use Scite for research verification
- Understand agentic AI in healthcare
- Build complete verification pipelines

**Key Deliverables:** Personal AI workflow map

**Instructor Prep:**
- Demonstrate complete pipeline (Scite → NotebookLM → Custom GPT)
- Show Scite's Smart Citations and retraction detection
- Prepare examples of workflow orchestration

---

## Teaching Best Practices

### Time Management (50 min sessions)
```
0-5 min:    Welcome & review previous week's assignment
5-20 min:   Core concepts (lecture/demo)
20-40 min:  Hands-on experimentation
40-48 min:  Discussion & questions
48-50 min:  Preview next week & assign homework
```

### Engagement Strategies
- **Start with their questions:** Begin each session asking what they tried and what confused them
- **Show failures:** Demonstrate when AI gets things wrong - it's instructive
- **Use their examples:** Ask for domain-specific scenarios from participants
- **Pair participants:** Mix technical comfort levels for peer support
- **Celebrate discoveries:** Acknowledge when participants find interesting use cases

### Common Challenges & Solutions

**Challenge:** Varied technical comfort levels
**Solution:** 
- Normalize asking questions
- Pair more/less experienced participants
- Provide written step-by-step guides
- Offer optional office hours

**Challenge:** Account setup issues
**Solution:**
- Send setup instructions 1 week before Week 1
- Have backup demonstration account ready
- Test on multiple browsers beforehand
- Know workarounds for common issues

**Challenge:** Participants want to dive deeper
**Solution:**
- Have "advanced track" resources ready
- Point to API documentation for coders
- Suggest office hours for specific use cases
- Connect them with community resources

**Challenge:** Participants concerned about ethics/job displacement
**Solution:**
- Address directly and honestly
- Emphasize AI as augmentation, not replacement
- Discuss institutional policies
- Provide framework for responsible use

---

## Assessment & Feedback

### Formative Assessment
- Weekly assignments (review but don't grade)
- Hands-on participation observation
- Discussion contributions
- Questions asked (engagement indicator)

### Summative Assessment (Optional)
- Week 6 workflow map
- Series reflection essay
- Prompt library portfolio
- Certificate of completion

### Collecting Feedback
- Mid-series check-in (after Week 3)
- End-of-session quick polls
- Final series evaluation
- 1-month follow-up survey (adoption tracking)

---

## Materials Organization

### Each Week Contains:
```
week-X-topic/
├── instructor-notes.md    ← Complete slide deck outline + teaching tips
└── student-handout.md     ← Concepts, exercises, assignments
```

### Root Directory Contains:
```
series-1-basics/
├── INSTRUCTOR-GUIDE.md     ← This file (general teaching guidance)
├── README.md               ← Series overview and structure
├── FLIER-COPY.md           ← Marketing/promotional copy
├── CONSISTENCY-REVIEW.md   ← Quality assurance documentation
└── week-X-topic/           ← Individual week materials
```

---

## Adaptation Guidelines

### For Different Audiences

**Healthcare/Clinical:**
- Emphasize patient education examples
- Use clinical case studies
- Discuss EHR integration possibilities
- Address HIPAA/PHI concerns prominently

**Research/Academic:**
- Focus on literature review applications
- Grant writing examples
- Data analysis interpretation
- Research methodology support

**Administrative:**
- Communication and reporting examples
- Process documentation
- Policy analysis
- Meeting preparation

### For Different Timeframes

**Intensive Workshop (2-3 days):**
- Combine Weeks 1-2 on Day 1
- Combine Weeks 3-4 on Day 2
- Combine Weeks 5-6 on Day 3
- Extend hands-on time
- Reduce take-home assignments

**Extended Timeline (12 weeks):**
- Split complex weeks into 2 sessions
- Add extra practice time
- Include guest speakers
- Incorporate project work time

**Self-Paced Online:**
- Record demonstrations
- Provide discussion forums
- Extend assignment deadlines
- Schedule optional live Q&A sessions

---

## Technical Requirements

### For Instructors:
- Laptop with reliable internet
- Projector/screen sharing capability
- Active accounts on: ChatGPT, Claude, Gemini, NotebookLM, Scite
- Backup demonstration materials (screenshots/videos)
- Guest wifi access for participants (if needed)

### For Participants:
- Laptop (tablets less ideal for hands-on work)
- Internet access
- Email address for account creation
- Optional: headphones for audio features

---

## Troubleshooting Resources

### Account Access Issues
- **Email verification delays:** Check spam folder, try re-sending
- **Geographic restrictions:** Rare but may require VPN
- **Institutional firewalls:** Work with IT beforehand
- **Phone verification:** Some services require real number

### Tool-Specific Issues
- **ChatGPT overloaded:** Try different time or use Claude
- **NotebookLM upload limits:** Break into smaller documents
- **Scite paywall:** Use free tier demonstrations, institutional access
- **Custom GPT creation:** Requires ChatGPT Plus subscription

### Teaching Environment Issues
- **No internet:** Have offline demonstrations ready
- **Projector failure:** Use participant screen shares
- **Tool outage:** Have backup activities prepared
- **Too many questions:** Schedule extended Q&A session

---

## Additional Resources

### For Continued Learning:
- **Official Documentation:** 
  - OpenAI Help Center (help.openai.com)
  - Anthropic Documentation (docs.anthropic.com)
  - Google Gemini Support (support.google.com/gemini)

### For Instructors:
- **Model Comparison:** Artificial Analysis (artificialanalysis.ai)
- **Benchmark Tracking:** LMSys Chatbot Arena
- **AI News:** Regular updates from OpenAI, Anthropic, Google blogs

### For Building Community:
- Set up discussion channel (Slack, Teams, etc.)
- Schedule optional office hours
- Create shared prompt library
- Organize follow-up sessions (3-month check-in)

---

## Version Control & Updates

**Current Version:** January 2026

**Review Schedule:**
- Minor updates: As new features release
- Major review: Every 6 months or after significant tool changes
- Content refresh: Annually

**Note:** The AI landscape evolves rapidly. Instructors should:
- Monitor major announcements from AI companies
- Test new features before incorporating
- Update examples to reflect current capabilities
- Maintain backward compatibility where possible

---

## Contact & Support

**For Questions About This Series:**
[Add appropriate contact information]

**For Technical Issues:**
[Add IT support contact]

**For Content Suggestions:**
[Add content owner contact]

---

*Last Updated: January 2026*