# Burp Suite and DVWA Setup

[← Back to index](../README.md)

- **DVWA (Damn Vulnerable Web Application):** an intentionally vulnerable app for legal practice.
- **Burp Suite:** an intercepting proxy for inspecting and modifying HTTP traffic.

> Use only on my own lab. Never test systems without permission.

## DVWA setup (general)
1. Install a web server, PHP, and MySQL/MariaDB (e.g., XAMPP, Docker, or a VM).
2. Place DVWA in the web root.
3. Configure database credentials in the DVWA config file.
4. Open `setup.php` and click **Create / Reset Database**.
5. Log in with the default credentials.
6. Set the **DVWA Security** level (Low, Medium, High, Impossible).

## Burp Suite setup
1. Open Burp → Proxy → Intercept.
2. Use Burp's built-in browser, or set the browser proxy to `127.0.0.1:8080`.
3. Turn Intercept on and load a DVWA page.
4. Forward, drop, or send the request to Repeater.

## Key Burp tools
| Tool | Purpose |
|---|---|
| Proxy | Intercept requests/responses |
| Repeater | Edit and resend manually |
| Intruder | Automate payloads |
| Decoder | Encode/decode data |

## My Reflection
I learned that Burp Suite is a useful tool for inspecting and testing web application traffic, while DVWA provides a deliberately vulnerable application for security practice. Setting up a testing environment requires proper configuration and troubleshooting. This lesson helped me understand how security professionals examine HTTP requests and identify possible weaknesses in web applications. I also learned that these tools should be used only in authorized testing environments.

## Review Questions
1. What does an intercepting proxy do?
2. Why is DVWA run in an isolated environment?
3. What is the difference between Repeater and Intruder?
