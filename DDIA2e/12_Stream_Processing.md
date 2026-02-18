# RIGHT PAGE — Article

## Stream Processing

Batch processing assumes the world pauses long enough for us to analyze it. Stream processing assumes it never does.

In batch systems, data is treated as complete. A dataset arrives, we process it, and we produce an output. There is a clear beginning and end. But most real-world systems do not behave this way. Users keep clicking. Sensors keep emitting readings. Markets keep moving. Data is not finite — it is unbounded.

Stream processing is a shift in mindset. Instead of waiting for data to be complete, we process each event as it arrives. An event is the atomic unit of a stream: a small, immutable record of something that happened at a specific time. The system never finishes; it continuously incorporates new events into its state.

This changes how we think about infrastructure. Traditional message brokers often treat messages as disposable. Once acknowledged, they disappear. But log-based systems treat streams as append-only logs. Nothing is erased. Consumers track their own position. This allows replaying history, rebuilding state, and deriving new views from past events.

At a deeper level, stream processing reveals a powerful duality: state and streams are two perspectives on the same reality. Current state can be seen as the accumulation of all past events. Conversely, a stream of changes is simply the record of how state evolves over time. Techniques like Change Data Capture make this explicit by turning database mutations into event streams.

Time becomes subtle. Events have an event time — when they actually happened — and a processing time — when the system handled them. If these diverge, naive windowing can produce misleading results. Stream processors must reason carefully about windows, joins, and late arrivals.

Fault tolerance also changes. Because streams are infinite, you cannot restart from the beginning. Instead, systems rely on checkpointing, idempotence, and transactional guarantees to achieve exactly-once semantics.

Stream processing is not just faster batch processing. It is a different mental model: the world as a continuous flow of events, where systems must remain correct while the story is still unfolding.

---

# LEFT PAGE — Visual Note

## Stream Processing

**Computing while the story unfolds**

---

### 1️⃣ Event as the Atom

🧩 Icon: small dot or spark

* Small immutable record (cannot be changed after creation — like ink on paper)
* Something happened (a click, payment, reading — concrete action)
* Has a timestamp (anchors it in time — narrative marker)
* Self-contained fact (no hidden context — portable truth)

---

### 2️⃣ Batch vs Stream

📦➡️🌊 Icon: box turning into wave

* Batch = finite dataset (clear start and end — closed book)
* Stream = unbounded flow (never-ending input — live broadcast)
* Batch waits for completeness (delayed reflection — report tomorrow)
* Stream reacts immediately (near-real-time response — live dashboard)

---

### 3️⃣ Messaging Evolution

📨 Icon: envelope vs log stack

* AMQP/JMS: message deleted after ack (task queue model — disposable mail)
* Order less critical (parallel tasks — factory line)
* Log-based broker: append-only log (like a ledger — permanent record)
* Replay possible (rebuild state — rewind history)

---

### 4️⃣ State ↔ Stream Duality

♻️ Icon: loop arrow

* State = accumulation of events (sum over time — running total)
* Stream = record of changes (diff of state — change history)
* Change Data Capture (database emits updates — shadow narrator)
* Derived systems stay synced (search, cache, analytics — mirrors)

---

### 5️⃣ Time Complexity

⏳ Icon: clock split in two

* Event time (when it actually happened — story order)
* Processing time (when system handled it — viewing order)
* Late arrivals distort windows (network lag — delayed scenes)
* Windows define analysis scope (tumbling, sliding, session — framing lens)

---

### 6️⃣ Stream Joins

🔗 Icon: linking chains

* Stream–stream join (match events within window — search → click)
* Stream–table join (enrich with database — add profile info)
* Table–table join (combine changelogs — materialized view)
* Continuous matching (never fully done — moving target)

---

### 7️⃣ Fault Tolerance

🛡️ Icon: shield

* Streams are infinite (cannot restart from zero — no rewind to origin)
* Checkpoint state (periodic snapshot — save progress)
* Idempotent writes (safe repetition — pressing button twice same effect)
* Exactly-once semantics (effect as if once — illusion of perfection)

---

# YOUTUBE SHORTS — 60s Transcript

When we talk about data processing, we often imagine a dataset that arrives, gets processed, and produces an output. That’s batch thinking. But most systems don’t operate in batches. They operate in streams.

Users keep clicking. Sensors keep emitting signals. Markets keep updating. Data doesn’t stop. It flows.

Stream processing is about handling each event as it happens. An event is a small, immutable fact — something that occurred at a specific time. The system continuously updates its state as new events arrive.

What’s powerful is the duality between state and streams. Your current database state is just the accumulation of all past events. And a stream is simply the record of how that state changes over time.

But time becomes tricky. There’s when an event actually happened, and when your system processed it. If those don’t align, your analytics can mislead you.

So stream processing isn’t just about speed. It’s about reasoning correctly in a world that never stops generating events.
