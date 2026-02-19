# Consistency and Consensus

*Many nodes. One truth.*

---

## RIGHT PAGE — Article (~370 words)

Distributed systems are built from unreliable components. Machines crash. Networks delay. Messages reorder. Yet some systems provide a powerful illusion: that there is only one copy of the data and every operation happens atomically. That illusion is called **linearizability**.

Linearizability guarantees recency. Once a write completes, every subsequent read must see it. The system behaves like a single-threaded variable. This is stronger than serializability, which is about transaction isolation across multiple objects. Linearizability concerns the freshness of individual objects.

The cost is unavoidable. To ensure a value is the latest, nodes must coordinate. Response time becomes proportional to network uncertainty. Strong consistency is slow because doubt must be eliminated.

Ordering lies at the center of this problem. Physical clocks drift, so distributed systems rely on logical clocks. Lamport timestamps preserve causal order: if event A happened before B, A gets a lower timestamp. But causality is weaker than linearizability. Two nodes can generate timestamps without knowing which write is truly the latest globally. Hybrid logical clocks combine physical time with logical counters to approximate real-time ordering while preserving causality.

To implement true fault-tolerant linearizability, systems use **consensus**. Consensus means multiple nodes agree on a single sequence of decisions. If they agree on the order of operations, the system behaves as if one machine executed them.

Algorithms such as Raft and Paxos rely on epochs and quorums. A majority must confirm each decision. This prevents split brain: two leaders accepting conflicting writes. Coordination services like Apache ZooKeeper and etcd package these guarantees into reusable infrastructure for locks, leases, and configuration management.

Many problems reduce to consensus: shared logs, uniqueness constraints, compare-and-set operations, distributed locks, atomic commit. Solve one, and you can transform the solution to others.

However, consensus trades availability for consistency during network partitions. Under the CAP trade-off, systems may choose to reject requests rather than risk stale data.

Consensus is powerful but expensive. It is justified when correctness demands a single authoritative order. Otherwise, weaker consistency may be the wiser design choice.

---

## LEFT PAGE — Visual Note (Hand-Drawable)

**Consistency & Consensus**
*Agreement under uncertainty.*

---

### 1️⃣ Linearizability

📏 Icon: Single straight line

* Appears as one copy — atomic illusion
* Recency guarantee — latest write visible
* Stronger freshness than isolation — per-object focus

---

### 2️⃣ Cost of Strong Consistency

🐢 Icon: Slow clock

* Must coordinate before replying — quorum round-trip
* Latency tied to network uncertainty — unavoidable delay
* Doubt eliminated before success — safety first

---

### 3️⃣ Ordering the World

🕰️ Icon: Clock with counter

* Physical clocks drift — unreliable global time
* Lamport clocks preserve causality — happened-before
* Causality ≠ linearizability — global freshness missing

---

### 4️⃣ Hybrid Logical Clocks

🔗 Icon: Linked clock gears

* Combine physical time + logical counter — best of both
* Approximate real-time ordering — bounded skew
* Used in modern distributed DBs — practical compromise

---

### 5️⃣ Consensus Core

🧑‍⚖️ Icon: Group vote

* Uniform agreement — no divergence
* Integrity — decide once
* Validity + termination — real proposal, eventual decision

---

### 6️⃣ Algorithms & Quorums

🏛️ Icon: Majority vote panel

* Raft / Paxos — leader-based replication
* Epoch numbers prevent split brain — single term leader
* Majority quorum confirms writes — overlap guarantee

---

### 7️⃣ Coordination Services

🗝️ Icon: Key and lock

* Apache ZooKeeper / etcd abstract consensus
* Provide locks, leases, config — higher-level tools
* Reuse instead of reimplement — reduce risk

---

### 8️⃣ CAP Trade-off

⚡ Icon: Broken network line

* Partition forces choice — consistency or availability
* CP returns error to protect truth — safe pause
* AP serves stale but live data — availability first

---

## YOUTUBE SHORTS (~60 seconds)

Distributed systems are unreliable by nature. Machines fail. Networks delay. Yet some systems behave as if there is only one copy of the data.

That illusion is linearizability. Once a write succeeds, every later read must see it. The system behaves like a single-threaded variable.

But that illusion is expensive. Nodes must coordinate before replying. Latency reflects network uncertainty.

To make this fault-tolerant, systems use consensus. Algorithms like Raft and Paxos ensure that a majority agrees on every operation’s order. Coordination services such as Apache ZooKeeper and etcd provide these guarantees as reusable building blocks.

Many distributed problems—locks, uniqueness constraints, shared logs—reduce to consensus.

Under network partitions, you must choose: reject requests to preserve consistency, or serve stale data to remain available.

Consensus gives you one truth across many machines.

But it demands patience—and careful judgment about when that strength is truly necessary.
