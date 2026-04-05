# Pattern: Hot Partition

## Description

A Hot Partition occurs when a disproportionate amount of traffic targets a single shard, partition, or key within a distributed system.

While the system may appear balanced overall, one node or partition becomes overloaded.

This often happens in systems using hash-based partitioning when certain keys receive far more requests than others.

---

## Typical Symptoms

Engineers may observe:

- One database shard overloaded
- Uneven CPU usage across nodes
- High latency for specific requests
- Increased error rates for specific keys

---

## Common Misleading Signals

The issue may appear as:

- Database performance problems
- Infrastructure imbalance
- Application inefficiency

But the real cause is **traffic concentration on a single partition**.

---

## Likely Root Causes

Typical causes include:

- Poor key distribution
- Popular user accounts
- Trending content
- Partitioning strategy limitations
- Sequential key generation

---

## First Checks

Engineers should inspect:

- Partition-level metrics
- Request distribution
- Key access frequency
- Node utilisation

---

## Useful Signals

Look for:

- Uneven load across partitions
- High request counts for specific keys
- Node-level performance disparities

---

## Prevention

### Better Partitioning Strategy

Use consistent hashing or improved key distribution.

### Load Balancing

Redistribute hot keys across nodes.

### Rate Limiting

Protect popular endpoints.

### Caching

Reduce repeated requests for hot keys.

---

<a href="../../categories/data/data.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
