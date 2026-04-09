# Pattern: Expired Certificate

## Description

Expired Certificate failures occur when TLS/SSL certificates used for secure communication reach their expiration date.

Once expired, clients will refuse secure connections, causing services that rely on HTTPS or TLS communication to fail.

This often causes sudden outages despite the underlying service being healthy.

---

## Typical Symptoms

Engineers may observe:

TLS handshake failures
Connection refusal errors
Authentication errors
Clients unable to establish HTTPS connections
Sudden API failures

---

## Common Misleading Signals

The issue may appear as:

Network connectivity issues
Authentication service failure
API gateway outage

However, the underlying cause is often an expired SSL/TLS certificate.

---

## Likely Root Causes

Typical causes include:

Missed certificate renewal
Automated renewal failures
Manual certificate deployment errors
Incorrect certificate chain

---

## First Checks

Engineers should check:

Certificate expiration dates
TLS handshake logs
Certificate renewal automation
Reverse proxy configurations

---

## Useful Signals

Look for:

TLS errors in logs
Certificate validation failures
SSL handshake metrics
Gateway error responses

---

## Prevention

**Automated Certificate Renewal**
Use systems like Let's Encrypt automation.

**Expiry Monitoring**
Alert well before certificate expiration.

**Certificate Management Systems**
Centralize certificate tracking.

---

<a href="../../categories/dependency/dependency.md" style="min-width:260px; border:1px solid #e5e7eb; border-radius:8px; padding:12px; text-decoration:none;">**<<Back**</a>