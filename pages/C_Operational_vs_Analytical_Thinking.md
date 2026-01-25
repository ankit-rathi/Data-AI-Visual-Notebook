# **C - Operational vs Analytical Thinking**

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/ce4d74a7-4956-4a19-94fd-64225d2685e5" />

> Systems generate **operational data** as they act in the world, recording each transaction needed to keep the business running, which is why this data is handled by **OLTP** systems optimized for fast, correct, low-latency updates. However, acting and understanding are different goals, so this constantly changing data is later stabilized into **analytical data**, which can be explored without interfering with operations. **OLAP** systems exist for this purpose, enabling large-scale comparison and pattern discovery across time. To ensure a unified and consistent memory of the organization, analytical data is centralized in a **data warehouse**, which integrates multiple operational sources into a single version of truth. Since different teams need different perspectives, focused subsets of this warehouse are exposed as **data marts**, trading completeness for relevance and speed. To make sense of large volumes, data is summarized through **aggregation**, producing **metrics** that quantify performance, while **dimensions** provide the context—such as time, geography, or product—that gives those numbers meaning. Together, these concepts exist to separate running the present from understanding the past so better decisions can shape the future.

> Operational Data, OLTP → Analytical Data → OLAP → Data Warehouse → Data Mart → Aggregation, Metric, Dimension

