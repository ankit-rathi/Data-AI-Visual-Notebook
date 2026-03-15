# Chapter 10 — Designing Decisions

---

# 1. Opening Observation

* Many predictive systems generate probabilities about future events.
* Fraud detection models estimate the likelihood that a transaction is fraudulent.
* Credit models estimate the probability of loan default.
* Recommendation systems estimate the likelihood that a user will engage with content.
* Yet these predictions alone do not determine what an organization should actually do.

---

# 2. Problem

* Predictive models output probabilities or scores rather than concrete actions.
* Organizations must still decide how to respond to those predictions.
* Different responses involve trade-offs between costs, risks, and benefits.
* Without structured decision rules, predictions remain informational rather than operational.
* The challenge becomes translating probabilistic forecasts into consistent actions.

---

# 3. Core Idea

* Decision rules convert probabilistic predictions into operational choices.
* These rules define how predictions map to actions under uncertainty.
* By specifying thresholds and trade-offs, organizations determine how predictive signals influence behavior.
* Decision design therefore bridges the gap between prediction systems and real-world actions.

---

# 4. System Model

```text id="m4x7x2"
prediction → threshold → decision
```

* **Prediction** provides an estimated probability or score for an event.
* A **threshold** defines the point at which the predicted probability triggers an action.
* The resulting **decision** determines how the organization responds to the predicted outcome.
* This mapping operationalizes predictive intelligence within decision processes.

---

# 5. Mechanism

* **Predictions vs decisions**

  * Predictions estimate outcomes; decisions determine actions taken in response.

* **Fundamentals of decision theory**

  * Decision-making frameworks evaluate alternatives under uncertainty.

* **Expected value and risk tradeoffs**

  * Decisions balance potential benefits against possible losses.

* **Decision thresholds**

  * Thresholds determine when predicted probabilities trigger particular actions.

* **Classification decisions**

  * Binary or categorical actions often arise from classification models.

* **Human vs algorithmic decision-making**

  * Decision authority may be automated, human-guided, or hybrid.

* **Costs of false positives and false negatives**

  * Different types of prediction errors carry different operational consequences.

---

# 6. Real-World Example — Fraud Detection Systems

* Payment platforms evaluate transactions using fraud detection models.
* Each transaction receives a predicted probability that it is fraudulent.
* Decision thresholds determine how the system responds to these probabilities.
* Transactions above a high threshold may be automatically blocked.
* Transactions within intermediate ranges may be flagged for manual review.
* Legitimate transactions below the threshold proceed without interruption.

---

# 7. Strategic Insight

* Predictive models generate potential intelligence, but decision rules convert that intelligence into action.
* Well-designed thresholds balance risk reduction with operational efficiency.
* Poorly designed decision rules can either allow harmful events or create excessive friction for users.
* Effective decision systems therefore require both accurate predictions and carefully designed decision policies.
* Once decisions are defined, organizations must embed them into real operational processes: **operational decision systems.**
