# Pattern: Memory Leak Under Load

## Description

A Memory Leak Under Load occurs when an application gradually consumes increasing amounts of memory during sustained traffic, eventually exhausting available resources.

Memory leaks typically result from objects that are allocated but never released. Under light load, the leak may go unnoticed. However, under heavy traffic, memory consumption accelerates rapidly.

Over time, the system becomes unstable and may trigger garbage collection storms, swap usage, or container restarts.

---

## Typical Symptoms

Engineers may observe:

- Gradually increasing memory usage
- Frequent garbage collection cycles
- Sudden container or service restarts
- Increasing latency under load
- Out-of-memory errors
- Service crashes

---

## Common Misleading Signals

The issue may appear as:

- High traffic levels
- Infrastructure instability
- Container orchestration problems

However, the root cause is typically **memory not being released properly within the application**.

---

## Likely Root Causes

Typical causes include:

- Objects not released after processing
- Growing caches without eviction policies
- Resource handles left open
- Background tasks accumulating state
- Session objects stored indefinitely

---

## First Checks

Engineers should check:

- Memory usage trends
- Heap allocation patterns
- Garbage collection metrics
- Object growth in heap dumps
- Application restart frequency

---

## Useful Signals

Look for:

- Heap size growth over time
- Frequent GC pauses
- Increasing memory allocation rate
- Heap dump object analysis

---

## Prevention

### Memory Profiling

Use profiling tools to detect leaks early.

### Cache Eviction Policies

Ensure caches have TTL or size limits.

### Resource Cleanup

Release objects, connections, and file handles properly.

### Load Testing

Run sustained load tests to detect leaks before production.

---

<a href="../../categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
