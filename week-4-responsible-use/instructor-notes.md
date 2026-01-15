# Week 4: Advanced Prompting and Responsible Use
## Instructor Notes (Convert to Slides)

---

### Slide 1: Title & Welcome Back
**Title:** Advanced Prompting and Responsible Use  
**Subtitle:** Week 4 - Verification, Ethics, and Red-Team Auditing

**Quick Check-In:**
- Review Week 3 homework: Share one prompt from your library
- Did anyone try the "Five Pillars" on a reasoning model?
- Did you notice the difference in output quality?

**Speaker Notes:**
- Acknowledge that prompting takes practice
- Today we combine advanced techniques with critical evaluation
- Key theme: Just because a model shows its "Thinking Process" doesn't mean that process is correct

---

### Slide 2: Today's Goals
**What We'll Cover:**
- Part A: Advanced prompting techniques (Chain-of-Thought, Self-Consistency)
- Part B: Understanding AI errors (factual vs. logical hallucinations)
- Part C: Chain-of-Verification (CoVe) pattern
- Part D: Red-team auditing and adversarial testing
- Ethics, bias, and privacy throughout

**Speaker Notes:**
- This is our "trust but verify" week
- In 2026, AI is more persuasive than ever - verification is critical
- We're moving from "chatting" to "clinical auditing"

---

## Part A: Advanced Prompting Techniques (Slides 3-5)

### Slide 3: Chain-of-Thought (CoT) Reasoning
**Core Concept:** Make the AI show its work

**The Magic Phrase:**
```
Let's think through this step-by-step:
[Your question or problem]
```

**Example Comparison:**
- **Without CoT:** "Is Spironolactone appropriate for this patient?" → Brief yes/no
- **With CoT:** "Let's think step-by-step: Is Spironolactone appropriate for a patient with eGFR 25 and K+ 5.8?" → Shows reasoning about indication vs. contraindications

**Speaker Notes:**
- Demo this live with a medical example
- Show how CoT catches errors that quick responses miss
- Particularly important for reasoning models (GPT-5, Deep Think)

---

### Slide 4: Self-Consistency Verification
**Core Concept:** Generate multiple approaches and compare

**Pattern:**
```
Approach 1: [Solve using method A]
Approach 2: [Solve using method B]  
Now compare: Where do these agree or disagree?
```

**When to Use:**
- Complex calculations
- Diagnostic reasoning
- Multiple valid approaches exist
- High-stakes decisions

**Speaker Notes:**
- If different approaches reach same conclusion → confidence increases
- If they disagree → need human review
- Demo with a clinical calculation example

---

### Slide 5: Verification Prompts
**Core Concept:** Always ask the AI to check its own work

**Critical Follow-Up Questions:**
```
Check your response above:
- What assumptions did you make?
- What could be wrong with this reasoning?
- Are there alternative explanations?
- What evidence contradicts this conclusion?
```

**Speaker Notes:**
- This is "adversarial prompting" - asking AI to find its own flaws
- Often catches errors that weren't obvious in initial response
- Sets up red-team auditing later in session

---

## Part B: Understanding AI Errors (Slides 6-8)

### Slide 6: The Two Types of Hallucinations

**Type 1: Factual Hallucination**
- Definition: Making up data that doesn't exist
- Example: Inventing a lab value, fabricating a citation
- Status in 2026: Rare in modern models with grounding

**Type 2: Logical Hallucination** ⚠️
- Definition: Using real data but reaching an unsound conclusion
- Example: Correctly identifying K+ 5.8 but still recommending Spironolactone
- Status in 2026: **COMMON and critical to detect**

**Speaker Notes:**
- In 2024, AI made up facts. In 2026, it often makes up logic.
- Logical hallucinations are harder to spot - the data looks correct
- This is why verification is non-negotiable for clinical use

---

### Slide 7: Why Logical Hallucinations Happen
**Root Causes:**
- **Pattern Matching:** Model has seen "HFrEF → Spironolactone" many times
- **Missing Context:** Doesn't weigh contraindication as heavily as indication
- **Confirmation Bias:** Once committed to an answer, supports it
- **Complexity Collapse:** Simplifies multi-factor decisions

**Visual:** Show example of AI correctly listing all data points but missing the critical interaction

