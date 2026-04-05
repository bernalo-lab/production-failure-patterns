# Category: Application

---

# 01. Pattern: Thundering Herd

## Description

The **Thundering Herd** pattern occurs when a large number of clients or services simultaneously attempt to perform the same operation, overwhelming a system resource.

This often happens when multiple workers, services, or processes are waiting on the same trigger event — such as a cache expiration, lock release, or service recovery.

When the event occurs, all waiting entities wake up and attempt the operation at the same time, creating a sudden surge of traffic or computation.

In distributed systems, this can rapidly overload databases, caches, APIs, or storage layers.

---

# 02. Pattern: Retry Storm

## Description

A **Retry Storm** occurs when multiple services repeatedly retry failed requests in a short time window, unintentionally overwhelming the system they depend on.

Retries are normally designed to improve reliability. When a request fails due to a temporary issue (network hiccup, timeout, or transient service slowdown), the client retries the request to recover automatically.

---

# 03. Pattern: Cache Stampede

## Description

A **Cache Stampede** occurs when many clients attempt to regenerate a cached value simultaneously after the cache entry expires.

Instead of one process rebuilding the cache while others wait, multiple processes attempt the same expensive operation.

This can overload databases, APIs, or backend systems.

The problem becomes severe in high-traffic environments where cache entries expire at the same moment.

---

# 04. Pattern: Dependency Cascade

## Description

A **Dependency Cascade** occurs when failure or slowdown in one service propagates through multiple dependent services, causing widespread system degradation.

Modern microservice architectures rely heavily on inter-service communication.

When one service becomes slow or unavailable, upstream services may block, retry, or fail — spreading the disruption throughout the system.

This cascading effect can rapidly transform a localized issue into a full system outage.

---

# 05. Pattern: Thread Pool Exhaustion

## Description

Thread Pool Exhaustion occurs when all available worker threads in a service become occupied, preventing new requests from being processed.

Most application servers and frameworks use thread pools to manage concurrency.

If threads become blocked — waiting for slow operations such as database calls or external APIs — the pool can fill up quickly.

Once exhausted, incoming requests must wait or fail.

---

# 06. Pattern: Connection Pool Exhaustion

## Description

Connection Pool Exhaustion occurs when all available database or service connections are in use, preventing new requests from obtaining a connection.

Connection pools are used to limit the number of open connections to databases or external services.

When connections are held too long or requests increase suddenly, the pool may become depleted.

This causes requests to wait indefinitely or fail.

---
