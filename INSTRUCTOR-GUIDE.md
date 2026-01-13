# Week 4: Verification & Clinical Ethics
## Instructor Notes (2026 Updated)

---

### Slide 1: Welcome & The "Trust but Verify" Era
**Title:** Moving from "Chatting" to "Clinical Auditing"
**Context:** In 2026, AI is more persuasive than ever. Our job is no longer just finding information; it is verifying it.

**Speaker Notes:**
- Review Week 3 homework: Did anyone find a reasoning model (GPT-5/Claude 4) that was overconfident?
- Key Theme: Just because a model shows its "Thinking Process" doesn't mean that process is correct.

---

### Slide 2: The New Hallucination: "Logical Errors"
**Concept:** In 2024, AI made up facts. In 2026, it often makes up **logic**.
- **Definition:** A logical hallucination is a diagnostic or treatment path that uses real data but reaches a medically unsound conclusion.
- **Example:** Correctly identifying a lab value but recommending a dosage that violates standard safety protocols.

---

### Slide 3: Advanced Technique: Chain-of-Verification (CoVe)
**Instructor Action:** Show a prompt that uses the "Independent Verification" pattern.
- **Step 1:** The model creates a draft.
- **Step 2:** The model identifies its own factual claims.
- **Step 3:** The model verifies each claim *without* looking at the initial draft (to prevent "confirmation bias").
- **Step 4:** The model finalizes the answer.

---

### Slide 4: Ethics & Bias in 2026
**Discussion Point:** Training data still reflects historical imbalances.
- **Case Study:** A risk-prediction algorithm that favors certain demographics based on historical spending rather than clinical need.
- **Instructor Note:** Emphasize that AI should be a "second opinion," not the "primary source."

---

### Slide 5: Privacy & "Shadow AI"
**Concept:** The danger of institutional non-compliance.
- **Definition:** "Shadow AI" refers to using unapproved consumer AI tools for protected health information (PHI).
- **Rule:** If the tool isn't in the "Institutional Safe Zone," never paste patient-identifiable data into it.

---

### Slide 5a: The "Red Team" Lab: From Search to Audit (30 Mins)
**Instructor Action:** Introduce the concept of **Adversarial Auditing**. We aren't just reading the AI's answer; we are trying to break its logic.

**The "Audit Pipeline" Steps:**
1.  **Extraction:** Identify every medical "assertion" the AI made (dosages, diagnoses, timelines).
2.  **Verification:** Force the AI to provide a direct quote from the source for *each* assertion.
3.  **Contradiction Search:** Specifically ask the AI to find reasons why its own suggestion might be wrong (Red Teaming).
---

### Slide 6: Live Demo: The Metformin Trap
**Scenario:** A patient with Stage 4 CKD (eGFR 25) is recommended for a Metformin increase.
- **Phase 1 (The Fail):** Ask a standard model to "Summarize the plan." It will likely repeat the dangerous dosage.
- **Phase 2 (The Audit):** Use the CoVe pattern. Watch the "Thinking" block as the model realizes the contraindication during the "Extraction" phase.
- **Key Takeaway:** The "Thought Process" is where the safety happens, not the final text.

---

### Slide 7: Wrap Up & Fun Homework
- Review the "Personal AI Stack" concept.
- **Looking Ahead:** Week 5 focuses on Knowledge Agents (NotebookLM).