**Speaker Notes:**
- Even reasoning models can make these errors
- The "thinking" process shows the flaw - if you know how to look
- This is where red-team auditing becomes essential

---

### Slide 8: Red Flags for Hallucinations
**Warning Signs:**
- Overly confident about uncertain things
- Provides specific numbers without caveats
- Citations you can't verify
- Contradicts known guidelines
- Ignores stated constraints from prompt
- Reasoning doesn't match conclusion

**Action:** When you see these, ALWAYS verify independently

**Speaker Notes:**
- Share real example of a subtle logical error
- Emphasize: Plausible ≠ Correct
- Build the mindset: "Assume it's wrong until proven right"

---

## Part C: Chain-of-Verification Pattern (Slides 9-11)

### Slide 9: Introducing Chain-of-Verification (CoVe)
**What is CoVe?**
A 4-step prompting pattern that forces the AI to independently verify its own claims

**Why CoVe Matters:**
- Prevents confirmation bias
- Forces AI to find supporting evidence
- Identifies unverifiable claims
- Creates an audit trail

**When to Use:**
- Patient education materials
- Research summaries
- Clinical decision support
- Any high-stakes output

**Speaker Notes:**
- This is advanced prompting meets verification
- CoVe is becoming standard practice in medical AI applications
- The key is **independent** verification in Step 3

---

### Slide 10: The CoVe 4-Step Pattern

**Step 1: Generate Draft**
```
Based on this PDF, summarize the key findings.
```

**Step 2: Extract Claims**
```
Now, extract every specific claim you just made into a bulleted list.
```

**Step 3: Verify Each Claim (Critical!)**
```
For each claim, find the exact sentence in the original PDF that supports it.  
If you cannot find a direct quote, mark it as 'UNVERIFIED'.
```

**Step 4: Finalize**
```
Provide a final summary using only the 'VERIFIED' claims.
```

**Speaker Notes:**
- Step 3 is where the magic happens
- The AI must go back to source WITHOUT looking at its draft
- Claims that can't be verified get flagged
- Demo this live with a research abstract

---

### Slide 11: CoVe Live Demonstration
**Instructor Activity:**
1. Take a medical research abstract
2. Run through the 4-step CoVe pattern
3. Show how Step 3 catches overclaims or inferences
4. Compare final summary to initial draft - what changed?

**Discussion Points:**
- Which claims were marked UNVERIFIED?
- Did the final summary feel "less confident"? That's good!
- Where would this be useful in your work?

**Speaker Notes:**
- Have this prepared ahead of time
- Use a real example with nuanced findings
- Show both successes and limitations of the pattern

---

## Part D: Red-Team Auditing (Slides 12-16)

### Slide 12: What is "Red-Teaming"?
**Definition:** Adversarial testing where you actively try to break the AI's logic

**In Cybersecurity:** Red teams try to hack systems to find vulnerabilities  
**In AI:** We try to find logical flaws that standard reading would miss

**Mindset Shift:**
- Not: "Is this answer good?"
- But: "Can I find a way this answer is wrong?"

**Speaker Notes:**
- This is professional-grade AI use
- Essential for medical/legal/high-stakes applications
- Uncomfortable at first - we're trained to accept authority
- But AI isn't an authority - it's a prediction machine

---

### Slide 13: The 3-Step Audit Pipeline

**Step 1: Assertion Extraction**
Don't ask if the summary is "good." Ask the AI to list its facts.
```
Read the provided summary. List every discrete clinical assertion made  
regarding medication dosages, diagnostic conclusions, and follow-up timelines.  
Format as a bulleted list.
```

**Step 2: Evidence Anchor**
Force the AI to prove its work using the source document.
```
For every assertion listed in Step 1, find the exact sentence or lab value  
in the original patient record that supports it. If no direct evidence exists,  
label it 'INFERRED'.
```

**Step 3: Adversarial Cross-Examination** (The Red Team Moment)
```
Now, act as a Chief Medical Officer reviewing this plan. Identify one reason  
why the suggested treatment might be contraindicated based on the patient's  
comorbidities. Be highly critical. Do not defer to the previous summary's authority.
```

