# Category: Dependency Failure Patterns

External services or internal dependencies.

These often create cascading failures.

---

# 01. Third-Party Dependency Degradation

## Description

<a href="../../patterns/dependency/third-party-dependency-degradation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Third-Party Dependency Degradation**</a> occurs when an external service that your system relies on becomes slow, unstable, or partially unavailable.

Unlike a complete outage, the dependency still responds but with degraded performance or intermittent failures. Because the dependency technically remains available, systems often continue sending traffic, which can propagate latency and failures throughout the system.

This pattern frequently causes cascading latency across services that depend on the degraded system.

---

# 02. DNS Resolution Failure

## Description

<a href="../../patterns/dependency/dns-resolution-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**DNS Resolution Failure**</a> occurs when services cannot resolve the hostname of a dependency or internal service.

Without proper DNS resolution, applications cannot locate the IP address of required services. This results in connection failures even though the target system may still be healthy.

DNS failures can disrupt large portions of distributed systems.

---

# 03. Expired Certificate

## Description

<a href="../../patterns/dependency/expired-certificate.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Expired Certificate**</a> occur when TLS/SSL certificates used for secure communication reach their expiration date.

Once expired, clients will refuse secure connections, causing services that rely on HTTPS or TLS communication to fail.

This often causes sudden outages despite the underlying service being healthy.

---

# 04. API Rate Limit Saturation

## Description

<a href="../../patterns/dependency/api-rate-limit-saturation.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**API Rate Limit Saturation**</a> occurs when a system exceeds the allowed request quota imposed by a dependency or internal API.

When rate limits are exceeded, the dependency begins rejecting requests, typically with HTTP 429 responses.

This often triggers retries that worsen the situation.

---

# 05. Authentication Service Failure

## Description

<a href="../../patterns/dependency/authentication-service-failure.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Authentication Service Failure**</a> occurs when the system responsible for issuing or validating authentication tokens becomes unavailable or unstable.

Because many services depend on authentication validation, this failure can block access across the entire platform.

---

# 06. Configuration Service Outage

## Description

<a href="../../patterns/dependency/configuration-service-outage.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Configuration Service Outage**</a> occurs when centralized configuration management systems become unavailable.

Services depending on dynamic configuration may fail to start or operate incorrectly.

---

# 07. Downstream Retry Amplification

## Description

<a href="../../patterns/dependency/downstream-retry-amplification.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Downstream Retry Amplification**</a> occurs when retry mechanisms multiply traffic toward failing services.

Instead of reducing failure impact, retries create additional load that worsens the problem.

---

# 08. Message Queue Backlog

## Description

<a href="../../patterns/dependency/message-queue-backlog.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Message Queue Backlog**</a> occurs when producers send messages faster than consumers can process them.

Over time, messages accumulate, causing delays and potential system instability.

---

# 09. Event Bus Lag

## Description

<a href="../../patterns/dependency/message-queue-backlog.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Event Bus Lag**</a> occurs when event propagation across distributed systems slows down.

Events remain in the event stream longer than expected, delaying downstream processing.

---

# 10. Dependency Timeout Cascade

## Description

<a href="../../patterns/dependency/dependency-timeout-cascade.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**Dependency Timeout Cascade**</a> occurs when one slow dependency causes multiple upstream services to experience timeouts.

These timeouts propagate through the call chain, eventually impacting many services.

---

<a href="../../README.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<< Back**</a>
