# 20 “Black Swan” Rare Production Failure Patterns

## Description
These are low-frequency but high-impact failures that are difficult to predict and often bypass normal operational safeguards. They usually emerge from rare edge cases, hidden system assumptions, or unexpected combinations of events, causing major incidents with little warning.

---

# 01. Pattern: Leap Second Failure

## Description

<a href="../../patterns/rare-patterns/leap-second.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Leap Second Failure**</a> happens when systems fail to correctly handle the insertion of an extra second in UTC timekeeping, causing time calculations, scheduling, and distributed coordination to behave unpredictably.

This can trigger outages in databases, schedulers, authentication systems, and distributed clusters that depend heavily on precise timestamps.

---

# 02. Pattern: DNS Cache Poisoning

## Description

<a href="../../patterns/rare-patterns/dns-cache-poisoning.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**DNS Cache Poisoning**</a> happens when incorrect or malicious DNS records are cached by resolvers, causing services to resolve dependencies to the wrong destination.

This can create widespread outages, traffic blackholes, and severe security risks across internal and external systems.

---

# 03. Pattern: Certificate Revocation Failure

## Description

<a href="../../patterns/rare-patterns/certificate-revocation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Certificate Revocation Failure**</a> happens when systems fail to properly check revoked certificates or cannot reach revocation services like CRL or OCSP, causing trust failures or unintended access blocks.

This often creates authentication outages and unexpected TLS failures across production systems.

---

# 04. Pattern: Cross-Region Failover Split Brain

## Description

<a href="../../patterns/rare-patterns/cross-region-failover.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Cross-Region Failover Split Brain**</a> happens when two regions or clusters both believe they are the active primary after a failover event, causing conflicting writes, duplicate processing, and severe data inconsistency.

This is especially dangerous in active-active systems, disaster recovery environments, and globally distributed databases.

---

# 05. Pattern: Zombie Leader Election

## Description

<a href="../../patterns/rare-patterns/zombie-leader-election.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Zombie Leader Election**</a> happens when an old leader node continues acting as leader after leadership should have transferred, causing duplicate ownership and conflicting operations across distributed systems.

This often creates severe consistency issues in databases, schedulers, and orchestration platforms.

---

# 06. Pattern: Backup Restore Corruption

## Description

<a href="../../patterns/rare-patterns/backup-restore-corruption.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Backup Restore Corruption**</a> happens when a backup appears successful, but restoration reveals missing, incomplete, or corrupted data that cannot safely recover production systems.

This creates major disaster recovery failures during the worst possible moment—when restoration is urgently needed.

---

# 07. Pattern: Data Replay Disaster

## Description

<a href="../../patterns/rare-patterns/data-replay-disaster.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Data Replay Disaster**</a> happens when old messages, events, or transactions are unintentionally replayed into production systems, causing duplicate actions, financial errors, or widespread state corruption.

This is especially dangerous in payment systems, event-driven platforms, and distributed workflows where replayed operations are not safely idempotent.

---

# 08. Pattern: Time Zone Conversion Catastrophe

## Description

<a href="../../patterns/rare-patterns/time-zone-conversion.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Time Zone Conversion Catastrophe**</a> happens when incorrect timezone handling causes systems to execute business logic at the wrong time, often affecting billing, scheduling, authentication, or regulatory workflows.

These failures are especially dangerous during daylight saving transitions and cross-region operations.

---

# 09. Pattern: Expired Root Certificate Cascade

## Description

<a href="../../patterns/rare-patterns/expired-root-cert-cascade.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Expired Root Certificate Cascade**</a> happens when a widely trusted root certificate expires, causing dependent services, clients, and integrations to suddenly fail trust validation across large parts of the system.

This often creates global outages with confusing downstream failures.

---

# 10. Pattern: Mass Token Revocation Lockout

## Description

