## **E. Data Models (Relational / Document / Graph)**

**Why:** The model dictates which patterns can be discovered efficiently.

**What:**

* Relational: **enforces structure and constraints**.
* Document: **allows flexibility and schema evolution**.
* Graph: **emphasizes relationships and network effects**.

**How:** Pick a model based on priority: integrity, adaptability, or relational analysis.

---

From first principles, a data model is not just a storage choice — it is a constraint system. It defines what relationships are easy to represent, what questions are easy to ask, and what patterns are easy to detect. Every model amplifies certain signals and suppresses others. Therefore, the model you choose shapes the insights you can efficiently discover.

A **relational model** organizes data into tables with predefined schemas and explicit relationships via foreign keys. Its strength is structural integrity. Constraints enforce consistency: a transaction cannot reference a non-existent customer; data types must align; duplication can be controlled. This makes relational systems ideal where correctness, auditability, and transactional precision matter — for example, banking ledgers or inventory systems. If your priority is integrity and controlled structure, relational modeling dominates.

A **document model** stores data as flexible, self-contained records (often JSON-like). Each document can evolve without rigid schema constraints. This supports adaptability. For example, a user profile may include varying fields — preferences, social links, activity history — which can change over time. In fast-evolving product environments, rigid schemas slow iteration. Document models allow rapid experimentation and schema evolution, trading some structural enforcement for flexibility.

A **graph model** centers on relationships as first-class citizens. Entities (nodes) connect through edges that represent interactions. This makes network effects computationally natural. For example, in fraud detection, suspicious activity often emerges not from individual attributes but from relationship patterns — shared devices, overlapping addresses, transaction loops. In recommendation systems, “users who bought X also bought Y” is fundamentally relational. Graph models make multi-hop relationship queries efficient and intuitive.

The key principle: models optimize for different constraints. Relational models optimize consistency and transactional reliability. Document models optimize adaptability and rapid iteration. Graph models optimize relational depth and network analysis.

Choosing a model is choosing a lens. If you prioritize integrity, enforce structure. If you prioritize evolution, allow flexibility. If you prioritize relationship discovery, center the graph.

Misalignment between model and problem creates friction: relational systems struggle with deep network queries; document systems can drift into inconsistency; graph systems may complicate simple transactional workflows.

Effective system design begins by clarifying which patterns matter most — then selecting the model that makes those patterns computationally natural rather than forced.
