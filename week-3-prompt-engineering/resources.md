# Week 3: Prompt Engineering - Supplemental Resources
## Tools, Templates & Practice Materials

---

## 🔗 Essential Links

### AI Platforms for Practice
- **ChatGPT:** [chat.openai.com](https://chat.openai.com) - Free tier available, Plus for GPT-5
- **Claude:** [claude.ai](https://claude.ai) - Free tier available
- **Gemini:** [gemini.google.com](https://gemini.google.com) - Free access to Gemini 3
- **Institutional AI (CWRU):** [ai.case.edu](https://ai.case.edu) - Privacy-compliant for practice

### Prompt Engineering Resources
- **OpenAI Prompt Engineering Guide:** [platform.openai.com/docs/guides/prompt-engineering](https://platform.openai.com/docs/guides/prompt-engineering)
- **Anthropic Prompt Library:** [docs.anthropic.com/en/prompt-library/library](https://docs.anthropic.com/en/prompt-library/library)
- **Google AI Studio (Gemini Prompting):** [ai.google.dev](https://ai.google.dev)

---

## 📝 Prompt Templates for Medical Use

### Template 1: Clinical Summarization
```
ROLE: You are a Clinical Documentation Specialist with 15 years of experience.

CONTEXT: I need to create a concise summary for physician handoff during 
shift change. The receiving physician needs to understand the patient's 
current status quickly.

TASK: Distill the provided clinical notes into a structured handoff summary.

CONSTRAINTS:
- Maximum 200 words
- Use SBAR format (Situation, Background, Assessment, Recommendation)
- Include only active issues requiring follow-up
- Cite specific lab values and vital signs
- Do NOT include resolved issues from prior admissions

THOUGHT PROCESS: First, identify active problems from the current admission. 
Then, extract the most recent relevant labs and vitals. Finally, structure 
the summary in SBAR format with clear action items.
```

### Template 2: Literature Synthesis
```
ROLE: You are a Medical Research Librarian and Systematic Review Specialist.

CONTEXT: I need to synthesize findings from multiple research papers to 
support a grant proposal section on [TOPIC].

TASK: Compare and synthesize the methodologies and key findings from the 
provided papers.

CONSTRAINTS:
- Create a comparison table with columns: Study, Design, N, Key Finding, Limitations
- Maximum 300 words of narrative synthesis
- Identify consensus findings vs. conflicting results
- Do NOT make claims beyond what the papers explicitly state
- Cite specific papers for each assertion (Author, Year)

THOUGHT PROCESS: First, extract study design and sample size for each paper. 
Then, identify the primary outcome measures. Next, note where findings agree 
or conflict. Finally, summarize the strength of evidence.
```

### Template 3: Patient Education Material
```
ROLE: You are a Patient Education Specialist who excels at explaining 
complex medical concepts in accessible language.

CONTEXT: I need to create patient-facing materials explaining [CONDITION/PROCEDURE] 
for patients with 8th-grade reading level and no medical background.

TASK: Write a patient education handout explaining [TOPIC].

CONSTRAINTS:
- 8th-grade reading level (use readability checker)
- Maximum 400 words
- Use analogies and everyday examples
- Avoid medical jargon; if technical term is necessary, define it immediately
- Include "When to Call Your Doctor" section
- Do NOT provide specific medical advice or dosing information

THOUGHT PROCESS: First, identify the core concept that patients must understand. 
Then, find an everyday analogy that relates. Next, explain the what/why/how 
in simple terms. Finally, add actionable guidance for when to seek help.
```

### Template 4: Research Methodology Critique
```
ROLE: You are a Biostatistician and Research Methodology Expert.

CONTEXT: I am reviewing a manuscript for peer review and need to assess 
the methodological rigor.

TASK: Critique the research methodology described in the provided manuscript 
section, focusing on statistical validity and potential biases.

CONSTRAINTS:
- Focus only on methodology, not on clinical implications
- Identify specific issues with: sample size, randomization, blinding, 
  statistical tests, confounding variables
- For each issue, explain why it matters and suggest improvement
- Do NOT critique writing style or formatting
- Maximum 500 words

THOUGHT PROCESS: First, identify the study design and confirm appropriate 
statistical methods. Then, check for adequate power calculation. Next, assess 
randomization and blinding procedures. Then, examine confounding variable control. 
Finally, evaluate whether conclusions are supported by the analysis.
```

---

## 🎯 Practice Exercises

### Exercise 1: Transform Vague to Specific
**Original Vague Prompt:**
"Explain diabetes to a patient."

**Your Task:** Rewrite using all Five Pillars. Consider:
- What type of diabetes?
- What does the patient need to know for action?
- What's their health literacy level?
- What format works best?
- What should you avoid saying?

**Instructor Example Answer:**
```
ROLE: You are a Certified Diabetes Educator.

CONTEXT: A newly diagnosed Type 2 diabetes patient (age 55, no medical background) 
needs to understand lifestyle modifications before their next appointment in 2 weeks.

TASK: Explain the three most important daily actions they can take to manage 
blood sugar, using everyday examples.

CONSTRAINTS:
- 6th-grade reading level
- Maximum 150 words
- Use food analogies (not medical terms)
- Do NOT discuss medications (that's next visit)
- Include one specific example for each action

THOUGHT PROCESS: Focus on the three highest-impact behaviors: diet, exercise, 
monitoring. For each, provide one concrete, achievable daily action with an example.
```

---

### Exercise 2: Delimiter Practice
**Scenario:** You have a 50-page clinical guideline PDF. You need to extract only the sections relevant to elderly patients (>75 years).

**Your Prompt:**
```
### INSTRUCTIONS ###
Extract all recommendations from the provided guideline that specifically 
mention elderly patients, patients over 75, or geriatric considerations.

### SOURCE_DOCUMENT ###
[Paste or upload your 50-page guideline here]

### CONSTRAINTS ###
- Only include recommendations that explicitly mention age >75 or "elderly"
- Cite the page number for each recommendation
- If a recommendation mentions age ranges, include the full range
- Do NOT infer recommendations for elderly patients from general population data
- Format as bulleted list with [Page X] citation after each item
```

**Why This Works:**
- Delimiters help AI navigate long documents
- Clear boundaries prevent hallucination
- Page number requirement creates audit trail
- Negative constraint prevents inference

---

### Exercise 3: Reasoning Model Practice
**Scenario:** A patient has conflicting lab values. You need deep reasoning, not fast answers.

**For GPT-5 (Reasoning Model):**
```
Take your time to reason through this clinical puzzle step-by-step:

A 68-year-old patient presents with:
- Serum calcium: 11.8 mg/dL (elevated)
- PTH: 15 pg/mL (low-normal)
- Vitamin D: 18 ng/mL (low)

Show your step-by-step thinking to identify the most likely diagnosis and 
explain why the PTH is surprisingly low given the hypercalcemia.
```

**For GPT-4o (Predictive Model):**
```
Provide a concise differential diagnosis for:
- Serum calcium: 11.8 mg/dL (elevated)
- PTH: 15 pg/mL (low-normal)
- Vitamin D: 18 ng/mL (low)

List top 3 diagnoses with brief rationale.
```

**Compare Results:** The reasoning model should walk through PTH physiology and identify non-PTH-mediated hypercalcemia (malignancy, sarcoidosis, etc.). The predictive model gives quick list but less depth.

---

## 📚 Recommended Background Reading

### Understanding Language Models
- **"How Large Language Models Work" (Anthropic):** [www.anthropic.com/news/core-views-on-ai-safety](https://www.anthropic.com/news/core-views-on-ai-safety)
- **OpenAI Research on Reasoning:** [openai.com/research/learning-to-reason](https://openai.com/research/learning-to-reason) (Note: 2026 link may differ)

### Medical AI Ethics & Safety
- **AMA Guidelines on AI in Medicine:** Search "AMA AI ethics guidelines" for latest 2026 version
- **FDA AI/ML Software as Medical Device:** [www.fda.gov/medical-devices/software-medical-device-samd](https://www.fda.gov/medical-devices/software-medical-device-samd)

### Prompt Engineering Scholarship
- **"Chain-of-Thought Prompting"** (Wei et al.) - Original research on CoT
- **"Constitutional AI"** (Anthropic) - How Claude is trained to be helpful and harmless

---

## 🧪 Sample Data for Practice

### Clinical Scenario for Prompt Lab
**Use this for in-class exercises:**

**Patient Scenario:**
```
67-year-old female
Chief Complaint: Progressive dyspnea on exertion over 3 months

History:
- Hypertension (20 years)
- Type 2 Diabetes (15 years)
- Former smoker (quit 10 years ago, 30 pack-year history)

Medications:
- Lisinopril 20mg daily
- Metformin 1000mg BID
- Atorvastatin 40mg daily

Vitals:
- BP: 142/88
- HR: 88, regular
- RR: 20
- O2 Sat: 94% on room air

Physical Exam:
- Bilateral basilar crackles
- JVD at 45 degrees
- 2+ pitting edema bilateral lower extremities
- S3 gallop on cardiac exam

Labs:
- BNP: 890 pg/mL (elevated)
- Creatinine: 1.4 mg/dL (baseline 1.1)
- eGFR: 42 mL/min/1.73m²
- Potassium: 4.2 mEq/L
- HbA1c: 7.8%

Imaging:
- CXR: Cardiomegaly, bilateral pleural effusions
- Echo: EF 35%, LV dilation
```

**Practice Prompts to Try:**
1. Differential diagnosis with Five Pillars framework
2. Patient education material at 8th-grade level
3. Treatment plan with reasoning model showing thought process
4. Medication reconciliation checking for contraindications

---

## 💡 Common Pitfalls & Solutions

### Pitfall 1: Over-Constraining
**Problem:** "Write exactly 147 words about diabetes complications in iambic pentameter using only words starting with S."

**Solution:** Constraints should enhance clarity, not create artificial difficulty. Use constraints that serve your actual need (reading level, length, format).

### Pitfall 2: Under-Constraining
**Problem:** "Summarize this 500-page document."

**Solution:** Add specificity: "Summarize the methodology section of this 500-page document, focusing on sample selection and statistical analysis. Maximum 200 words."

### Pitfall 3: Mixing Multiple Tasks
**Problem:** "Summarize this paper, critique its methodology, write a patient handout, and create a bibliography in APA format."

**Solution:** One task per prompt. Chain prompts if needed: First summarize, then critique that summary, etc.

### Pitfall 4: No Verification Hook
**Problem:** Constraints don't include citation or source requirements.

**Solution:** Always add: "Cite specific sections/pages" or "Include evidence for each claim" to create audit trail.

---

## 🔄 Iteration Examples

### First Draft → Final Version

**Iteration 1 (Too Vague):**
```
Explain the SleepFM model.
```
*Output: Generic, technical explanation*

**Iteration 2 (Better, But Still Generic):**
```
Explain the SleepFM model in simple terms for a patient.
```
*Output: Less technical, but no context for why patient cares*

**Iteration 3 (Good Constraints):**
```
ROLE: You are a Sleep Medicine Specialist.
TASK: Explain how the SleepFM AI model helps predict heart problems 
from sleep data.
CONSTRAINTS: 8th-grade reading level, maximum 100 words, use analogy.
AUDIENCE: Patient considering home sleep study.
```
*Output: Clear, contextualized, appropriate*

**Iteration 4 (Professional-Grade):**
```
ROLE: You are a Sleep Medicine Specialist who excels at patient education.

CONTEXT: A patient is considering enrolling in a research study that uses 
AI to analyze their sleep data for heart risk prediction. They are anxious 
about "AI knowing their health" before they do.

TASK: Explain how the SleepFM model works and why it's useful for early 
detection, addressing their concern about AI and privacy.

CONSTRAINTS:
- 8th-grade reading level
- Maximum 120 words
- Use a "window into your body" analogy
- Address privacy concern directly but briefly
- End with one reassuring statement

THOUGHT PROCESS: First, explain what the AI "sees" in sleep patterns. 
Then, connect that to heart health using accessible analogy. Finally, 
briefly address privacy and emphasize patient control.
```
*Output: Precise, empathetic, addresses specific concern*

---

## 📖 Prompt Library Starter Templates

### Your Personal Library Structure
Create a document (Google Doc, Notion, or text file) with this structure:

```
# My Prompt Library

## Category: Clinical Documentation
### Prompt: Shift Handoff Summary
**Purpose:** Create SBAR handoff for shift change
**Last Updated:** [Date]
**Works Best With:** GPT-4o (speed), Claude (detail)

**Prompt:**
[Full text of prompt with all five pillars]

**Notes:**
- Works well for adult medicine patients
- Needs adjustment for pediatric cases (add growth/development)
- If output too long, adjust "active issues" constraint to "top 3 active issues"

**Sample Output:**
[Paste example of good output]

---

## Category: Research & Literature
### Prompt: Methodology Comparison Table
[Same structure repeated]

---

## Category: Patient Education
[Continue pattern]
```

---

## 🎓 Advanced Resources (Optional)

### For Those Who Want to Go Deeper

**Few-Shot Prompting:**
Provide examples within your prompt:
```
Create a patient-friendly explanation using this style:

Example 1:
Medical: "Hypertension is elevated blood pressure."
Patient-Friendly: "Your heart is pumping harder than it should, like a 
water pump working overtime."

Example 2:
Medical: "Hyperglycemia indicates elevated serum glucose."
Patient-Friendly: "There's too much sugar in your blood, like adding too 
much sugar to your coffee."

Now create one for: Hyperlipidemia
```

**System vs. User Prompts:**
- **System Prompt:** Sets overall behavior (in Custom GPTs, this is "Instructions")
- **User Prompt:** Individual requests within that framework

**Advanced Delimiters:**
```
<clinical_context>
[Patient data]
</clinical_context>

<guidelines>
[Treatment guidelines]
</guidelines>

<query>
Based ONLY on the clinical_context and guidelines above, recommend treatment.
</query>
```

---

## ✅ Week 3 Checklist

Before next week, you should have:
- [ ] Created accounts on ChatGPT, Claude, and Gemini (if not already)
- [ ] Built 3 prompts using the Five Pillars framework
- [ ] Tested each prompt and iterated at least once
- [ ] Started a prompt library document
- [ ] Compared one prompt between reasoning (GPT-5) and predictive (GPT-4o) models
- [ ] Saved your best prompts for use in Week 4's verification exercises

---

## 🆘 Help & Support

**Technical Issues:**
- ChatGPT Support: [help.openai.com](https://help.openai.com)
- Claude Support: [support.anthropic.com](https://support.anthropic.com)
- Gemini Support: [support.google.com/gemini](https://support.google.com/gemini)

**Institutional Resources:**
- CWRU AI Support: [Contact your IT department]
- HIPAA-Compliant AI: Use ONLY institutionally-approved compliant tools



*These resources supplement Week 3 instructor notes and student handout. Use them as reference materials throughout the series.*
