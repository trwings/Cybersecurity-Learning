# Phase 1 — Cybersecurity Fundamentals Revision

## 1. Cybersecurity

Cybersecurity is the practice of protecting digital systems, networks, devices, applications, and information from unauthorized access, misuse, disruption, modification, destruction, and theft.

---

# 2. Important Security Terms

### Asset

Something valuable that needs protection.

### Threat

Something capable of causing harm.

### Threat Actor

A person or group capable of carrying out malicious activity.

### Vulnerability

A weakness that can potentially be exploited.

### Exploit

A technique or method used to take advantage of a vulnerability.

### Attack

An attempt to compromise a system or resource.

### Risk

The possibility of loss or harm.

### Impact

The consequence of a security event.

---

# 3. Security Relationship

```text
Threat
   +
Vulnerability
   ↓
Risk

Exploit
   ↓
Attack
   ↓
Impact
```

---

# 4. CIA Triad

```text
C = Confidentiality
I = Integrity
A = Availability
```

### Confidentiality

Prevent unauthorized access to information.

### Integrity

Ensure information remains accurate and is not improperly modified.

### Availability

Ensure authorized users can access systems and information when required.

---

# 5. Authentication

Authentication answers:

> Who are you?

Examples:

* Password
* PIN
* Fingerprint
* Security key
* Authentication app

---

# 6. Authorization

Authorization answers:

> What are you allowed to do?

Example:

```text
Authentication
      ↓
Identity verified
      ↓
Authorization
      ↓
Permissions checked
      ↓
Access granted/denied
```

---

# 7. Authentication Factors

### Something You Know

Password/PIN.

### Something You Have

Security key/token/device.

### Something You Are

Fingerprint/face.

Other contextual factors can include:

* Somewhere you are
* Something you do

---

# 8. MFA

Multi-Factor Authentication uses multiple different authentication factors.

Example:

```text
Password
+
Authenticator code
```

---

# 9. Least Privilege

Users and systems should receive only the permissions required for their tasks.

---

# 10. Privilege Escalation

### Vertical

Lower privilege → higher privilege.

### Horizontal

One user → another user's resources at a similar privilege level.

---

# 11. Encryption

Encryption protects confidentiality by transforming plaintext into ciphertext using cryptographic algorithms and keys.

```text
Plaintext
 ↓
Encryption
 ↓
Ciphertext
```

---

# 12. Symmetric Encryption

Uses the same secret key for encryption and decryption.

Example:

```text
AES
```

---

# 13. Asymmetric Cryptography

Uses a public/private key pair.

Examples:

```text
RSA
ECC
```

---

# 14. Hashing

Hashing produces a digest from input data.

Examples:

```text
SHA-256
SHA-512
SHA-3
```

Dedicated password-hashing algorithms include:

```text
Argon2
bcrypt
scrypt
```

---

# 15. Encoding

Encoding changes data representation.

Example:

```text
Base64
```

Encoding does not provide confidentiality.

---

# 16. The Three-Way Difference

```text
Encryption
→ Confidentiality
→ Reversible with appropriate key

Hashing
→ Digest / integrity / password verification
→ Designed to be one-way

Encoding
→ Representation / compatibility
→ Usually reversible
```

---

# 17. Malware

Malware means malicious software.

Examples:

* Virus
* Worm
* Trojan
* Ransomware
* Spyware
* Rootkit

---

# 18. Phishing

Phishing uses deceptive communication to trick victims into:

* Revealing information
* Clicking malicious links
* Opening malicious attachments
* Visiting fraudulent websites

---

# 19. Social Engineering

Social engineering attacks human behavior instead of relying only on technical vulnerabilities.

---

# 20. Password Attacks

### Brute Force

Trying many possible passwords.

### Dictionary Attack

Trying words/passwords from a list.

### Credential Stuffing

Using leaked credentials against other services.

### Password Spraying

Trying common passwords against many accounts.

---

# 21. DoS and DDoS

### DoS

