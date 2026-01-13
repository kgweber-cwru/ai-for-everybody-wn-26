# Week 4: Advanced Prompting & Responsible Use - Verification & Clinical Ethics
## Student Handout

---

### Part A: Advanced Prompting Techniques (Foundation)

## Chain-of-Thought (CoT) Reasoning
When you need reliable reasoning for complex tasks, explicitly ask the model to show its work:

**Basic CoT Prompt:**
```
Let's think through this step-by-step:
[Your question or problem]
```

**Example (Medical):**
```
Let's think through this step-by-step:
A patient has eGFR 25 and K+ 5.8. Would Spironolactone be appropriate for HFrEF? 
First, identify the indication. Then, check for contraindications.
```

## Self-Consistency Verification
Generate multiple approaches and compare them:

**Pattern:**
```
Approach 1: [Ask for solution method A]
Approach 2: [Ask for solution method B]
Compare: Where do these approaches agree or disagree?
```

## Verification Prompts
**Always ask the model to check its own work:**
```
Check your response above. 
- What assumptions did you make?
- What could be wrong with this reasoning?
- Are there alternative explanations?
```

---

### Part B: Understanding AI Errors and Hallucinations

## The Two Types of AI Errors:
1. **Factual Hallucination:** Making up a lab value or a citation. (Rare in 2026 models).
2. **Logical Hallucination:** Having the right data but reaching a dangerous conclusion. (Common in 2026 models).

---

### Part C: Chain-of-Verification (CoVe) Pattern
Use this prompt pattern when accuracy is non-negotiable (e.g., patient education materials or research summaries):

**Prompt 1:** "Based on this PDF, summarize the key findings."
**Prompt 2:** "Now, extract every specific claim you just made into a list."
**Prompt 3:** "For each claim, find the specific sentence in the original PDF that supports it. If you cannot find a direct quote, mark it as 'unverified'."
**Prompt 4:** "Provide a final summary using only the 'verified' claims."

---

### Part D: Red Team Auditing & Adversarial Testing

## 🛡️ Adversarial Thinking: The "Red Team" Mindset
In 2026, AI models are so good at sounding human that we often lower our guard. **Adversarial Thinking** means assuming the AI is "hallucinating logic" until you prove otherwise.

## 🕵️ Seminar Activity: The Expanded "Red Team" Challenge
**The Setup:** You are a Clinical Auditor. You have been handed an AI-generated summary of a complex patient case.
**The Goal:** Use a 3-step pipeline to find the logical "hallucination" that a standard read-through would miss.
Don't ask if the summary is "good." Ask the AI to list its facts.
> **Prompt:** "Read the provided summary. List every discrete clinical assertion made regarding medication dosages, diagnostic conclusions, and follow-up timelines. Format as a bulleted list."

### Step 2: The "Evidence" Anchor
Force the AI to prove its work using the source document.
> **Prompt:** "For every assertion listed in Step 1, find the exact sentence or lab value in the original patient record that supports it. If no direct evidence exists, label it 'INFERRED'."

### Step 3: The "Adversarial" Cross-Examination
This is the true Red Team moment. Force the AI to act as its own critic.
> **Prompt:** "Now, act as a Chief Medical Officer reviewing this plan. Identify one reason why the suggested treatment might be contraindicated based on the patient's comorbidities. Be highly critical. Do not defer to the previous summary's authority."

---

## 🧪 Case Study for the Lab: The Overconfident Resident
**Input Text (Paste this into the AI):**
> "Patient: 72yo Female. Hx: Heart Failure (HFrEF), CKD Stage 3, Hypertension. 
> Labs: Potassium 5.6 mEq/L (High), Creatinine 1.9. 
> AI Plan: Patient's BP is still 150/90. Suggest starting Spironolactone 25mg daily to improve mortality outcomes and manage blood pressure."

**The Hidden Error:** Spironolactone is life-saving in HFrEF, but it is often contraindicated or requires extreme caution when Potassium is already >5.0 and the patient has CKD. A "lazy" AI will focus on the HFrEF benefit and ignore the hyperkalemia risk.

**Exercise:** Run the 3-step pipeline. Does the AI catch the Potassium risk in Step 3?

---

## ⚖️ Ethics & Privacy Checklist
- [ ] **PHI Check:** Am I using an institutional-grade tool (e.g., ai.case.edu)? 
- [ ] **Bias Check:** Did the AI assume a "standard" patient profile, or did it account for this specific patient's unique background?
- [ ] **Transparency Check:** Can I explain to a colleague *how* the AI reached this conclusion?

---

## 🏠 Take-Home Assignment: The "Logic Audit"
1.  **Find a guideline:** Upload a 2025/2026 clinical guideline (e.g., ADA, ACC) to your AI.
2.  **Generate a 'Lazy' Summary:** Ask the AI to summarize a complex case based on that guideline.
3.  **Perform the Audit:** Run the **3-Step Audit Pipeline** from today's lab.
4.  **Reflect:** Did the "Adversarial" prompt (Step 3) change the final recommendation? Write down what changed.

---

## 📅 Looking Ahead
**Next Week:** We build **Knowledge Agents**. You will learn how to "ground" an AI in a folder of your own PDFs using **NotebookLM**, creating a "Personal Brain" that doesn't hallucinate outside your provided sources.