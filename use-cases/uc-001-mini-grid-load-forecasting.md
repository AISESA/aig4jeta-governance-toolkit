# Use Case UC-001 – AI-based Load Forecasting for Rural Mini-Grids in East Africa

---

## 1. Basic Information

- **Use Case ID:** UC-001  
- **Title:** AI-based Load Forecasting for Rural Mini-Grids in East Africa  
- **Version:** 0.1 (Draft)  
- **Date Created:** 2025-12-03  
- **Last Updated:** 2025-12-03  
- **Author(s):** AISESA AI Working Group (Example Use Case)  

---

## 2. Context & Problem Statement

### 2.1. Background

A rural district in East Africa is served by a set of solar-diesel hybrid mini-grids operated by a local utility and community energy cooperative. Demand is growing due to productive uses of energy (e.g., milling, welding, cold storage) and new household connections. However, limited forecasting capacity leads to:

- Frequent battery depletion or diesel overuse,  
- Poor planning for new connections, and  
- Higher operating costs passed on to consumers.

The operator wants to use AI-based load forecasting to improve planning and operations while protecting affordability and reliability for low-income households.

### 2.2. Problem Being Addressed

- Lack of accurate, short-term (hourly/daily) and medium-term (weekly/monthly) demand forecasts.  
- Over- or under-sizing of generation and storage, leading to outages or unnecessary diesel use.  
- Difficulty planning tariff structures and expansion plans.

### 2.3. Affected Stakeholders

- Rural households (including women-led households).  
- Small and medium enterprises (SMEs) relying on electricity for income.  
- Local mini-grid operator and staff.  
- Local government and regulators.  
- Community leaders and energy access advocates.

---

## 3. AI Solution Description

### 3.1. AI Method / Approach

The solution uses:

- A time-series forecasting model (e.g., gradient boosted trees or LSTM) trained on historical load data.  
- Weather and calendar features (temperature, solar irradiance, day of week, market days, holidays).  
- Simple explainability tools (feature importance, partial dependence plots) to help operators understand drivers of demand.

### 3.2. Data Used

- **Data types:**
  - Historical hourly load from smart meters or feeder meters.  
  - Weather data (temperature, cloud cover, solar irradiance).  
  - Calendar and local events (market days, paydays, school terms).

- **Data sources:**
  - Utility mini-grid SCADA / meter data.  
  - National meteorological service or open weather APIs.  
  - Local government / community calendars.

- **Local relevance:**
  - Models are trained on **local mini-grid data** from the specific district (not only on foreign benchmarks).  
  - Data captures seasonal patterns such as rainy and dry seasons, agricultural cycles, and local festivities.

### 3.3. System Overview

1. Raw meter data is collected and cleaned daily.  
2. The AI model generates:
   - Short-term (next 24–72 hours) load forecasts for operational dispatch and diesel scheduling.  
   - Medium-term (next 3–12 months) forecasts for planning expansion and storage sizing.  
3. Outputs are visualized on a dashboard used by:
   - Mini-grid operators for day-to-day decisions.  
   - Planners for investment and tariff design scenarios.

---

## 4. TRUST Matrix Mapping

### 4.1. Transparency

- **Data Lineage:**  
  - Sources documented: “Mini-grid SCADA system; National Met Office API; Local event calendar.”  
  - Data cleaning and feature engineering steps documented in a technical note.

- **Explainability:**  
  - Feature importance is shared with operators (e.g., “market day” and “temperature” influence peaks).  
  - Plain-language explanations for non-technical stakeholders are included in training materials.

### 4.2. Risk & Reliability

- **Failure Impact:**  
  - Moderate: Poor forecasts may cause short-term outages or higher diesel usage, affecting reliability and tariffs.

- **Uptime Requirement:**  
  - The AI service itself does not require 99.9% uptime, but forecast unavailability for more than 24 hours triggers fallback to manual planning methods.

- **Mitigation:**  
  - Operators maintain conservative planning margins, and human review is required for major operational changes.

### 4.3. Understanding (Context)

- **Local Relevance:**  
  - Model trained on 18–24 months of local mini-grid data, capturing agricultural and seasonal patterns.  
  - Separate models or segments for residential, commercial, and productive users.

- **Stakeholder Buy-in:**  
  - Community workshops held to explain objectives and potential tariff/quality impacts.  
  - Local operators participated in model design and validation.