<a href="../../patterns/rare-patterns/mass-token-revo-lockout.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Mass Token Revocation Lockout**</a> happens when a large-scale token invalidation event revokes active sessions across users, services, or platforms, causing sudden access failures and widespread authentication disruption.

This is especially dangerous during secret rotation, IAM incidents, or emergency security response actions.

---

# 11. Pattern: Cloud Provider Control Plane Partition

## Description

<a href="../../patterns/rare-patterns/cloud-provider-control-plane.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Cloud Provider Control Plane Partition**</a> happens when the cloud provider’s management plane becomes unavailable or partially partitioned, preventing orchestration actions while workloads may still be running.

This creates major operational risk because systems appear healthy but cannot be managed, scaled, or recovered.

---

# 12. Pattern: Hidden Dependency Global Outage

## Description

<a href="../../patterns/rare-patterns/hidden-dependency-global.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Hidden Dependency Global Outage**</a> happens when an undocumented or poorly understood shared dependency fails, causing widespread impact across many unrelated services.

These failures are dangerous because engineers often do not realise the dependency even exists until production breaks.

---

# 13. Pattern: BGP Route Leak Blackhole

## Description

<a href="../../patterns/rare-patterns/bgp-route-leak-blackhole.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**BGP Route Leak Blackhole**</a. happens when incorrect routing information is propagated across the internet, causing traffic to be misrouted, intercepted, or completely dropped.

This can lead to large-scale outages affecting multiple regions, providers, and services simultaneously.

---

# 14. Pattern: Dead Letter Queue Silent Explosion

## Description

<a href="../../patterns/rare-patterns/dead-letter-queue.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Dead Letter Queue Silent Explosion**</a> happens when failed messages accumulate rapidly in a DLQ without triggering alerts, eventually overwhelming storage or hiding systemic failures.

This creates delayed outages and hidden data loss scenarios.

---

# 15. Pattern: Distributed Lock Global Freeze

## Description

<a href="../../patterns/rare-patterns/distributed-lock-global.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Distributed Lock Global Freeze**</a> happens when a locking mechanism fails or becomes stuck, preventing systems from progressing and effectively freezing critical workflows across services.

This can halt processing pipelines, job schedulers, and transactional systems.

---

# 16. Pattern: Retry Storm Triggered by Monitoring Failure

## Description

<a href="../../patterns/rare-patterns/retry-storm-triggered.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Retry Storm Triggered by Monitoring Failure**</a> happens when monitoring or alerting systems fail to detect an issue, allowing aggressive retry logic to escalate into a storm that overwhelms services.

This turns a small failure into a large-scale outage.

---

# 17. Pattern: Phantom Duplicate Payment Cascade

## Description

<a href="../../patterns/rare-patterns/phantom-duplicate-payment.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Phantom Duplicate Payment Cascade**</a> happens when payment systems unintentionally process the same transaction multiple times, often triggered by retries, race conditions, or replayed events.

This creates financial, legal, and trust issues at scale.

---

# 18. Pattern: Stale Disaster Recovery Environment Failure

## Description

<a href="../../patterns/rare-patterns/stale-disaster-recovery.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Stale Disaster Recovery Environment Failure**</a> happens when a DR environment is outdated, misconfigured, or not aligned with production, causing failover to fail or behave incorrectly during an incident.

---

# 19. Pattern: Backup Encryption Key Loss

## Description

<a href="../../patterns/rare-patterns/backup-encryption-key-loss.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Backup Encryption Key Loss**</a> happens when encryption keys required to decrypt backups are lost, corrupted, or inaccessible, rendering backups unusable.

This creates catastrophic data loss risk even when backups exist.

---

# 20. Pattern: Shadow Feature Flag Catastrophe

## Description

<a href="../../patterns/rare-patterns/shadow-feature-flag.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Shadow Feature Flag Catastrophe**</a> happens when hidden, forgotten, or poorly controlled feature flags unexpectedly activate or conflict, causing major production instability.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>
