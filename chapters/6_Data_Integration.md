## Chapter 6 — Data Integration

### Chapter Crux

Organizations generate data across many independent systems—applications, databases, logs, sensors, and third-party platforms. Each system captures only a **partial view of reality**. Data integration exists to combine these fragmented observations into coherent datasets that can support analysis and decision-making.

Without integration, data remains scattered across operational silos. Customer information might live in one system, transactions in another, and behavioral logs in a third. Decision-makers cannot easily reconstruct the full picture of what is happening in the business.

Data integration solves this by building **pipelines that move, transform, and unify data across systems**. These pipelines ensure that data from multiple sources can be combined into consistent, analyzable structures. Integration also manages how data evolves over time through schema changes and coordination between producing and consuming systems.

In essence, data integration transforms isolated data sources into a **shared foundation for organizational intelligence**.

---

### Problem

Modern organizations operate dozens or even hundreds of systems that generate data independently.

Examples include:

* operational transaction systems
* mobile and web applications
* customer relationship platforms
* marketing tools
* payment systems
* infrastructure logs

Each system records data in its own format, schema, and timing. This creates several challenges:

* inconsistent definitions across systems
* duplicate or conflicting records
* incompatible schemas
* delayed or incomplete data availability

For example, a company may store customer profiles in one system, purchase transactions in another, and marketing interactions in a third. Without integration, it becomes difficult to answer basic questions such as:

* Which customers are most valuable?
* Which marketing campaigns drive purchases?
* How does behavior change across channels?

The core problem is **data fragmentation**. Individual datasets capture partial truths, but organizations need a unified view.

---

### Key Diagram

**Data Integration Pipeline**

```id="9cb9g5"
Multiple Data Sources
   ↓
Data Pipelines
   ↓
Transformation & Standardization
   ↓
Unified Data Platform
   ↓
Analytics & Intelligence
```

Explanation:

* **Data sources:** operational systems producing raw data
* **Pipelines:** processes that move data between systems
* **Transformation:** cleaning, structuring, and standardizing data
* **Unified platform:** centralized datasets ready for analysis

Integration connects distributed observations into a coherent data foundation.

---

### Core Mechanism

Data integration relies on several core architectural mechanisms.

**1. Data Pipelines**

Data pipelines move data from source systems into analytical environments such as data warehouses or data lakes.

Pipelines typically perform tasks such as:

* extracting data from operational systems
* transforming data into standardized formats
* loading it into centralized storage

This process enables organizations to analyze data across multiple systems.

---

**2. ETL vs ELT**

Two common integration patterns are:

* **ETL (Extract → Transform → Load):**
  Data is transformed before entering the storage system.

* **ELT (Extract → Load → Transform):**
  Data is first loaded into a centralized platform and then transformed there.

Modern cloud data platforms often favor ELT because it allows more flexible and scalable transformations.

---

**3. Batch vs Streaming**

Data pipelines can operate in different modes:

* **Batch processing:** data is processed periodically in large groups (e.g., hourly or daily).
* **Streaming:** data is processed continuously as events occur.

Batch pipelines support large-scale analytics, while streaming systems enable real-time decision-making.

---

**4. Data Contracts and Schema Evolution**

As systems evolve, the structure of data often changes.

Data contracts define **clear agreements between data producers and consumers** about schema structure and expected fields. These agreements help prevent downstream systems from breaking when schemas change.

Managing schema evolution ensures that integration pipelines remain stable even as source systems evolve.

---

### Example

Consider a retail company that operates multiple systems:

* an e-commerce platform recording online purchases
* a point-of-sale system capturing in-store transactions
* a marketing platform tracking email campaigns
* a customer support system recording service interactions

Each system generates its own dataset.

Data integration pipelines extract data from these systems and load it into a centralized warehouse. During transformation, customer identifiers are standardized so that records from different systems can be linked.

Once integrated, the company can analyze questions such as:

* how marketing campaigns influence purchases
* how support interactions affect customer retention
* how online and offline behavior relate

Integration allows the organization to view the **full customer journey** rather than isolated events.

---

### Insight

Organizations rarely suffer from a lack of data—they suffer from **fragmented data**.

Each system captures a small piece of reality, but decisions require a **holistic view across systems**.

Data integration bridges this gap by connecting independent observations into unified datasets that can support analytics, machine learning, and decision systems.

In other words:

> Data becomes valuable not when it is captured, but when it can be **connected and understood across the entire organization**.
