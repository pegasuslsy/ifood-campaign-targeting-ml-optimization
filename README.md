# ifood-campaign-targeting-ml-optimization

An end-to-end **predictive + prescriptive** analytics project for iFood marketing campaigns: **predict who will respond** and **optimize who to contact** under budget and business constraints.

---

## Overview

Marketing teams rarely have the budget to contact everyone. The practical question is not only **“who is likely to respond?”** but also **“who should we contact to maximize expected responses under constraints?”**

This project implements a two-stage pipeline:

1. **Predict**: train a classification model to estimate each customer’s **response probability**
2. **Prescribe**: select the best subset of customers using **integer optimization (Gurobi)** with optional business constraints (e.g., fatigue control, segment quotas)

---

## Key Features

- ✅ End-to-end workflow: **EDA → modeling → optimization**
- ✅ Handles class imbalance with **SMOTE**
- ✅ Compares multiple models: **Logistic Regression / Random Forest / XGBoost**
- ✅ Produces an **actionable contact list** (not just probabilities)
- ✅ Optimization layer supports extensible constraints:
  - Contact budget / top-K limit
  - Marketing fatigue controls
  - Segment quota / fairness constraints
  - Blacklist / whitelist rules
