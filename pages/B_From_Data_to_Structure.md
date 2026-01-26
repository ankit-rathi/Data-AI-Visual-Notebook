# **B - From Data to Structure**

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/089b5a07-4361-4dc8-94e8-6350d4bcbd69" />

> To remember reality at scale, we first capture individual facts as **records**, each holding one piece of truth. Since facts have multiple parts, we divide records into **fields**. To make sure everyone understands the fields the same way, we agree on a **schema**, which defines what each field means. When similar facts repeat over time, they form a **table**, but repetition alone isn’t enough—each record needs a unique identity, which is why we use a **primary key**. Reality is connected, so records are linked through **relationships**, helping the system represent the world without mistakes or duplication. All of this is managed by a **database**, whose main job is not just storing facts, but keeping them reliable. When reality changes, updates happen in complete units called **transactions**, because partial updates can create wrong information. **Consistency** makes sure updates follow the rules, and **latency** reminds us that data loses value if it arrives too late. Together, these ideas help us **store truth safely and usefully**, even as the world changes around us.

> Record → Field → Schema → Table → Primary Key, Relationship → Database, Transaction, Consistency → Latency
