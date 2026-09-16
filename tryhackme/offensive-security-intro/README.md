TryHackMe — Offensive Security Intro

1 - Overview

Platform: TryHackMe
Room: Offensive Security Intro
Category: Offensive Security / Web
Difficulty: Beginner

Objective

Identify and exploit a vulnerability in the simulated FakeBank web application.

---

2 - Target

Target application:

http://fakebank.thm

All activities were performed exclusively within the authorized TryHackMe laboratory environment.

---

3 - Reconnaissance

The first step was to identify resources available on the target web application.

The tool DIRB was used to perform directory enumeration.

Command

dirb http://fakebank.thm

Result

The enumeration identified the following resources:

http://fakebank.thm/bank-transfer
http://fakebank.thm/image

Evidence

screenshots/01-dirb.jpeg

---

4 - Endpoint Analysis

The "/bank-transfer" endpoint was investigated because its name indicated a potentially sensitive financial function.

URL:

http://fakebank.thm/bank-transfer

The endpoint exposed an Admin Portal containing functionality for performing bank transfers.

Evidence

screenshots/03-bank-transfer.jpeg

---

5 - Exploitation

The application initially displayed a negative account balance:

-$1,232.32

The discovered administrative functionality allowed a transfer to be created.

A transfer of:

$5,000.00

was performed to my own account within the laboratory.

The application accepted the operation and the account balance was modified.

Evidence

The platform hasn't updated; it's probably a bug.

---

6 - Attack Chain

The complete attack path was:

Directory Enumeration
        ↓
Endpoint Discovery
        ↓
/bank-transfer
        ↓
Admin Portal
        ↓
Transfer Functionality
        ↓
Successful Transaction

---

7 - Security Analysis

The exercise demonstrates the importance of properly protecting administrative functionality.

The administrative endpoint was discoverable through directory enumeration and exposed functionality capable of modifying financial data.

The key security concepts demonstrated were:

-Attack surface discovery
-Directory enumeration
-Endpoint discovery
-Administrative functionality exposure
-Access control
-Impact analysis

---

8 - Impact

In a real-world application, unauthorized access to a financial transfer function could potentially result in:

-Unauthorized transactions
-Financial loss
-Modification of financial records
-Compromise of data integrity

The activity described in this write-up was limited to the authorized TryHackMe laboratory.

---

9 - Mitigation

Potential security controls include:

-Strong authentication for administrative functions
-Proper authorization and role-based access control
-Server-side validation of financial operations
-Restriction of administrative endpoints
-Logging and monitoring of sensitive transactions
-Separation of administrative and standard user functionality

Hiding an administrative URL is not, by itself, a security control.

---

10 - Lessons Learned

This room introduced the basic workflow of a web security assessment:

Reconnaissance
      ↓
Enumeration
      ↓
Discovery
      ↓
Analysis
      ↓
Exploitation
      ↓
Impact
      ↓
Mitigation

The main lesson was that functionality not exposed through the application's visible interface may still be accessible through directly discoverable endpoints.

---

11 - Tools

| Tool     | Purpose                              |
| -------- | ------------------------------------ |
| DIRB     | Directory and resource enumeration   |
| Browser  | Application analysis and interaction |
| Terminal | Command execution                    |

---

12 - Status

Room completed.

This write-up documents the methodology, commands, findings, evidence, impact, and security considerations observed during the laboratory exercise.
