# 1-Click Co-Pilot — Hybrid Intelligence for Small Restaurants (SMEs)
**Turn messy daily data into one coherent, actionable strategy — in a single click.**

---

## Why this exists
Time is the #1 bottleneck for small businesses. Owners cook, serve, buy supplies, post content, handle delivery apps… there’s no time left for analysis.  
Yet every day they still need to:
- draft a **marketing plan**, identify **strengths/weaknesses**, plan **daily content**, and
- keep all of that **aligned with the long-term plan**.

**1-Click Co-Pilot** is a “hybrid intelligence” system that pairs *human business sense* with *Generative AI* to compress hours of work into minutes—without asking the owner to learn data tools.

---

## Design philosophy: Hybrid Intelligence
- **Human Analyst (you/owner):** set the business question, validate charts, add context only humans know, and approve insights.
- **Generative AI:** synthesize multi-source signals at scale into a structured, consistent plan.

> Let machines do what they’re great at (scale, synthesis), and let humans do what AI can’t (judgment, context, ethics).

---

## Repository structure (maps to the working folders)


---

## End-to-end workflow (4 phases)

### Phase 1 — Internal signal (Sales)
- Pull **daily sales & environment** from your data repo.
- Python pipelines **clean**, run **EDA**, and **forecast** with Linear Regression (recursive) and Prophet.
- Produce human-readable visualizations.

### Phase 2 — Internal signal (POS depth)
- Load **ticket-level POS** and run **Market Basket Analysis** to discover pairings and bundle ideas.
- **Human validation step:** charts & notes are reviewed and promoted to curated `sales_insight` / `gpos_insight`.

### Phase 3 — External context
- Bring in **Google Trends**, **customer reviews**, and the **long-term plan** from `00_nd_plan`.
- Align near-term tactics with brand and north-star objectives.

### Phase 4 — AI synthesis → one coherent plan
- A tight **Prompt Engineering** blueprint instructs the LLM to:
  1) act as a **professional marketer**,  
  2) use only the files we pass,  
  3) produce a **nine-part deliverable** owners actually need:
     - Weekly **Action Plan** (Who/What/When/Why/Impact)  
     - **Daily promo ideas** tied to Market Basket pairings  
     - **7-day content topics** aligned with current trends  
     - **Menu engineering** (hero items, bundles, price hints)  
     - **Positioning: strengths & pain points**  
     - **CRM/voice-of-customer** highlights from reviews  
     - **Operational hints** (staffing windows / queue risks)  
     - **Risk & SWOT notes** with mitigations  
     - **KPIs** to track (conversion, wait time, NPS, redemption, etc.)

---

## Quickstart

### 1) Environment
- Python **3.10+**
- Create a virtual env and install deps:
```bash
python -m venv venv
source venv/bin/activate         # Windows: venv\Scripts\activate
pip install -r requirements.txt


