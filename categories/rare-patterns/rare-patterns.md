# 20 “Black Swan” Rare Production Failure Patterns

## Description
These are low-frequency but high-impact failure patterns that can create severe outages, regulatory incidents, financial loss, or complete operational paralysis. They are often difficult to predict, poorly documented, and rarely included in standard incident playbooks.

When they happen, they expose gaps in architecture, resilience planning, and incident judgement.

These patterns create authority because very few engineers prepare for them properly.

---

1. # Leap Second Failure

Time-based systems fail due to unexpected leap second handling, causing crashes, scheduling failures, or distributed coordination issues.

---

2. # DNS Cache Poisoning

Corrupted or malicious DNS resolution causes services to route traffic to invalid or hostile destinations.

---

3. # Certificate Revocation Failure

A revoked certificate remains trusted or revocation checks fail, creating security and availability risks.

---

4. # Cross-Region Failover Split Brain

Two regions believe they are primary simultaneously, causing data corruption, duplicate writes, or operational conflict.

---

5. # Zombie Leader Election

A failed node continues acting as leader after replacement, creating inconsistent writes and coordination failures.

---

6. # Backup Restore Corruption

Backups appear healthy but fail during restoration, revealing unusable recovery paths during critical incidents.

---

7. # Data Replay Disaster

Replay of historical events or messages causes duplication, financial inconsistencies, or irreversible workflow corruption.

---

8. # Timezone Rule Change Failure

Government or regional timezone changes break scheduling, billing, trading, or compliance workflows unexpectedly.

---

9. # Expired Root Certificate Authority

A trusted root CA expires, breaking TLS validation across large parts of the platform simultaneously.

---

10. # Cloud Provider Regional Metadata Failure

Cloud metadata or identity services fail regionally, breaking instance startup, credential refresh, or service discovery.

---

11. # Hidden Dependency Blackout

An undocumented internal dependency fails and causes widespread outages because nobody knew it was critical.

---

12. # Orphaned Distributed Lock

A stale distributed lock survives failure conditions and permanently blocks critical production workflows.

---

13. # Phantom Retry Storm

Retries continue from forgotten legacy workers or zombie consumers, creating unexplained saturation without visible ownership.

---

14. # Compliance Kill Switch Trigger

Automated compliance or fraud protection systems disable legitimate production traffic at scale.

---

15. # Immutable Log Corruption

Audit logs or append-only stores become corrupted, creating operational and legal recovery risks.

---

16. # Cascading Feature Flag Reversal

Emergency flag rollback triggers unexpected dependency failures across unrelated services.

---

17. # Global Clock Drift Event

Large-scale time drift across nodes breaks certificates, distributed coordination, and ordering guarantees.

---

18. # Silent Data Truncation

Systems silently truncate payloads or records without alerting, causing delayed business and compliance failures.

---

19. # Emergency Vendor Shutdown

A critical SaaS provider or payment gateway becomes unavailable with no immediate migration path.

---

20. # Disaster Recovery Runbook Failure

The documented DR process itself fails during execution because assumptions, permissions, or dependencies are outdated.

---

# Why These Matter

**Most engineers prepare for**:

CPU spikes
memory leaks
dependency timeouts

*Very few prepare for*:

split brain
broken restore paths
replay disasters
trust chain collapse

*That difference separates*:

<b>Monitoring Engineers</b> from <b>Incident Engineers</b>

This is exactly where serious authority is built.

---

A <a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>
