# **E - Scale and Distribution**

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f304d0ce-226e-4115-a8d7-bb1315ed7f86" />

> From first principles, these concepts arise from the need to build systems that can handle **more data, arriving faster, without failing**. As **volume** increases, a single machine becomes insufficient, forcing data to be **partitioned** into smaller pieces so work can be distributed. When those partitions are spread across multiple machines, this becomes **sharding**, enabling horizontal growth. Increasing **velocity** and **variety** put additional pressure on the system, requiring it to process diverse data quickly, which directly impacts **throughput**, or how much work the system can complete in a given time. To raise throughput, systems parallelize across shards, but parallelism introduces failure risk, which is why **replication** is necessary to maintain availability. Replication enables **fault tolerance**, allowing the system to continue operating even when individual components fail. Together, partitioning, sharding, replication, and fault tolerance allow the system to maintain throughput under growing volume, velocity, and variety—this combined capability is what we call **scalability**.

> Volume, Velocity, Variety → Partitioning, Sharding → Throughput → Replication, Fault Tolerance → Scalability
