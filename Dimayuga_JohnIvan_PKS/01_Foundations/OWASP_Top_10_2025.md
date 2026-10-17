# OWASP Top 10 (2025)

[← Back to index](../README.md)

OWASP publishes a ranked list of the most critical web application security risks.

> Verify names and order against the course deck, since categories are renamed and reordered between editions.

| # | Category | Summary |
|---|---|---|
| A01 | Broken Access Control | Users can act outside their permissions (e.g., viewing others' data) |
| A02 | Security Misconfiguration | Default credentials, open services, unsafe settings |
| A03 | Software Supply Chain Failures | Compromised libraries, dependencies, or build pipelines |
| A04 | Cryptographic Failures | Weak or missing encryption, poor key handling |
| A05 | Injection | Untrusted input interpreted as commands or queries (SQLi, command injection, XSS) |
| A06 | Insecure Design | Flaws in the design itself, not just coding bugs |
| A07 | Authentication Failures | Weak login, no MFA, session problems |
| A08 | Software or Data Integrity Failures | Unverified updates or data |
| A09 | Security Logging and Alerting Failures | Attacks go unnoticed |
| A10 | Mishandling of Exceptional Conditions | Poor error handling leaks information or creates weaknesses |

## Focus in this course
- A05 Injection → [SQL Injection](../05_Web_Application_Security/SQL_Injection.md) and [Command Injection](../05_Web_Application_Security/Command_Injection.md)

## My Reflection
I learned about common and important web application security risks, including broken access control, injection vulnerabilities, and security misconfigurations. These vulnerabilities can expose sensitive information and affect the reliability of an application. Studying the OWASP Top 10 helped me understand the importance of identifying risks and applying proper security measures. I realized that developers should test their applications regularly and follow secure coding practices to reduce potential attacks.

## Review Questions
1. Which category covers SQL injection?
2. How is Insecure Design different from a coding bug?
3. Why does missing logging matter even if it does not cause an attack?
