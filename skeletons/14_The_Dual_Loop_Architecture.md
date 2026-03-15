# Chapter 14 — Learning and Execution Systems

---

# 1. Opening Observation

* Many intelligent digital systems operate through two distinct environments.
* Machine learning models are trained using large historical datasets in analytical environments.
* The resulting models are then deployed into live products that interact with users in real time.
* Product systems apply predictions instantly, while learning processes occur separately in the background.
* This separation enables systems to continuously improve while maintaining reliable operational performance.

---

# 2. Problem

* Training machine learning models requires large datasets, experimentation, and heavy computation.
* Operational systems, however, must respond quickly to user interactions and events.
* Combining these two activities within the same environment can slow down products and introduce instability.
* Organizations therefore need architectures that allow models to improve without disrupting operational workflows.
* The challenge becomes coordinating learning processes with real-time decision execution.

---

# 3. Core Idea

* Intelligent systems separate **learning systems** from **execution systems**.
* Learning systems analyze historical data to improve models and decision logic.
* Execution systems apply those models within operational products to make real-time decisions.
* This architecture allows organizations to continuously refine intelligence while maintaining reliable system behavior.

---

# 4. System Model

```text id="zzlhg7"
offline learning system ↔ online execution system
```

* The **offline learning system** processes historical data to train and update models.
* The **online execution system** applies trained models to real-time events.
* Updates flow from the learning system to the execution system through deployment processes.
* Feedback from operational outcomes returns to the learning system for further improvement.

---

# 5. Mechanism

* **Separation of training and inference**

  * Training occurs offline using historical datasets, while inference generates predictions during live interactions.

* **Offline learning pipelines**

  * Data preparation, feature generation, and model training workflows operate in analytical environments.

* **Online execution systems**

  * Operational services integrate trained models into user-facing applications.

* **Model updates and deployments**

  * Newly trained models are versioned and deployed into production systems.

* **Batch vs real-time intelligence**

  * Some intelligence updates periodically, while other decisions require immediate predictions.

* **Continuous model improvement**

  * Feedback data from operational systems supports ongoing model refinement.

* **System architecture for intelligent products**

  * Infrastructure coordinates data pipelines, model training, and deployment processes.

---

# 6. Real-World Example — Online Advertising Bidding Systems

* Advertising platforms train models that estimate the probability that a user will click on or convert from an advertisement.
* Historical ad impressions, user behavior, and campaign results are processed in offline learning pipelines.
* These pipelines train predictive models that estimate engagement probabilities.
* The trained models are deployed into real-time bidding systems that evaluate ad opportunities as they occur.
* When a user loads a webpage or app, the execution system uses the model to determine which advertisement to display and how much to bid.
* Performance data from these impressions feeds back into future training cycles.

---

# 7. Strategic Insight

* Separating learning from execution allows organizations to scale intelligent systems effectively.
* Learning systems focus on improving models, while execution systems focus on delivering real-time decisions.
* This architectural separation enables continuous intelligence improvement without disrupting operational performance.
* However, improving decision systems requires more than passive feedback from outcomes.
* Organizations must also actively test alternative strategies through structured experimentation: **experimentation systems.**
