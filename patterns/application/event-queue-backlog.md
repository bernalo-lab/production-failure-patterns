# Pattern: Event Queue Backlog

## Description

Event Queue Backlog occurs when events are produced faster than they can be consumed, causing queues to grow uncontrollably.

This is common in systems using message brokers or asynchronous processing pipelines.

As backlog grows, event processing delays increase and downstream services become overwhelmed.

---

## Typical Symptoms

Common indicators include:

- Growing message queue depth
- Delayed event processing
- Consumer lag
- Increased system latency
- Worker saturation

---

## Common Misleading Signals

The issue may appear as:

- Slow consumers
- Broker instability
- Application performance issues

However, the real issue is **an imbalance between event production and consumption**.

---

## Likely Root Causes

Typical causes include:

- Slow event consumers
- Consumer crashes
- Downstream dependency delays
- Insufficient worker scaling
- Event burst spikes

---

## First Checks

Check:

- Queue depth metrics
- Consumer processing rate
- Event production rate
- Worker health
- Broker performance

---

## Useful Signals

Look for:

- Increasing consumer lag
- Worker saturation metrics
- Event processing latency

---

## Prevention

### Consumer Autoscaling

Scale consumers dynamically based on queue depth.

### Rate Limiting

Control event production rate.

### Dead Letter Queues

Handle failed messages separately.

### Backpressure

Signal producers to slow down when queues grow.

---

<a href="../../categories/application/application.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**>> Back**</a>
