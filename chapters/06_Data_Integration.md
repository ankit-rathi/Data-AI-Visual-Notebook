# Chapter 6 — Data Integration

---

## Fragmented Observations Across Organizational Systems

* Modern organizations operate through many specialized systems built for specific operational tasks.
* Examples include:

  * sales systems recording transactions
  * marketing platforms tracking campaigns
  * operational systems monitoring logistics or manufacturing
  * support systems managing customer interactions
* Each system captures a **narrow slice of organizational activity**, optimized for operational efficiency rather than analytical completeness.
* As a result, data is scattered across multiple databases, applications, and services.
* These systems rarely share a unified structure, meaning the same entities may appear differently in different systems.
* Without integration, analysts and decision-makers see **fragmented observations rather than a coherent representation of the organization**.

---

## Connecting Partial Views into a Unified Dataset

* Data integration is the process of combining data from multiple sources into a unified and consistent dataset.
* The objective is not merely to collect data, but to **connect observations that originate in different systems**.
* Integration makes it possible to reconstruct processes that span multiple systems, such as:

  * the full customer lifecycle
  * supply chain operations
  * product usage and support interactions
* Achieving this requires:

  * aligning entity identifiers across systems
  * reconciling differences in data formats
  * consolidating multiple event streams into a shared structure
* Once integrated, datasets begin to reflect the organization as **an interconnected system of activities rather than isolated operational silos**.

---

## The Data Pipeline: Moving and Transforming Information

* Integration is typically implemented through **data pipelines** that move data from operational systems into analytical environments.

* These pipelines generally involve three core stages:

  * **Extraction** – retrieving data from source systems such as databases, APIs, or event streams.
  * **Transformation** – cleaning, standardizing, and reshaping data into a consistent format.
  * **Loading** – storing the transformed data in a central repository such as a data warehouse or data lake.

* Pipelines may operate in different modes depending on requirements:

  * **Batch processing** for periodic updates
  * **Streaming pipelines** for near real-time data movement

* Reliable pipelines ensure that integrated datasets remain **continuously updated as new events occur**.

---

## Maintaining Consistency Across Evolving Systems

* Integration is not a one-time task but an ongoing process that must adapt as systems evolve.
* Operational systems frequently change:

  * schemas evolve
  * new attributes are added
  * systems are replaced or upgraded
* Integration pipelines must handle these changes without breaking downstream datasets.
* This requires:

  * schema management and version control
  * monitoring pipelines for failures or inconsistencies
  * maintaining documentation of data transformations
* Sustained integration efforts ensure that unified datasets remain **reliable representations of organizational activity over time**.

---

## Revealing System-Level Relationships Through Integration

* Once datasets from different systems are combined, previously hidden relationships become visible.
* Analysts can connect events across domains, enabling insights such as:

  * linking marketing campaigns to sales outcomes
  * connecting product usage patterns with customer churn
  * tracing operational delays back to upstream causes
* Integrated datasets allow organizations to move from **isolated metrics to system-level analysis**.
* This shift transforms data from a collection of operational records into a **comprehensive view of organizational behavior**.

---

## Diagram — Conceptual Illustration

```
Sales System      Marketing System      Operations System
      │                    │                    │
      │                    │                    │
      └──────────┬─────────┴─────────┬──────────┘
                 │                   │
            Data Extraction
                 │
                 ↓
           Data Transformation
      (Standardization & Linking)
                 │
                 ↓
           Unified Dataset
                 │
                 ↓
        Organization-Wide View
```

### Explanation

The diagram illustrates how **data integration connects multiple operational systems into a unified dataset**.

* Independent systems each produce their own datasets.
* Data pipelines extract information from these systems.
* Transformation processes standardize formats and connect related entities.
* The integrated result becomes a **unified dataset** that reflects the organization’s activities across systems.

This unified dataset allows analysts and decision systems to observe relationships that were previously hidden within isolated systems.

---

### Guidance for Drawing in PowerPoint

Layout:

* Use a **top-to-bottom flow** with multiple systems feeding into a pipeline.

Shapes:

* Rectangles for source systems:

  * Sales System
  * Marketing System
  * Operations System
* A rectangle labeled **Data Extraction** below them.
* A rectangle labeled **Data Transformation** beneath extraction.
* A rectangle labeled **Unified Dataset** at the bottom.
* Final rectangle labeled **Organization-Wide View**.

Arrows:

* Arrows from each source system pointing toward the extraction stage.
* Downward arrows connecting each stage of the pipeline.

Design suggestions:

* Place the source systems horizontally at the top.
* Use a consistent color for pipeline stages.
* Keep the layout symmetrical and uncluttered.

---

## Example — Integrating Customer Data Across Systems

Consider how an online retailer integrates customer data from multiple systems.

Three independent systems produce relevant data:

* **E-commerce platform**

  * records purchases and orders

* **Marketing automation system**

  * tracks email campaigns and website visits

* **Customer support platform**

  * logs service requests and complaints

Mapping this example to the diagram:

1. **Source Systems**

   * The sales platform records purchase events.
   * The marketing system tracks campaign engagement.
   * The support system records customer tickets.

2. **Data Extraction**

   * Data pipelines retrieve records from each system’s database or API.

3. **Data Transformation**

   * Customer identifiers are standardized across systems.
   * Data formats and timestamps are normalized.
   * Events are linked to the same customer entity.

4. **Unified Dataset**

   * All customer-related events are combined into a central data platform.

5. **Organization-Wide View**

   * Analysts can now observe the full customer lifecycle:

     * marketing exposure
     * purchasing behavior
     * support interactions

Without integration, each system would provide only a partial view of customer activity.

---

## Seeing the Organization as an Interconnected System

* Organizations generate data across many independent systems, each capturing a limited perspective.
* Data integration connects these partial observations into unified datasets that reveal relationships across processes.
* Through pipelines that extract, transform, and load data, fragmented records become part of a coherent analytical environment.
* When integration is successful, the organization becomes observable as a **connected system of events, entities, and processes**.

**Transition to the Next Chapter**

Once data from multiple sources has been integrated, organizations can begin examining it for patterns, relationships, and signals. At this stage, the focus shifts from managing data to interpreting it. The next chapter introduces analytical thinking—the process of transforming data into meaningful insights.

---

## References

* Kleppmann, Martin. *Designing Data-Intensive Applications.* O’Reilly Media, 2017.

* Kimball, Ralph & Ross, Margy. *The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling.* Wiley, 2013.

* Inmon, William H. *Building the Data Warehouse.* Wiley, 2005.

* Hellerstein, Joseph, Stonebraker, Michael, & Hamilton, James. “Architecture of a Database System.” *Foundations and Trends in Databases*, 2007.

* Vassiliadis, Panos. “A Survey of Extract–Transform–Load Technology.” *International Journal of Data Warehousing and Mining*, 2009.

* Zaharia, Matei et al. “Apache Spark: A Unified Engine for Big Data Processing.” *Communications of the ACM*, 2016.
