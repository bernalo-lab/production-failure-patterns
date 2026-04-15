# Category: Data & Storage Failure Patterns 

---

# 01. Pattern: Database Connection Exhaustion

## Description

<a href="../../patterns/data/database-connection-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Database Connection Exhaustion**</a> occurs when the number of active database connections reaches the maximum allowed limit, preventing new requests from obtaining a connection.

This pattern appears in production systems when traffic spikes, queries run slowly, transactions remain open too long, or applications fail to release connections back to the pool. Once the connection limit is reached, application requests begin to queue, time out, or fail completely.

---

# 02. Pattern: Hot Partition / Hot Shard

## Description

A <a href="../../patterns/data/hot-partition.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Hot Partition**</a> occurs when a disproportionate amount of traffic targets a single shard, partition, or key within a distributed system.

While the system may appear balanced overall, one node or partition becomes overloaded.

This often happens in systems using hash-based partitioning when certain keys receive far more requests than others.

---

# 03. Pattern: Replication Lag

## Description

<a href="../../patterns/data/replication-lag.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Replication Lag**</a> occurs when a replica database or storage node falls behind the primary and no longer reflects current data in real time.

This pattern appears in production systems when write volume increases, replication channels slow down, network connectivity degrades, or replicas lack sufficient resources to keep up. As the lag grows, applications reading from replicas may serve stale data, causing inconsistent user behaviour and hard-to-diagnose incidents.

---

# 04. Pattern: Database Lock Contention

## Description

<a href="../../patterns/data/database-lock-contention.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Database Lock Contention**</a> occurs when multiple transactions attempt to access the same database resources simultaneously and are forced to wait for locks to be released.

This pattern commonly appears in production systems during high concurrency workloads, poorly designed transaction boundaries, or when long-running transactions hold locks for extended periods. As contention increases, query latency rises and application throughput drops.

---

# 05. Pattern: Storage Latency Spike

## Description

A <a href="../../patterns/data/storage-latency-spike.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Storage Latency Spike**</a> occurs when the time required to read or write data from persistent storage suddenly increases.

This pattern often appears in distributed systems when storage nodes become overloaded, disks enter degraded states, or background maintenance tasks interfere with normal workloads. Even small increases in storage latency can cascade into application-level timeouts and system instability.

---

# 06. Pattern: Index Corruption or Missing Index

## Description

<a href="../../patterns/data/index-corruption.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Index Corruption or Missing Index**</a> occurs when database indexes become invalid, corrupted, or are missing entirely for critical queries.

Indexes are essential for efficient data retrieval. When they are corrupted or missing, the database may fall back to full table scans, dramatically increasing query latency and resource consumption.

---

# 07. Pattern: Transaction Deadlock Storm

## Description

A <a href="../../patterns/data/transaction-deadlock-storm.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Transaction Deadlock Storm**</a> occurs when multiple transactions hold locks that block each other in a circular dependency, causing the database to abort transactions repeatedly.

When deadlocks occur frequently, systems may experience retries, increased latency, and cascading service degradation.

---

# 08. Pattern: Schema Migration Failure

## Description

A <a href="../../patterns/data/schema-migration-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Schema Migration Failure**</a> occurs when database schema changes fail during deployment or introduce incompatibilities with running application versions.

In large distributed systems, schema migrations must be coordinated carefully. If migrations break compatibility or fail midway, applications may begin failing unexpectedly.

---

# 09. Pattern: Backup Job Interference

## Description

<a href="../../patterns/data/backup-job-interference.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Backup Job Interference**</a> occurs when scheduled database or storage backups consume significant system resources and negatively impact production workloads.

Backup processes may compete with live traffic for disk I/O, CPU, or database locks, causing latency spikes and service degradation.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>

