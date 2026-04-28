# Category: Business Logic & Workflow Failure Patterns

## Description
These failures occur when business processes break even though infrastructure appears healthy. They involve duplicate processing, failed compensations, stuck workflows, payment inconsistencies, and orchestration deadlocks that traditional monitoring often misses.

---

# 01. Pattern: Idempotency Failure

## Description

<a href="../../patterns/business-logic/idempotency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Idempotency Failure**</a> happens when the same operation is processed multiple times and produces different or duplicate outcomes instead of safely returning the same result.

This creates financial errors, duplicate records, repeated notifications, and inconsistent workflow behaviour, especially in distributed systems with retries and async processing.

---

# 02. Pattern: Duplicate Event Processing

## Description

<a href="../../patterns/business-logic/duplicate-event-processing.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Duplicate Event Processing**</a> happens when the same event is consumed more than once and downstream systems process each copy as a new action.

This often creates invisible operational failures because infrastructure appears healthy while business outcomes become inconsistent.

---

# 03. Pattern: Poison Message Loop

## Description

<a href="../../patterns/business-logic/poison-message-loop.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Poison Message Loop**</a> happens when a malformed or problematic message repeatedly fails processing and is continuously retried without resolution.

This blocks consumer throughput, increases queue pressure, and creates hidden operational failures that appear as platform instability.

---

# 04. Pattern: Compensating Transaction Failure

## Description

<a href="../../patterns/business-logic/compensating-transaction.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Compensating Transaction Failure**</a> happens when rollback or recovery actions meant to reverse a failed workflow also fail, leaving the system in a partially completed and inconsistent state.

This is especially dangerous in payment systems, booking flows, and distributed transaction processes.

---

# 05. Pattern: Workflow Orchestration Deadlock

## Description

<a href="../../patterns/business-logic/workflow-orchestration-deadlock.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Workflow Orchestration Deadlock**</a> happens when multiple services or workflow steps wait indefinitely for each other to complete, preventing forward progress.

This creates silent operational failures because systems appear alive but business processes stop moving.

---

# 06. Pattern: Payment State Inconsistency

## Description

<a href="../../patterns/business-logic/payment-state-inconsistency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Payment State Inconsistency**</a> happens when payment status differs across systems such as payment gateways, internal ledgers, order systems, and customer records.

The payment may be successful in one system and failed or pending in another, creating operational confusion and customer trust issues.

---

# 07. Pattern: Retry Without State Validation

## Description

<a href="../../patterns/business-logic/retry-without-state-val.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Retry Without State Validation**</a> happens when failed operations are retried without first checking whether the previous attempt partially or fully succeeded.

This creates duplicate actions, financial inconsistencies, and hidden business workflow corruption.

---

# 08. Pattern: Human Approval Bottleneck Failure

## Description

<a href="../../patterns/business-logic/human-approval-bottleneck.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Human Approval Bottleneck Failure**</a> happens when manual approval steps become delayed, blocked, or unavailable, causing automated workflows to stall.

This often creates invisible operational incidents because the platform is technically healthy, but business outcomes stop progressing.

---

# 09. Pattern: Scheduled Job Overlap Collision

## Description

<a href="../../patterns/business-logic/scheduled-job-overlap.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Scheduled Job Overlap Collision**</a> happens when recurring jobs start before previous executions have completed, causing duplicate work, contention, or conflicting updates.

This is common in reporting jobs, billing runs, cleanup tasks, and data synchronisation processes.

---

# 10. Pattern: Zombie Process / Orphaned Workflow

## Description

<a href="../../patterns/business-logic/zombie-process.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Zombie Process / Orphaned Workflow**</a> happens when background jobs, transactions, or workflows continue running without ownership, visibility, or proper completion paths.

These hidden processes consume resources, create stale state, and silently block normal operations.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
