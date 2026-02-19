# Stream Processing

*Continuous computation on unbounded reality.*

---

## RIGHT PAGE — Article (~370 words)

Batch processing assumes the world pauses. You collect a complete dataset, run computation, and produce output. Stream processing rejects that assumption. In the real world, data does not finish. Users click, sensors emit readings, databases change, markets move. The dataset is unbounded.

The fundamental unit of a stream is an event: a small, immutable record of something that happened at a specific time. Instead of processing a finished dataset, stream systems process events continuously as they arrive, reducing the delay between cause and effect.

This shift required a change in infrastructure. Traditional brokers like Java Message Service or Advanced Message Queuing Protocol treat messages as transient tasks. Once acknowledged, they disappear. That works for task queues. It does not work when history matters.

Log-based brokers such as Apache Kafka changed the model. A stream becomes an append-only log stored on disk. Consumers track their position using offsets. Messages are not deleted; they can be replayed. This enables recovery, reprocessing, and the construction of new derived systems from historical data.

At the core lies a powerful duality: state and streams are two views of the same system. Application state is the integration of all past events. A change stream is the derivative of that state over time. Techniques like change data capture turn database writes into streams, allowing caches, search indexes, and analytics systems to stay synchronized with the system of record.

Time introduces complexity. Event time describes when something actually happened. Processing time describes when the system handled it. These differ because networks delay, systems restart, and events arrive late. Windowing strategies—tumbling, hopping, sliding, and session windows—define how we aggregate across time despite disorder.

Stream joins extend relational thinking into continuous data. We join stream-to-stream within windows, stream-to-table for enrichment, and table-to-table to maintain materialized views from changelogs.

Because streams never end, fault tolerance must be incremental. Microbatching, checkpointing, idempotent writes, and atomic commits enable exactly-once semantics—the effect as if each event were processed once, even if retries occur.

Stream processing is batch processing without an end. The filesystem becomes a log. The job becomes a perpetual computation. The system becomes a living function over time.

---

## LEFT PAGE — Visual Note (Hand-Drawable)

**Stream Processing**
*The world does not pause.*

---

### 1️⃣ Unbounded Data

🕒 Icon: Infinite loop

* Data never finishes (user clicks, sensors) — real world flow
* Events arrive continuously — no final snapshot
* Computation must be ongoing — perpetual job

---

### 2️⃣ Event = Atomic Fact

📦 Icon: Small sealed box

* Immutable record of something — cannot edit history
* Has a timestamp — moment in time
* Self-contained payload — minimal unit

---

### 3️⃣ Messaging Evolution

📨 Icon: Two pipeline paths

* JMS/AMQP delete after ack — task queue model
* Apache Kafka retains append-only log — replayable history
* Consumers track offsets — bookmark position

---

### 4️⃣ State ↔ Stream Duality

🔄 Icon: Integral symbol loop

* State = integration of events — accumulated past
* Stream = derivative of state — change over time
* CDC extracts DB changes — sync systems

---

### 5️⃣ Reasoning About Time

⏳ Icon: Two clocks

* Event time ≠ processing time — arrival lag
* Late events distort windows — backlog spikes
* Windows: tumbling, hopping, sliding, session — time slicing

---

### 6️⃣ Stream Joins

🔗 Icon: Interlocking chains

* Stream–stream — within time window
* Stream–table — enrich with latest state
* Table–table — materialized view updates

---

### 7️⃣ Exactly-Once Semantics

🛡️ Icon: Shield with checkmark

* Checkpoint state periodically — recovery anchor
* Idempotent writes — safe retries
* Atomic commits — all or nothing

---

### 8️⃣ Mental Model

🎬 Icon: Film reel

* Release order ≠ story order — narrative timing
* Must reorder by event time — correct history
* Continuous batch thinking — never-ending input

---

## YOUTUBE SHORTS (~60 seconds)

Stream processing begins with a simple realization: data never finishes.

In batch systems, we assume completeness. In reality, events continue indefinitely—clicks, transactions, sensor readings. Instead of processing a fixed dataset, we process events one by one as they arrive.

An event is immutable. It represents something that happened at a specific time. When you append events to a log, you are recording history. Systems like Apache Kafka treat streams as durable logs, not disposable messages. That means you can replay history, rebuild state, or recover from failure.

There is a deep idea underneath: state and streams are dual. State is simply the accumulation of all past events. A stream is the sequence of changes to that state.

Time complicates everything. Events happen at one time but may be processed later. Good stream systems distinguish event time from processing time and use windows to compute aggregates correctly despite delays.

Joins, enrichment, materialized views, and exactly-once guarantees all build on one principle: continuous computation over unbounded data.

Stream processing is not a different paradigm from batch. It is batch processing that never ends.