### 4.4. Safety & Security

- **Safety:**  
  - The system does not directly switch equipment; it provides recommendations reviewed by human operators.  
  - Critical safety interlocks (overload protection, emergency shutdowns) remain independent of the AI model.

- **Security:**  
  - Data and models hosted on a secure server with role-based access.  
  - Basic cybersecurity practices applied (strong passwords, HTTPS, regular backups).

### 4.5. Trustworthiness (Ethics)

- **Bias & Fairness:**  
  - Forecasting is at feeder/segment level, not targeting specific households; risk of individual discrimination is low.  
  - Monitoring ensures that connection or disconnection decisions are not automated based solely on forecast outputs.

- **Energy Justice:**  
  - Use case aims to **improve reliability** and **reduce costs**, especially by optimizing diesel usage.  
  - Equity analysis assesses whether improvements are shared across all customer classes, including the poorest households.

---

## 5. Governance & Oversight

### 5.1. Policies & Standards Applied

- National energy regulatory guidelines on mini-grid operations (where applicable).  
- Emerging AI and data protection policies (country-specific, to be referenced).  
- AISESA AI Ethics Principles v0.1 and TRUST Matrix v0.1.

### 5.2. Roles & Responsibilities

- **Mini-grid Operator:** Owns operational decisions; responsible for how AI forecasts are used.  
- **Technical Provider / Data Science Partner:** Responsible for model development, documentation, and updates.  
- **Regulator:** Ensures that tariff and service quality impacts remain within approved frameworks.  
- **Community Committee:** Provides feedback on service quality and equity impacts.

### 5.3. Monitoring & Evaluation

Key indicators:

- Forecast accuracy (e.g., MAPE, MAE).  
- Outage frequency and duration.  
- Diesel consumption per kWh delivered.  
- Number of new connections and affordability metrics.  
- Community satisfaction (survey-based).

---

## 6. Impacts & Outcomes

### 6.1. Positive Outcomes (Intended)

- Reduced diesel fuel use by 10–20% through better scheduling.  
- Fewer unplanned outages during peak periods.  
- Improved planning for new connections and capacity expansions.  
- More stable tariffs over time.

### 6.2. Risks & Unintended Consequences

- Over-reliance on AI forecasts could reduce operator skills or situational awareness.  
- Model drift (e.g., due to economic shocks or climate impacts) may degrade accuracy unnoticed.  
- If not managed carefully, improved reliability could first benefit commercial users, leaving households with less improvement.

### 6.3. Mitigation Measures

- Regular model retraining and performance audits (e.g., quarterly).  
- Operator training to interpret forecasts critically and override when needed.  
- Equity review of service improvements by customer type and income segment.

---

## 7. Community & Stakeholder Engagement

### 7.1. Engagement Process

- Initial consultations with community leaders and customer groups to explain the project.  
- Co-design sessions to understand local load patterns and priority services (e.g., clinics, schools, water pumps).  
- Regular community meetings to share performance results and collect feedback.

### 7.2. Feedback & Grievance Mechanisms

- Simple grievance channels via:
  - Local energy committee meetings.  
  - SMS/WhatsApp hotline managed by the operator.  
- Issues logged into an **action log** and reviewed in monthly operator-community coordination meetings.

---

## 8. Lessons Learned & Recommendations

- **Key lessons:**
  - Local context (market days, agricultural seasons) dramatically improves forecast quality.  
  - Human operators must remain central; training is as important as the model.  
  - Community transparency about how AI is used builds acceptance and reduces suspicion.

- **Recommendations for replication or scaling:**
  - Start with pilot mini-grids and scale gradually, validating in each new context.  
  - Standardize data collection and governance practices early (metering, privacy, security).  
  - Integrate AI forecasting into broader planning tools (e.g., least-cost electrification, tariff modeling).

---

## 9. References & Documentation

- [AISESA AIG4JETA Governance Toolkit – TRUST Matrix v0.1](../governance/trust-matrix-v0.1.md)  
- [AISESA AIG4JETA Governance Toolkit – AI Ethics Principles v0.1](../governance/ai-ethics-principles-v0.1.md)  
- [National mini-grid regulatory guidelines – *placeholder reference*]  
- [Internal technical design document – *to be added when available*]
