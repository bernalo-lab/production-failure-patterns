# Pattern: Retry Storm

## Description

A **Retry Storm** occurs when multiple services repeatedly retry failed requests in a short time window, unintentionally overwhelming the system they depend on.

Retries are normally designed to improve reliability. When a request fails due to a temporary issue (network hiccup, timeout, or transient service slowdown), the client retries the request to recover automatically.

However, when retries are misconfigured or uncontrolled, they can create a **positive feedback loop**:

1. A downstream service slows or fails.
2. Upstream services retry aggressively.
3. The additional traffic increases load on the failing service.
4. The dependency slows down even further.
5. More retries are triggered.

Within seconds, a relatively small failure can turn into a **system-wide cascading failure**.

Retry storms are especially dangerous in **microservice architectures**, where dozens or hundreds of services communicate over the network and rely heavily on automated retry logic.

---

## Typical Symptoms

Engineers often observe the following behaviours during a retry storm:

- Sudden **spike in request volume**
- Rapid **increase in error rates**
- **Queue depth growth** in message queues or worker systems
- **Timeouts between services**
- **High CPU or thread usage** on dependent services
- **Duplicate requests** arriving at downstream APIs
- Significant **latency spikes across multiple services**
- Database or third-party API saturation

In many cases, the system appears to be under **unexpected heavy traffic**, even though the real cause is retry amplification.

---

## Common Misleading Signals

Retry storms frequently mislead engineers during incident response.

Common misinterpretations include:

- Appears like a **sudden traffic spike from users**
- Looks like a **database performance failure**
- Alerts from a **downstream service failing first**
- Metrics suggesting **high load rather than cascading retries**
- Autoscaling events that appear to trigger the problem

Because retries amplify traffic, the root cause can be mistaken for a **capacity issue**, when the real problem is uncontrolled retry behaviour.

---

## Likely Root Causes

Retry storms typically arise from a combination of system design and configuration issues.

Common root causes include:

- **Aggressive retry policies**
  - Immediate retries without delay
- **Lack of exponential backoff**
- **Missing jitter in retry intervals**
- **Multiple retry layers**
  - Client retries
  - API gateway retries
  - SDK retries
- **Dependency slowdown or partial outage**
- **Missing circuit breakers**
- **High request fan-out architectures**
- **Retries triggered across multiple services simultaneously**

In distributed systems, these factors combine to create **retry amplification**, where the original traffic multiplies exponentially.

---

## First Checks

When engineers suspect a retry storm, the following checks can help quickly confirm the issue:

1. **Retry configuration**
   - Are retries immediate?
   - How many retry attempts are configured?

2. **Downstream error rate**
   - Which service started failing first?

3. **Request amplification**
   - Are duplicate requests being generated?

4. **Queue or worker metrics**
   - Is queue depth growing unusually fast?

5. **Dependency health**
   - Is a third-party API or internal service degraded?

6. **Autoscaling behaviour**
   - Are additional instances being created due to retry load?

Quickly identifying the retry amplification pattern can prevent engineers from chasing incorrect root causes.

---

## Useful Signals

The following signals are particularly helpful when diagnosing retry storms:

### Logs

Look for patterns such as:

- repeated request IDs
- retry messages in application logs
- timeout errors across services

Example indicators:

- `retry attempt=1`
- `retry attempt=2`
- `timeout contacting service`

---

### Metrics

Useful metrics include:

- **Request rate per service**
- **Retry count**
- **HTTP 5xx error rate**
- **Dependency latency**
- **Queue depth**
- **Worker thread usage**

A classic sign of retry storms is:

> Request volume increasing while success rate decreases.

---

### Traces

Distributed tracing can reveal:

- repeated identical requests
- cascading service retries
- repeated spans to the same dependency

This helps confirm that retries, rather than user traffic, are driving load.

---

## Prevention

Several engineering practices help prevent retry storms from occurring.


### Exponential Backoff

Retries should gradually increase delay between attempts.

Example:

Retry 1 → wait 100ms
Retry 2 → wait 300ms
Retry 3 → wait 900ms


This reduces retry amplification.

---

### Jitter

Randomizing retry intervals prevents synchronized retry waves across services.

Without jitter, thousands of clients may retry simultaneously.

---

### Circuit Breakers

Circuit breakers stop retry attempts when a dependency is clearly failing.

This protects downstream systems from overload.

---

### Retry Budgets

Limit the total retry volume allowed within a time window.

This prevents runaway retry loops.

---

### Observability

Track retry metrics explicitly:

- retry rate
- dependency error rate
- request amplification factor

Observability helps engineers detect retry storms early.

---

## Key Takeaway

Retry storms are a classic distributed systems failure pattern where **reliability mechanisms become the source of instability**.

Retries should always be implemented carefully with:

- exponential backoff
- jitter
- circuit breakers
- retry limits

Without these protections, retries can quickly transform a minor outage into a **major production incident**.