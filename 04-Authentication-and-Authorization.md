# Authentication and Authorization

## 1. Introduction

Authentication and authorization are fundamental concepts in cybersecurity and identity management.

They are often confused.

The easiest way to remember the difference is:

> **Authentication = Who are you?**

> **Authorization = What are you allowed to do?**

---

# 2. Authentication

Authentication is the process of verifying the identity of a user, device, or system.

Example:

You enter:

```text
Username: ali
Password: ********
```

The system checks whether the credentials are valid.

If they are valid, your identity is authenticated.

---

# 3. Authentication Factors

Authentication factors are commonly divided into categories.

## Something You Know

Information known by the user.

Examples:

* Password
* PIN
* Security question

## Something You Have

Something physically possessed by the user.

Examples:

* Security key
* Smartphone
* Authentication token
* Smart card

## Something You Are

A biometric characteristic.

Examples:

* Fingerprint
* Face
* Iris

## Somewhere You Are

Location can sometimes be used as an additional contextual factor.

Example:

* Access allowed only from an approved location.

## Something You Do

Behavioral characteristics.

Examples:

* Typing behavior
* Mouse movement patterns
* Other behavioral biometrics

---

# 4. Multi-Factor Authentication

**Multi-Factor Authentication (MFA)** uses multiple authentication factors.

Example:

```text
Password
   +
Authenticator app code
```

The attacker would need more than just the password.

Important:

> Two passwords are not necessarily two different authentication factors.

Two factors should normally come from different factor categories.

---

# 5. Password Security

Passwords should be:

* Long
* Unique
* Difficult to guess
* Not reused across important accounts

Organizations can improve password security with:

* Password policies
* Password managers
* MFA
* Rate limiting
* Account lockout/risk controls
* Secure password storage

---

# 6. Password Storage

Applications should not store user passwords as plain text.

Instead, passwords should be processed using appropriate password-hashing mechanisms.

Password storage commonly involves:

* Password hashing
* Unique salts
* Appropriate password-hashing algorithms

Examples of password-hashing algorithms include:

* Argon2
* bcrypt
* scrypt

---

# 7. Authorization

Authorization determines what an authenticated identity is allowed to access or perform.

Example:

A university system may have:

```text
Student
   ↓
View own marks

Teacher
   ↓
View and update assigned marks

Administrator
   ↓
Manage users and system settings
```

All three users may authenticate successfully.

Their permissions are different.

---

# 8. Authentication vs Authorization

| Authentication                  | Authorization                     |
| ------------------------------- | --------------------------------- |
| Verifies identity               | Determines permissions            |
| "Who are you?"                  | "What can you do?"                |
| Happens before access decisions | Depends on identity/permissions   |
| Uses credentials/factors        | Uses roles, permissions, policies |

---

# 9. Example

Suppose you log into GitHub.

### Authentication

GitHub verifies that you are the account owner.

### Authorization

GitHub determines what you can do.

For example:

* View repositories
* Create repositories
* Modify repositories you can write to
* Manage repository settings if you have permission

---

# 10. Access Control

Access control determines who or what can access resources and under which conditions.

Common models include:

### DAC — Discretionary Access Control

The resource owner can control access.

### MAC — Mandatory Access Control

Access decisions are based on centrally defined security classifications/policies.

### RBAC — Role-Based Access Control

Permissions are assigned according to roles.

Example:

```text
Admin → Full management permissions

Teacher → Teaching-related permissions

Student → Student-related permissions
```

### ABAC — Attribute-Based Access Control

Access decisions use attributes.

Possible attributes include:

* User
* Role
* Device
* Location
* Resource
* Time
* Security conditions

---

# 11. Least Privilege

The principle of **least privilege** means users and systems should receive only the permissions necessary to perform their required tasks.

Example:

A student does not need administrator access to a university server.

Least privilege reduces the potential damage caused by:

* Compromised accounts
* Insider misuse
* Malware
* Human mistakes

---

# 12. Privilege Escalation

Privilege escalation occurs when an attacker or user gains higher privileges than they should have.

Two common categories:

### Vertical Privilege Escalation

A lower-privileged user gains higher privileges.

Example:

```text
Normal user
     ↓
Administrator
```

### Horizontal Privilege Escalation

A user accesses another user's resources at a similar privilege level.

Example:

```text
User A
  ↓
Accesses User B's account data
```

---

# 13. Session Management

After authentication, applications commonly create a session so the user does not need to authenticate on every request.

Sessions may use:

* Session cookies
* Session identifiers
* Tokens

Poor session management can lead to security problems.

Important security practices include:

* Secure cookie settings
* Appropriate session expiration
* Session invalidation after logout
* Protection against session theft

---

# 14. Identity

An identity represents an entity that can be recognized by a system.

Entities may include:

* Human users
* Organizations
* Devices
* Applications
* Services

---

# 15. Identity and Access Management

**Identity and Access Management (IAM)** is the discipline of managing digital identities and their access.

IAM commonly involves:

* Identity creation
* Authentication
* Authorization
* Access provisioning
* Access reviews
* Account lifecycle management
* Deprovisioning

---

# 16. Authentication and Authorization Example

Imagine a company employee.

```text
Employee
   ↓
Enters username + password
   ↓
Authentication
   ↓
Identity verified
   ↓
Authorization check
   ↓
Permissions determined
   ↓
Access granted/denied
```

---

# 17. Common Authentication Problems

Examples:

* Weak passwords
* Password reuse
* Credential theft
* Phishing
* Missing MFA
* Poor session management
* Insecure password storage

---

# 18. Common Authorization Problems

Examples:

* Excessive permissions
* Broken access control
* Missing authorization checks
* Incorrect role assignment
* Direct object access without proper authorization

---

# 19. Important Difference

Remember:

```text
Authentication
      ↓
Identity verification

Authorization
      ↓
Permission decision
```

A user can be successfully authenticated but still not be authorized to access a particular resource.

---

## Key Terms

```text
Authentication
Authorization
MFA
Password
Biometrics
Authentication Factor
Access Control
DAC
MAC
RBAC
ABAC
Least Privilege
Privilege Escalation
Session
Identity
IAM
Vertical Privilege Escalation
Horizontal Privilege Escalation
```