**Speaker Notes:**
- Step 3 is where safety happens
- The AI must actively argue against its own recommendation
- Often catches dangerous oversights

---

### Slide 14: Live Demo - The Metformin Trap
**Case Study Setup:**
```
Patient: 72yo Female  
Hx: Heart Failure (HFrEF), CKD Stage 3, Hypertension  
Labs: Potassium 5.6 mEq/L (High), Creatinine 1.9  
AI Plan: Patient's BP is still 150/90. Suggest starting Spironolactone 25mg daily  
to improve mortality outcomes and manage blood pressure.
```

**The Hidden Error:** 
- Spironolactone is life-saving in HFrEF ✓
- BUT contraindicated when K+ >5.0 with CKD ✗
- A "lazy" AI focuses on the benefit and ignores the hyperkalemia risk

**Instructor Demonstration:**
1. Show a standard model giving this recommendation
2. Run the 3-Step Audit Pipeline
3. Watch Step 3 catch the contraindication
4. Compare initial vs. audited recommendation

**Speaker Notes:**
- This is a real pattern of AI error
- The data is all correct - the logic is flawed
- Red-teaming saves lives in this scenario

---

### Slide 15: Hands-On Red-Team Exercise (20 min)
**Activity:** Students practice the 3-Step Audit Pipeline

**Provided Materials:**
- Clinical case study (see student handout)
- OR bring your own AI-generated summary

**Task:**
1. Run Step 1: Extract all assertions
2. Run Step 2: Find evidence for each
3. Run Step 3: Adversarial review
4. Document: Did Step 3 change the recommendation?

**Group Discussion After:**
- What did the adversarial prompt catch?
- Were you surprised by what changed?
- Where could you use this in your work?

**Speaker Notes:**
- Circulate and help
- Some students will find errors, some won't - both are learning
- Emphasize: This is a skill that improves with practice

---

### Slide 16: Ethics & Bias
**Ethical Considerations:**
- **Disclosure:** When and how to disclose AI use
- **Academic Integrity:** Following institutional policies
- **Professional Standards:** AI as assistant, not decision-maker
- **Patient Care:** Never use AI output without verification

**Understanding Bias:**
- Training data reflects historical imbalances
- Can perpetuate stereotypes in diagnoses, treatment recommendations
- Example: Pain management recommendations varying by demographic

**Mitigation Strategies:**
- Request multiple perspectives in prompts
- Question assumptions in AI outputs
- Use diverse examples
- Critical evaluation is non-negotiable

**Speaker Notes:**
- This isn't theoretical - real harms have occurred
- Discuss recent examples if available
- Emphasize institutional policies
- AI should expand perspectives, not narrow them

---

### Slide 17: Privacy & "Shadow AI"
**Never Share with Public AI:**
- Patient information (PHI/PII)
- Confidential research data
- Proprietary information
- Sensitive institutional data

**The "Shadow AI" Problem:**
- Definition: Using unapproved consumer AI tools for protected information
- Risk: Data becomes training data, privacy violations, compliance issues
- Rule: If the tool isn't in the "Institutional Safe Zone," don't use it for real data

**Best Practices:**
- De-identify before using
- Check privacy policies
- Use institutional AI instances when available
- Follow HIPAA/institutional guidelines

**Speaker Notes:**
- This is non-negotiable
- Share consequences if applicable
- Provide list of approved institutional tools
- Emphasize: Convenience doesn't override compliance

---

### Slide 18: Privacy Scenario Discussion
**Scenario 1:** "I want to use ChatGPT to help write a patient education handout about diabetes."
- ✓ Generic information is fine
- ✗ Don't paste actual patient questions with identifiers

**Scenario 2:** "Can I upload de-identified patient data for analysis?"
- Depends: Check if tool is approved for research data
- Verify: Is it truly de-identified? (no dates, locations, rare conditions)
- Better: Use institutional AI instances

**Scenario 3:** "I want to summarize a published research paper."
- ✓ Published information is public
- ✓ Fine to use any tool
- Note: Still verify the summary for accuracy

**Speaker Notes:**
- Use these as discussion prompts
- Have students generate other scenarios
- Clear up gray areas
- Provide written guidelines to take away

---