Attempts to make a service unavailable.

### DDoS

A distributed attack involving multiple sources.

---

# 22. Zero-Day

A zero-day vulnerability is a vulnerability for which defenders may not yet have an available fix or may not yet know about it.

---

# 23. Security Controls

### Preventive

Try to prevent incidents.

Examples:

* MFA
* Firewall
* Access control

### Detective

Identify suspicious activity.

Examples:

* IDS
* SIEM
* Log monitoring

### Corrective

Help restore or correct systems.

Examples:

* Recovery
* System restoration
* Malware removal

---

# 24. Defense in Depth

Use multiple security layers instead of depending on a single control.

```text
Authentication
      ↓
MFA
      ↓
Firewall
      ↓
Endpoint Protection
      ↓
Logging
      ↓
Monitoring
      ↓
Incident Response
```

---

# 25. Offensive vs Defensive Security

### Offensive Security

Finds and demonstrates weaknesses through authorized testing.

### Defensive Security

Protects systems and detects/responds to attacks.

---

# 26. Red Team vs Blue Team

| Red Team                    | Blue Team           |
| --------------------------- | ------------------- |
| Simulates attackers         | Defends systems     |
| Finds weaknesses            | Detects attacks     |
| Performs authorized attacks | Investigates alerts |
| Tests defenses              | Improves defenses   |

---

# 27. Important Questions

Before moving forward, you should be able to answer these without looking at your notes:

1. What is cybersecurity?
2. What is an asset?
3. What is a threat?
4. What is a threat actor?
5. What is a vulnerability?
6. What is an exploit?
7. What is an attack?
8. What is risk?
9. What is impact?
10. Explain the CIA Triad.
11. What is confidentiality?
12. What is integrity?
13. What is availability?
14. What is authentication?
15. What is authorization?
16. What is MFA?
17. What is least privilege?
18. What is privilege escalation?
19. What is encryption?
20. What is hashing?
21. What is encoding?
22. Difference between encryption and hashing?
23. Difference between hashing and encoding?
24. What is symmetric encryption?
25. What is asymmetric cryptography?
26. What are public and private keys?
27. What is a digital signature?
28. What is malware?
29. What is phishing?
30. What is social engineering?
31. What is brute force?
32. What is credential stuffing?
33. What is password spraying?
34. What is DoS?
35. What is DDoS?
36. What is a zero-day?
37. What is defense in depth?
38. What is a security control?
39. What is offensive security?
40. What is defensive security?
41. What is a red team?
42. What is a blue team?

---

# Phase 1 Completion Standard

You should not merely memorize definitions.

You should be able to explain each concept in your own words and give a simple example.

For example, you should be able to explain:

> "A vulnerability is a weakness. An exploit is the technique used to take advantage of that weakness. A threat is something capable of causing harm, while risk represents the potential for loss or harm."

You should also be able to distinguish:

```text
Threat ≠ Vulnerability ≠ Exploit

Authentication ≠ Authorization

Encryption ≠ Hashing ≠ Encoding

Confidentiality ≠ Integrity ≠ Availability
```

---

# Phase 1 Final Mental Model

```text
                    CYBERSECURITY
                         │
          ┌──────────────┼──────────────┐
          │              │              │
       OFFENSIVE      DEFENSIVE      GOVERNANCE
          │              │
     Find Weaknesses   Protect Systems
          │              │
       Red Team        Blue Team
          │              │
          └───────┬──────┘
                  │
             FUNDAMENTALS
                  │
      ┌───────────┼────────────┐
      │           │            │
     CIA      Identity      Threats
      │        & Access        │
      │           │            │
      └───────────┼────────────┘
                  │
       Encryption / Hashing
          / Encoding
                  │
            Risk & Security
              Controls
```

---

# Phase 1 Goal

After completing this phase, you should have a basic understanding of how cybersecurity works and be ready to move into deeper technical foundations such as networking, operating systems, Linux, Windows, web technologies, and security tooling.
