# SQL Injection (SQLi)

[← Back to index](../README.md)

SQL injection happens when user input is inserted directly into a SQL query, letting an attacker change the query's meaning.

## Concept example
Vulnerable code:
```php
$query = "SELECT * FROM users WHERE id = '$id'";
```
If `$id` is `1' OR '1'='1`, the query becomes:
```sql
SELECT * FROM users WHERE id = '1' OR '1'='1';
```
The condition is always true, so all rows are returned.

## Types
- **In-band (error/union-based):** results visible in the response.
- **Blind (boolean/time-based):** inferred from app behavior.
- **Out-of-band:** data exfiltrated through another channel.

## Impact
Data theft (confidentiality), data modification or deletion (integrity), and sometimes server compromise.

## Prevention
1. **Parameterized queries / prepared statements** (primary defense)
2. Allow-list input validation
3. Least-privilege database accounts
4. Hide detailed database errors
5. Use ORMs and stored procedures correctly

Safe version:
```php
$stmt = $pdo->prepare("SELECT * FROM users WHERE id = ?");
$stmt->execute([$id]);
```

## Related
[DVWA SQL Injection Lab](../06_Laboratory_Activities/DVWA_SQL_Injection_Lab.md)

## My Reflection
I learned that SQL injection happens when an application handles user input insecurely and allows unintended SQL commands to affect database queries. Through our DVWA SQL Injection activity, I became more familiar with how this vulnerability can be tested in a controlled environment. I also learned that different security levels can change how the application handles input. This activity helped me understand the importance of prepared statements, parameterized queries, and proper input handling to protect databases.

## Review Questions
1. Why do prepared statements stop SQL injection?
2. Which CIA goals can SQLi violate?
3. How is blind SQLi different from error-based?