### Slide 19: Key Takeaways
**Advanced Techniques:**
- Chain-of-Thought: Make AI show its work
- Self-Consistency: Multiple approaches increase confidence
- Verification Prompts: Ask AI to check itself

**Verification:**
- Factual hallucinations: Rare
- Logical hallucinations: Common and critical
- Chain-of-Verification (CoVe): 4-step pattern for high-stakes work
- Red-Team Auditing: 3-step adversarial testing

**Responsible Use:**
- Ethics: Disclose AI use appropriately
- Bias: Question assumptions, seek diverse perspectives
- Privacy: Never share protected information with public tools

---

### Slide 20: Looking Ahead - Week 5
**Next Week: Knowledge Agents & Grounded AI**
- Build "Personal Brains" that don't hallucinate outside your sources
- NotebookLM for document-grounded responses
- Custom GPTs with system instructions
- RAG (Retrieval-Augmented Generation)

**Assignment for Next Week:**
**The "Logic Audit"**
1. Find a clinical guideline (2025/2026 ADA, ACC, etc.)
2. Upload to your AI and generate a 'lazy' summary
3. Run the 3-Step Audit Pipeline from today
4. Reflect: Did the adversarial prompt (Step 3) change the recommendation?
5. Write 2-3 paragraphs about what you learned

**Speaker Notes:**
- Emphasize: This assignment builds critical verification skills
- Next week's "grounded AI" will reduce need for red-teaming
- But verification will always be necessary

---

### Slide 21: Questions & Discussion
**Open Floor**

**Prompt Questions if Needed:**
- What verification technique will you try first?
- Where do you see bias risks in your domain?
- What questions do you have about privacy policies?
- How will you use red-team auditing in your work?

---

## Teaching Tips

### Time Management (50 min)
- Slides 1-2: Welcome & Goals (5 min)
- Slides 3-5: Advanced Prompting (8 min)
- Slides 6-8: Understanding Errors (7 min)
- Slides 9-11: CoVe Pattern (8 min)
- Slides 12-15: Red-Team Auditing (15 min - includes hands-on)
- Slides 16-18: Ethics & Privacy (5 min)
- Slides 19-21: Wrap-up (2 min)

### Critical Demonstrations
**Must Prepare:**
1. CoVe pattern with real research abstract (Slide 11)
2. Metformin/Spironolactone red-team demo (Slide 14)
3. Privacy scenarios (Slide 18)

### Common Questions

**Q: "Isn't this a lot of work just to verify AI output?"**
A: For routine tasks, maybe less verification needed. For clinical decisions, patient education, published work - absolutely worth it. The alternative is publishing or using dangerously flawed information.

**Q: "Will AI eventually not need verification?"**
A: Models are improving, but verification will remain important. Even humans need second opinions on complex decisions. Think of verification as standard practice, not a temporary workaround.

**Q: "How do I know if my prompt is 'adversarial' enough?"**
A: If the AI agrees with everything from its first response, push harder. Good adversarial prompts should surface at least some concerns or caveats.

**Q: "Can I use these techniques with any model?"**
A: Yes! CoVe and red-teaming work across all models. Reasoning models (GPT-5, Deep Think) may show more of their thought process, but the patterns work universally.

### Adaptation Notes

**If Short on Time:**
- Combine Slides 3-5 into brief overview
- Focus more time on red-team auditing (core skill)
- Assign CoVe practice as homework

**If Students Are Struggling:**
- Spend more time on simple CoT examples
- Do red-team exercise as guided group activity
- Provide template prompts for the assignment

**If Students Are Advanced:**
- Introduce "Constitutional AI" concept
- Discuss multi-agent verification systems
- Preview Week 6's orchestration early
- Have them create their own red-team scenarios

---

## Backup Materials

**If Live Demo Fails:**
- Have screenshots/video of CoVe in action
- Pre-prepared outputs showing before/after audit
- Written case studies for analysis

**Additional Case Studies:**
- Medication dosing errors
- Diagnostic reasoning flaws
- Citation fabrication examples
- Bias in treatment recommendations

**Further Reading:**
- Chain-of-Verification paper (if published)
- Institutional AI use policies
- HIPAA guidelines for AI
- Bias in medical AI literature

---

*Week 4 Complete - Ready for Week 5: Knowledge Agents*
