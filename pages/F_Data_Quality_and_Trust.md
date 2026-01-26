# **F - Data Quality and Trust**

<img width="800" height="533" alt="image" src="https://github.com/user-attachments/assets/2d1221a0-5d93-4572-9c25-39047e0a3238" />

> From first principles, these concepts exist because data is useful only when it can be **trusted to reflect reality at the right time**. **Data quality** is the result we care about, and it comes from a few basic properties. **Completeness** means nothing important is missing. **Accuracy** means the data matches what actually happened. **Freshness** reminds us that even correct data becomes less valuable if it arrives too late. Because real systems are messy, these properties cannot be taken for granted, so we use **validation** to continuously check rules, ranges, structure, and timing. When data breaks these expectations, an **anomaly** appears—an early warning that reality and data are drifting apart. To catch such problems reliably, systems rely on **monitoring**, which watches how data behaves over time rather than looking at a single snapshot. When monitoring shows a serious loss of trust—due to missing, wrong, or stale data—it becomes a **data incident**, forcing teams to investigate, fix the problem, and restore confidence in the data.

> Data Quality → Completeness, Accuracy, Freshness → Validation → Anomaly, Monitoring → Data Incident
