# Week 4: Responsible Use & Verification - Supplemental Resources
## Chain-of-Verification, Red-Team Auditing & Clinical Ethics Materials

---

## 🔗 Essential Links

### Verification Tools
- **OpenAI Fact-Checking Best Practices:** [platform.openai.com/docs/guides/safety-best-practices](https://platform.openai.com/docs/guides/safety-best-practices)
- **Anthropic's Claude Constitutional AI:** [www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback](https://www.anthropic.com/news/constitutional-ai-harmlessness-from-ai-feedback)

### Medical Guidelines for Practice
- **American College of Cardiology Guidelines:** [www.acc.org/guidelines](https://www.acc.org/guidelines)
- **American Diabetes Association Standards:** [diabetesjournals.org/care/issue/47/Supplement_1](https://diabetesjournals.org/care/issue/47/Supplement_1) (2026 edition)
- **NCCN Guidelines (Oncology):** [www.nccn.org/guidelines](https://www.nccn.org/guidelines) (requires free registration)
- **UpToDate Clinical Guidelines:** [www.uptodate.com](https://www.uptodate.com) (institutional access required)

### AI Ethics & Governance
- **AMA Principles for AI in Medicine:** [www.ama-assn.org/practice-management/digital/augmented-intelligence-ai](https://www.ama-assn.org/practice-management/digital/augmented-intelligence-ai)
- **FDA AI/ML Medical Devices:** [www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-aiml-enabled-medical-devices](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-aiml-enabled-medical-devices)
- **WHO AI Ethics Guidelines:** Search "WHO AI ethics health" for 2026 version

---

## 📝 Chain-of-Verification (CoVe) Templates

### CoVe Template 1: Clinical Guideline Summary
**Use this when summarizing treatment guidelines:**

```
STEP 1 - INITIAL GENERATION:
Prompt: "Based on the [2026 ADA Diabetes Guidelines] provided, summarize 
the first-line treatment recommendations for newly diagnosed Type 2 diabetes 
in adults without contraindications."

STEP 2 - CLAIM EXTRACTION:
Prompt: "List every specific clinical claim you made in the summary above. 
Format as numbered list. Include dosages, timeframes, and any quantitative 
recommendations."

STEP 3 - VERIFICATION:
Prompt: "For each claim in the list above, find the exact sentence or table 
in the original guideline document that supports it. Provide page number and 
section heading. If no direct evidence exists, mark as 'UNVERIFIED - INFERRED'."

STEP 4 - VERIFIED SUMMARY:
Prompt: "Create a final summary using ONLY the claims marked as verified in 
Step 3. For each statement, include parenthetical citation (Section, Page)."
```

---

### CoVe Template 2: Patient Case Summary
**Use this for clinical documentation:**

```
STEP 1 - INITIAL GENERATION:
Prompt: "Based on the patient chart provided, create an SBAR summary for 
physician handoff. Focus on active issues and pending decisions."

STEP 2 - CLAIM EXTRACTION:
Prompt: "Extract every discrete clinical assertion from your SBAR above:
- Lab values
- Vital sign trends
- Medication recommendations
- Pending tests or consultations
Format as bulleted list."

STEP 3 - VERIFICATION:
Prompt: "For each assertion, identify the specific chart entry (date, time, 
source) that supports it. Mark any inferences or assumptions as 'INFERRED'."

STEP 4 - VERIFIED SUMMARY:
Prompt: "Rewrite the SBAR using only verified facts. For inferred items, 
clearly label them as clinical impressions rather than documented facts. 
Use format: '[VERIFIED] ...' or '[CLINICAL IMPRESSION] ...'"
```

---

## 🛡️ Red-Team Audit Scripts

### 3-Step Red-Team Pipeline

**STEP 1: FACT LIST**
```
Read the AI-generated summary below. List every discrete clinical assertion 
made regarding:
- Medication dosages
- Lab value thresholds
- Diagnostic criteria
- Treatment timelines
- Contraindications

Format as numbered list. Be exhaustive.

[Paste AI output here]
```

**STEP 2: EVIDENCE ANCHOR**
```
For every assertion listed in Step 1, find the exact sentence, lab value, 
or guideline statement in the source document that supports it.

Format as:
1. [Assertion] → Source: [Exact quote] (Page X, Section Y)

If no direct evidence exists, label as:
1. [Assertion] → INFERRED (No direct source found)
```

**STEP 3: ADVERSARIAL CROSS-EXAMINATION**
```
Now, act as a Chief Medical Officer conducting a critical safety review. 
Your job is to find potential errors, not to validate the plan.

Analyze the treatment plan above and identify:
1. One contraindication based on patient comorbidities
2. One drug-drug interaction risk
3. One renal or hepatic dosing consideration that may have been missed

Be highly critical. Do not defer to the previous summary's authority.
```

---

## 🧪 Practice Case Studies

### Case Study 1: The Spironolactone Dilemma
**Patient Data:**
```
Patient: 72-year-old Female
History: Heart Failure (HFrEF, EF 30%), CKD Stage 3, Hypertension
Labs: 
- Potassium: 5.6 mEq/L (High)
- Creatinine: 1.9 mg/dL
- eGFR: 32 mL/min/1.73m²
Blood Pressure: 150/90 mmHg (elevated)

Current Medications:
- Lisinopril 20mg daily
- Metoprolol 50mg BID
- Furosemide 40mg daily
```

**The Setup:**
Paste this into AI with prompt:
```
Based on this patient's Heart Failure with reduced ejection fraction (HFrEF) 
and persistent hypertension, recommend medication adjustments to improve 
outcomes and blood pressure control.
```

**Expected Error:**
Many AI models will suggest adding Spironolactone (proven mortality benefit in HFrEF) but may downplay or miss the significant hyperkalemia risk given K+ already 5.6 and CKD.

**Red-Team Exercise:**
Run the 3-step pipeline. Does Step 3 (Adversarial) catch the potassium risk?

**Teaching Point:**
This demonstrates "logical hallucination" - the AI has correct knowledge about HFrEF and Spironolactone benefits, but fails to integrate all patient-specific risk factors.

---

### Case Study 2: Anticoagulation in Elderly Patient
**Patient Data:**
```
Patient: 84-year-old Male
History: Atrial Fibrillation (CHA2DS2-VASc score: 5), History of falls (3 in past year)
Labs:
- Creatinine: 2.1 mg/dL
- eGFR: 28 mL/min/1.73m²
- Hemoglobin: 10.2 g/dL (mild anemia)
Weight: 58 kg

Current Medications:
- Diltiazem 240mg daily
- ASA 81mg daily
```

**The Prompt:**
```
This patient has atrial fibrillation with high stroke risk (CHA2DS2-VASc: 5). 
Recommend anticoagulation strategy.
```

**Expected Issues to Catch:**
- Renal dosing adjustments for DOACs
- Fall risk vs stroke risk assessment
- Bleeding risk factors (age, anemia, low weight)
- May need apixaban dose adjustment or avoid certain agents

**Red-Team Focus:**
Step 3 should identify bleeding risk factors and renal dosing requirements.

---

### Case Study 3: Metformin in CKD
**Patient Data:**
```
Patient: 65-year-old Female
History: Type 2 Diabetes (A1c 8.2%), CKD Stage 3b
Labs:
- eGFR: 38 mL/min/1.73m²
- Creatinine: 1.6 mg/dL
- Stable over past 6 months

Current: Diet controlled, no diabetes medications
```

**The Prompt:**
```
Patient has uncontrolled Type 2 diabetes (A1c 8.2%). Recommend first-line 
pharmacologic therapy.
```

**Expected Response:**
AI should recommend Metformin (correct first-line agent) BUT must address eGFR consideration.

**What to Verify:**
- Does AI mention eGFR threshold? (Metformin can be used with eGFR ≥30, avoided if <30)
- Does it recommend dose adjustment?
- Does it mention monitoring for lactic acidosis risk?

**Red-Team Step 3:**
Should identify: "Metformin dose should be reduced (max 1000mg daily) given eGFR 38, with close monitoring for GI symptoms and lactic acidosis risk. Discontinue if eGFR drops below 30."

---

## ⚖️ Ethics Decision Trees

### Privacy & PHI Decision Tree

**Question 1: Does this task involve real patient data?**
- YES → Go to Question 2
- NO → Standard AI tools OK (but still verify outputs)

**Question 2: Can the data be fully de-identified?**
- YES → De-identify, then use standard tools. Document de-identification process.
- NO → Go to Question 3

**Question 3: Is there institutional HIPAA-compliant AI available?**
- YES → Use institutionally-approved AI. Document usage.
- NO → Do not use AI for this task. Use traditional methods.

**De-Identification Checklist:**
- [ ] Remove all names (patient, family, providers)
- [ ] Remove all dates (use relative: "3 months ago" instead of "October 2025")
- [ ] Remove MRN, account numbers, device IDs
- [ ] Remove addresses, phone numbers, emails
- [ ] Remove ages >89 (use ">89" instead of specific age)
- [ ] Remove unique characteristics (rare diseases, unusual circumstances)
- [ ] Consider: Could this case be identified from available information?

---

### Bias Assessment Checklist

**When reviewing AI output, check for:**

- [ ] **Default Demographic Assumptions:** Did AI assume patient gender, race, or socioeconomic status not stated in prompt?
- [ ] **Cultural Insensitivity:** Are recommendations culturally appropriate? (diet, lifestyle, family structure assumptions)
- [ ] **Age Bias:** Did AI apply standards appropriate for patient age? (e.g., aggressive treatment in elderly, dismissing symptoms in young patients)
- [ ] **Language Accessibility:** Is patient education material accessible to non-English speakers or low health literacy?
- [ ] **Access Assumptions:** Did AI recommend resources that may not be accessible (expensive medications, specialist referrals in underserved areas)?
- [ ] **Research Bias:** Are recommendations based on diverse study populations or primarily one demographic?

**If any box checked, revise prompt to explicitly address:**
```
Additional constraint: Ensure recommendations are appropriate for [specific 
patient demographics] and consider [access/cultural factors]. Do not make 
assumptions about [unstated characteristics].
```

---

## 📚 Recommended Reading

### Academic Papers on AI Verification

**Chain-of-Verification Prompting:**
- "Chain-of-Verification Reduces Hallucination in Large Language Models" (2023)
- Search: Google Scholar for latest citations and applications

**AI in Clinical Decision-Making:**
- "Large Language Models in Medicine" - *New England Journal of Medicine* (search for 2025-2026 updates)
- "Clinical Validation of AI-Generated Medical Text" - Recent publications in *JAMA* or *Nature Medicine*

### Clinical Guidelines for Common Scenarios

**Download and Practice With:**
1. **AHA/ACC Heart Failure Guidelines** - Free PDF from acc.org
2. **ADA Diabetes Standards of Care** - Updated annually, free access
3. **KDIGO CKD Guidelines** - Free from kdigo.org
4. **IDSA Antimicrobial Guidelines** - Free access for members

**Practice Exercise:** 
- Upload one guideline to AI
- Ask for treatment summary
- Run CoVe verification
- Check if AI correctly cited sections

---

## 🔬 Advanced Verification Techniques

### Self-Consistency Checking

**Technique:** Ask same question multiple times with different framing, compare answers.

**Example:**
```
Prompt 1: "What is the recommended first-line antihypertensive for a 
60-year-old Black patient with no other comorbidities?"

Prompt 2: "For a 60-year-old patient of African ancestry with uncomplicated 
hypertension, list the JNC-8 recommended initial therapy."

Prompt 3: "According to current hypertension guidelines, what class of 
medication should be started first in a Black adult with essential hypertension?"
```

**Verification:** Do all three prompts give consistent answers? If not, which is correct according to guidelines (JNC-8 recommends CCB or thiazide diuretic for Black patients, not ACEi/ARB first-line).

---

### Multi-Model Consensus

**Technique:** Run same prompt through GPT-5, Claude, and Gemini. Compare outputs.

**When Useful:**
- High-stakes clinical decisions
- Controversial or evolving topics
- Areas with conflicting guidelines

**How to Interpret:**
- **All agree:** Higher confidence (but still verify against primary sources)
- **One differs:** Investigate which has better evidence
- **All differ:** Red flag - consult primary literature directly

---

### Citation Validation

**Always Verify:**
1. **Does the citation actually exist?** (AI may generate plausible-looking fake citations)
2. **Does the cited source say what AI claims?** (Check the actual page/section)
3. **Is the citation current?** (Using 2020 guideline when 2026 exists)
4. **Is the citation appropriate authority?** (Blog post vs peer-reviewed guideline)

**How to Check:**
- PubMed: [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov)
- Google Scholar: [scholar.google.com](https://scholar.google.com)
- DOI lookup: [doi.org](https://doi.org)
- Direct guideline websites (ACC, ADA, NCCN, etc.)

---

## 🎯 Weekly Practice Schedule

### Day 1-2: CoVe Mastery
- Select one clinical guideline
- Ask AI to summarize a specific section
- Run full 4-step CoVe process
- Document: What did Step 3 reveal that Step 1 missed?

### Day 3-4: Red-Team Practice
- Use one of the case studies provided
- Run complete 3-step red-team pipeline
- Did Step 3 (Adversarial) identify safety issues?
- Refine your adversarial prompts for better detection

### Day 5-6: Ethics Review
- Review your Week 3 prompts
- Apply bias assessment checklist
- Revise prompts to address any issues
- Document changes made

### Day 7: Integration
- Take one real task from your work
- Apply both CoVe AND red-team verification
- Document time investment vs confidence in output
- Compare to traditional (non-AI) approach

---

## 💡 Common Verification Pitfalls

### Pitfall 1: Over-Trusting Formatted Output
**Problem:** AI presents information in tables, bullet points, or professional formatting - looks authoritative.

**Solution:** Format ≠ Accuracy. Verify content regardless of presentation.

### Pitfall 2: Citation Illusion
**Problem:** AI provides "citations" that look real but may be fabricated.

**Solution:** Verify every citation. Look up the DOI or PubMed ID. Check the actual page cited.

### Pitfall 3: Verification Fatigue
**Problem:** After verifying first few claims, you trust the rest without checking.

**Solution:** Use sampling strategy - verify 100% of high-stakes claims (dosages, contraindications), 50% of moderate-stakes, 25% of low-stakes. If errors found, increase sampling rate.

### Pitfall 4: Confirmation Bias
**Problem:** You verify only the claims that align with your existing beliefs.

**Solution:** Specifically verify claims that surprise you or contradict your expectations - these are where AI errors are most dangerous.

---

## ✅ Week 4 Checklist

Before Week 5, you should have:
- [ ] Practiced CoVe on at least one clinical guideline summary
- [ ] Completed 3-step red-team audit on at least two case studies
- [ ] Identified one bias or assumption in an AI output
- [ ] Verified at least 3 AI-generated citations (checked actual sources)
- [ ] Documented one instance where adversarial prompting revealed an error
- [ ] Updated your Week 3 prompt library with verification steps
- [ ] Reviewed your institution's AI governance policy (if available)

---

## 🆘 Help & Support

**Verification Tools:**
- PubMed: [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov)
- Cochrane Library: [www.cochranelibrary.com](https://www.cochranelibrary.com)
- Clinical Guidelines: See links at top of document

**Ethics Consultation:**
- Your institution's IRB/Ethics Board
- AMA Ethics Hotline (if available)
- Professional society ethics resources

**Technical Support:**
- Same as Week 3 (ChatGPT, Claude, Gemini support sites)

---

*These resources supplement Week 4 instructor notes and student handout. Practice verification techniques on low-stakes tasks before applying to clinical decisions.*
