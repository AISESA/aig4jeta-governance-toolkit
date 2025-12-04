# TRUST Matrix: AI Risk Assessment Framework for Energy
**Version:** 0.1 (Draft)
**Scope:** Evaluation of AI models used in Grid Management & Energy Distribution.

---

## 1. T - Transparency
* **Data Lineage:** Is the training data source clearly documented?
    * [ ] Yes (Source: __________)
    * [ ] No
* **Explainability:** Can the model's decision-making process be interpreted by non-technical stakeholders?
    * [ ] High (Rule-based / Linear)
    * [ ] Medium (Feature importance available)
    * [ ] Low (Black box neural net)

## 2. R - Risk & Reliability
* **Failure Impact:** What is the worst-case scenario if the model fails?
    * [ ] Minor (Data logging error)
    * [ ] Moderate (Temporary local outage)
    * [ ] Critical (Grid instability / Safety hazard)
* **Uptime Requirement:** 99.9% availability required? [ ] Yes / [ ] No

## 3. U - Understanding (Context)
* **Local Relevance:** Was the model trained on data relevant to the specific African region of deployment?
    * [ ] Yes, local data used
    * [ ] No, pre-trained on global/western datasets only
* **Stakeholder Buy-in:** Have local community leaders been consulted? [ ] Yes / [ ] No

## 4. S - Safety & Security
* **Adversarial Robustness:** Has the model been tested against cyber-attacks (e.g., data poisoning)?
    * [ ] Tested & Verified
    * [ ] Testing in progress
    * [ ] Not tested
* **Human-in-the-Loop:** Is there a human operator required to approve high-stakes decisions? [ ] Yes / [ ] No

## 5. T - Trustworthiness (Ethics)
* **Bias Auditing:** Has the model been checked for bias against specific demographics or regions?
    * [ ] Audit passed
    * [ ] Audit pending
    * [ ] Not applicable
* **Energy Justice:** Does this deployment support equitable energy access? [ ] Yes / [ ] No

---
*Reference: Adapted for AISESA Just Energy Transition Initiative*
