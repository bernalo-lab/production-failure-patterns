# Category: Data & Storage Failure Patterns 

---

# 01. Pattern: Database Connection Exhaustion

## Description

<a href="../../patterns/data/database-connection-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Database Connection Exhaustion** </a> occurs when the number of active database connections reaches the maximum allowed limit, preventing new requests from obtaining a connection.

This pattern appears in production systems when traffic spikes, queries run slowly, transactions remain open too long, or applications fail to release connections back to the pool. Once the connection limit is reached, application requests begin to queue, time out, or fail completely.

---

# 02. Pattern: Hot Partition / Hot Shard

## Description

A <a href="../../patterns/data/hot-partition.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Hot Partition** </a> occurs when a disproportionate amount of traffic targets a single shard, partition, or key within a distributed system.

While the system may appear balanced overall, one node or partition becomes overloaded.

This often happens in systems using hash-based partitioning when certain keys receive far more requests than others.

---

# 03. Pattern: Replication Lag

## Description

<a href="../../patterns/data/replication-lag.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Replication Lag** </a> occurs when a replica database or storage node falls behind the primary and no longer reflects current data in real time.

This pattern appears in production systems when write volume increases, replication channels slow down, network connectivity degrades, or replicas lack sufficient resources to keep up. As the lag grows, applications reading from replicas may serve stale data, causing inconsistent user behaviour and hard-to-diagnose incidents.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>

