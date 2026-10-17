# Command Injection

[← Back to index](../README.md)

Command injection occurs when an application passes user input to an operating-system shell without proper validation, so an attacker can add their own commands.

## Concept example
An app that pings a user-supplied address:
```php
shell_exec("ping -c 4 " . $ip);
```
If the input includes a command separator followed by another command, the server runs both.

## Common separators
`;`  `&&`  `||`  `|` (behavior differs slightly between Linux and Windows)

## Impact
Reading files, running arbitrary commands, full server compromise: affects confidentiality, integrity, and availability.

## Prevention
1. Avoid calling OS commands; use built-in language functions.
2. Allow-list validation (e.g., accept only valid IP addresses).
3. Escape arguments (e.g., `escapeshellarg`).
4. Run the app with a low-privilege account.

## SQLi vs command injection
| | SQL Injection | Command Injection |
|---|---|---|
| Target | Database | Operating system |
| Cause | Input in SQL query | Input in shell command |
| Main defense | Prepared statements | Avoid shell / allow-list |

## My Reflection
I learned that command injection occurs when an application allows user input to influence operating system commands in an unsafe way. This can allow an attacker to execute commands that were not intended by the developer. The lesson helped me understand why applications should avoid directly passing untrusted input to system commands. I also learned that validating input and using safer programming methods can reduce the risk of this vulnerability.

## Review Questions
1. What causes command injection?
2. Why is allow-list validation better than block-list?
3. Why does least privilege reduce the damage?
