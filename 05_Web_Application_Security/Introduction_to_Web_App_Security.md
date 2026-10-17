# Introduction to Web Application Security

[← Back to index](../README.md)

## How a web app works
Browser (client) → HTTP/HTTPS request → web server → application logic → database → response.

## Core concepts
- **HTTP methods:** GET, POST, PUT, DELETE.
- **Status codes:** 200 OK, 302 redirect, 403 forbidden, 404 not found, 500 server error.
- **Cookies and sessions:** keep users logged in.
- **Authentication:** who you are. **Authorization:** what you may do.
- **Never trust user input:** form fields, URLs, headers, and cookies can all be manipulated.

## Common defenses
Input validation, output encoding, parameterized queries, least privilege, HTTPS, secure error handling, logging.

## Related notes
[OWASP Top 10](../01_Foundations/OWASP_Top_10_2025.md) · [SQL Injection](SQL_Injection.md) · [Command Injection](Command_Injection.md)

## My Reflection
I learned that web applications can have vulnerabilities that attackers may exploit if they are not properly developed and secured. Input validation, authentication, authorization, and secure coding practices are important for protecting applications. This lesson helped me understand why developers must consider security throughout the development process instead of treating it as a final step. It also prepared me for the hands-on activities involving DVWA and web application testing.

## Review Questions
1. Authentication vs authorization?
2. Why must server-side validation exist even if the browser validates input?
3. What does a 403 status mean?
