# Category: Application Failure Patterns

## Description
These failures come from code execution, runtime behaviour, concurrency issues, and application logic faults. They include crashes, thread exhaustion, memory leaks, and state corruption that directly impact service reliability.

---

# 01. Pattern: Thundering Herd

## Description

The <a href="../../patterns/application/thundering-herd.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Thundering Herd** </a> pattern occurs when a large number of clients or services simultaneously attempt to perform the same operation, overwhelming a system resource.

This often happens when multiple workers, services, or processes are waiting on the same trigger event — such as a cache expiration, lock release, or service recovery.

When the event occurs, all waiting entities wake up and attempt the operation at the same time, creating a sudden surge of traffic or computation.

In distributed systems, this can rapidly overload databases, caches, APIs, or storage layers.

---

# 02. Pattern: Retry Storm

## Description

A <a href="../../patterns/application/retry-storm.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Retry Storm** </a> occurs when multiple services repeatedly retry failed requests in a short time window, unintentionally overwhelming the system they depend on.

Retries are normally designed to improve reliability. When a request fails due to a temporary issue (network hiccup, timeout, or transient service slowdown), the client retries the request to recover automatically.

---

# 03. Pattern: Cache Stampede

## Description

A <a href="../../patterns/application/cache-stampede.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Cache Stampede** </a> occurs when many clients attempt to regenerate a cached value simultaneously after the cache entry expires.

Instead of one process rebuilding the cache while others wait, multiple processes attempt the same expensive operation.

This can overload databases, APIs, or backend systems.

The problem becomes severe in high-traffic environments where cache entries expire at the same moment.

---

# 04. Pattern: Dependency Cascade

## Description

A <a href="../../patterns/application/dependency-cascade.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Dependency Cascade** </a> occurs when failure or slowdown in one service propagates through multiple dependent services, causing widespread system degradation.

Modern microservice architectures rely heavily on inter-service communication.

When one service becomes slow or unavailable, upstream services may block, retry, or fail — spreading the disruption throughout the system.

This cascading effect can rapidly transform a localized issue into a full system outage.

---

# 05. Pattern: Thread Pool Exhaustion

## Description

<a href="../../patterns/application/thread-pool-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Thread Pool Exhaustion** </a> occurs when all available worker threads in a service become occupied, preventing new requests from being processed.

Most application servers and frameworks use thread pools to manage concurrency.

If threads become blocked — waiting for slow operations such as database calls or external APIs — the pool can fill up quickly.

Once exhausted, incoming requests must wait or fail.

---

# 06. Pattern: Connection Pool Exhaustion

## Description

<a href="../../patterns/application/connection-pool-exhaustion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Connection Pool Exhaustion** </a> occurs when all available database or service connections are in use, preventing new requests from obtaining a connection.

Connection pools are used to limit the number of open connections to databases or external services.

When connections are held too long or requests increase suddenly, the pool may become depleted.

This causes requests to wait indefinitely or fail.

---

# 07. Pattern: Event Queue Backlog

## Description
<a href="../../patterns/application/event-queue-backlog.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Event Queue Backlog** </a> occurs when events are produced faster than they can be consumed, causing queues to grow uncontrollably.

This is common in systems using message brokers or asynchronous processing pipelines.

As backlog grows, event processing delays increase and downstream services become overwhelmed.

---

# 08. Lock Contention

## Description
<a href="../../patterns/application/lock-contention.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Lock Contention** </a> occurs when multiple processes, threads, or transactions compete for the same lock, causing work to block and throughput to fall.

This pattern appears in production systems when many operations target the same rows, keys, or shared resources at the same time. As lock wait times increase, requests become slower, queues form, and dependent services may begin to time out.

---

# 09. Memory Leak Under Load

## Description
A <a href="../../patterns/application/memory-leak-under-load.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Memory Leak Under Load** </a> occurs when an application gradually consumes increasing amounts of memory during sustained traffic, eventually exhausting available resources.

Memory leaks typically result from objects that are allocated but never released. Under light load, the leak may go unnoticed. However, under heavy traffic, memory consumption accelerates rapidly.

Over time, the system becomes unstable and may trigger garbage collection storms, swap usage, or container restarts.

---

# 10. Partial Service Degradation

## Description
<a href="../../patterns/application/partial-service-degradation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Partial Service Degradation** </a> occurs when a service continues operating but with reduced functionality or performance.

Instead of failing completely, certain operations fail while others remain available.

This often causes confusing symptoms during incident response.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back** </a>
