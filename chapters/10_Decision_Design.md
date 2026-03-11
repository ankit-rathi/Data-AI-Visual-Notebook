# Chapter 10 — Decision Design

---

## When Predictions Must Become Choices

* Predictive models estimate the likelihood of future outcomes, but predictions alone do not change what happens in the real world.
* Organizations create value only when predictions influence **decisions and actions**.
* Without clear decision mechanisms, predictive insights often remain unused or inconsistently interpreted by different individuals.
* For example:

  * a churn prediction only matters if it triggers a retention intervention
  * a fraud probability only matters if it affects transaction approval
* The critical challenge is determining **how predictive insights should translate into operational choices**.
* Decision design addresses this challenge by defining structured rules that connect predictions to actions.

---

## Defining Decisions Within Organizational Systems

* Decision design begins by identifying the **specific decisions that occur within a process**.
* These decisions often appear at key points where the organization must choose between alternatives.
* Examples include:

  * approving or rejecting a loan application
  * targeting or excluding a customer from a promotion
  * flagging or allowing a financial transaction
* Each decision involves:

  * a **set of possible actions**
  * available **information or predictions**
  * potential **outcomes associated with each action**
* Clarifying these elements ensures that predictive insights are tied to **explicit decision points rather than vague interpretation**.

---

## Evaluating Alternatives Through Decision Theory

* Decision theory provides a framework for choosing between possible actions under uncertainty.
* Instead of selecting actions intuitively, decision theory evaluates alternatives using:

  * predicted probabilities of outcomes
  * expected costs and benefits
  * potential risks or trade-offs
* This approach allows organizations to compare actions in terms of **expected value**.
* For example:

  * approving a loan with moderate default risk may still be profitable if interest revenue exceeds expected losses.
* Structured evaluation ensures that decisions are guided by **quantitative reasoning rather than subjective interpretation**.

---

## Translating Predictions into Decision Rules

* To operationalize decisions, organizations often define **decision rules** that connect predictions to actions.
* These rules typically rely on thresholds that determine when a particular action should occur.
* For example:

  * reject a loan if predicted default probability exceeds a defined limit
  * trigger a customer retention campaign if churn probability exceeds a threshold
  * flag transactions for review if fraud risk crosses a risk score threshold
* Decision rules create **consistency and repeatability**, ensuring that predictive insights are applied systematically.
* Well-designed rules prevent situations where the same prediction leads to different actions depending on who interprets it.

---

## Balancing Human Judgment and Automated Decisions

* Not all decisions can or should be fully automated.

* Some decisions require contextual understanding, ethical considerations, or complex judgment.

* Organizations often combine automation with human oversight through different decision structures:

  * **Fully automated decisions**

    * systems apply rules and execute actions immediately

  * **human-in-the-loop decisions**

    * systems provide recommendations while humans make final choices

  * **human-only decisions supported by analytics**

    * predictions inform but do not directly trigger actions

* Selecting the appropriate level of automation ensures that decision systems remain **both efficient and responsible**.

---

## Diagram — Conceptual Illustration

```
Prediction
(Estimated Probability)
        ↓
Decision Rule
(Threshold / Evaluation)
        ↓
Selected Action
        ↓
Operational Execution
        ↓
Real-World Outcome
```

### Explanation

The diagram illustrates how predictive intelligence becomes operational action through decision design.

* A **prediction** provides an estimate of the likelihood of an outcome.
* A **decision rule** evaluates the prediction using thresholds or expected value calculations.
* Based on this evaluation, the system selects an **action**.
* The action is executed operationally, producing a **real-world outcome**.

The diagram highlights that predictions only influence reality when they pass through a **structured decision mechanism**.

---

### Guidance for Drawing in PowerPoint

Layout:

* Use a **vertical flow diagram** showing the transition from prediction to outcome.

Shapes:

* Rectangles for each stage:

  * Prediction
  * Decision Rule
  * Selected Action
  * Operational Execution
  * Real-World Outcome

Arrows:

* Downward arrows connecting each stage.

Design suggestions:

* Highlight **Decision Rule** slightly to emphasize its role as the bridge between intelligence and action.
* Keep shapes evenly spaced.
* Use concise labels within each box.

---

## Example Section — Automated Fraud Detection in Digital Payments

Consider how a digital payment platform uses predictive intelligence to detect fraudulent transactions.

Mapping this scenario to the diagram:

1. **Prediction**

   * A machine learning model analyzes each transaction and estimates the **probability of fraud**.

2. **Decision Rule**

   * The platform defines risk thresholds:

     * low risk → allow transaction
     * medium risk → require additional authentication
     * high risk → block transaction

3. **Selected Action**

   * Based on the predicted fraud probability, the system chooses one of these actions.

4. **Operational Execution**

   * The payment platform automatically enforces the chosen response in real time.

5. **Real-World Outcome**

   * Fraudulent transactions may be prevented while legitimate transactions continue smoothly.

Through this process, predictive intelligence becomes operational value by guiding **consistent decision-making within the payment system**.

---

## Final Section — Designing Decisions That Turn Intelligence into Action

* Predictive intelligence provides estimates about future outcomes, but predictions alone do not create impact.
* Decision design connects predictive insights to operational choices through structured evaluation and rules.
* By defining decision points, comparing alternatives, and establishing thresholds, organizations ensure that predictions consistently influence actions.
* Effective decision design therefore transforms predictive models into **practical decision systems that shape real-world outcomes**.

**Transition to the Next Chapter**

Designing decisions clarifies what choices must be made and how intelligence can support them. However, these decision processes must ultimately operate within real systems that execute actions. The next chapter examines operational decision systems that embed intelligence directly into business operations.

---

## References

* Howard, Ronald A., & Abbas, Ali E. *Foundations of Decision Analysis.* Pearson, 2015.

* Keeney, Ralph L., & Raiffa, Howard. *Decisions with Multiple Objectives: Preferences and Value Trade-Offs.* Cambridge University Press, 1993.

* Hastie, Trevor, Tibshirani, Robert, & Friedman, Jerome. *The Elements of Statistical Learning.* Springer, 2009.

* Provost, Foster, & Fawcett, Tom. *Data Science for Business.* O’Reilly Media, 2013.

* Pearl, Judea. *Causality: Models, Reasoning, and Inference.* Cambridge University Press, 2009.

* Shmueli, Galit & Koppius, Otto. “Predictive Analytics in Information Systems Research.” *MIS Quarterly*, 2011.
