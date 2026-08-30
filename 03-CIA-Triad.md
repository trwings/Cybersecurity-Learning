# CIA Triad

## 1. Introduction

The **CIA Triad** is one of the fundamental models of cybersecurity.

CIA stands for:

* **Confidentiality**
* **Integrity**
* **Availability**

It provides a simple way to understand the primary security objectives for information and systems.

---

# 2. Confidentiality

Confidentiality means preventing unauthorized people from accessing information.

In simple words:

> **Only authorized people should be able to see the information.**

Examples:

* Only a student should access their academic records.
* Only authorized employees should access company data.
* Only authorized users should access a database.

---

# 3. Controls Used for Confidentiality

Examples include:

* Passwords
* Multi-factor authentication
* Access control
* Encryption
* File permissions
* Network segmentation
* Data classification

---

# 4. Confidentiality Example

Suppose a hospital stores patient records.

If an unauthorized person accesses patient information:

```text
Unauthorized access
       ↓
Confidentiality compromised
```

---

# 5. Integrity

Integrity means maintaining the accuracy, consistency, and trustworthiness of information.

In simple words:

> **Data should not be changed improperly.**

Example:

A student's marks are:

```text
Original:
85
```

If an unauthorized person changes them to:

```text
95
```

the integrity of the data has been compromised.

---

# 6. Controls Used for Integrity

Examples:

* Access controls
* File permissions
* Hashing
* Digital signatures
* Audit logs
* Version control
* Input validation
* Database constraints

---

# 7. Availability

Availability means authorized users should be able to access systems and information when needed.

Example:

An online banking service should be available to legitimate customers.

If an attack causes the service to become unavailable:

```text
Service unavailable
       ↓
Availability compromised
```

---

# 8. Controls Used for Availability

Examples:

* Backups
* Redundant systems
* Load balancing
* Failover systems
* Disaster recovery
* DDoS protection
* Monitoring
* Capacity planning

---

# 9. CIA Triad Example

Imagine an online banking system.

### Confidentiality

Only authorized customers should see account information.

### Integrity

Account balances and transactions must not be modified improperly.

### Availability

Customers should be able to access banking services when needed.

All three are important.

---

# 10. CIA and Common Attacks

| Security Objective | Example Violation         |
| ------------------ | ------------------------- |
| Confidentiality    | Data theft                |
| Integrity          | Unauthorized modification |
| Availability       | DDoS                      |
| Confidentiality    | Credential theft          |
| Integrity          | Database manipulation     |
| Availability       | Service outage            |

---

# 11. Confidentiality vs Integrity

These are commonly confused.

### Confidentiality

Asks:

> "Who can see the information?"

### Integrity

Asks:

> "Has the information been changed incorrectly?"

Example:

If someone reads your private document:

**Confidentiality is compromised.**

If someone modifies your private document:

**Integrity is compromised.**

---

# 12. Integrity vs Availability

### Integrity

The information must remain correct.

### Availability

The information/service must remain accessible.

Example:

A database can be:

* Available but incorrect.
* Correct but unavailable.

Therefore, these are separate security objectives.

---

# 13. CIA Triad in Real Life

Consider an ATM.

### Confidentiality

Only the authorized account holder should access account information.

### Integrity

The account balance and transaction records must remain accurate.

### Availability

The ATM/banking service should be operational when customers need it.

---

# 14. Beyond the CIA Triad

CIA is fundamental, but modern security discussions often consider additional properties.

Examples:

### Authenticity

Ensuring that an entity or piece of information is genuine.

### Accountability

Being able to associate actions with responsible identities.

### Non-repudiation

Providing evidence that can help prevent an involved party from falsely denying an action.

These concepts complement the CIA Triad.

---

# 15. CIA Risk Analysis

When analyzing a system, ask:

### Confidentiality

What happens if this information is exposed?

### Integrity

What happens if this information is modified?

### Availability

What happens if this system becomes unavailable?

This is a useful beginner security-analysis technique.

---

# 16. CIA Quick Memory Trick

Remember:

```text
C = Can unauthorized people SEE it?
I = Is the information CORRECT?
A = Can authorized people ACCESS it?
```

---

## Key Terms

```text
CIA Triad
Confidentiality
Integrity
Availability
Authenticity
Accountability
Non-repudiation
Access Control
Encryption
Hashing
Digital Signature
Backup
Redundancy
Disaster Recovery
```
