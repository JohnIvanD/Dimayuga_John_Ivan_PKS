# DVWA SQL Injection Lab

[← Back to index](../README.md)

> Perform only in my own DVWA lab.

## Objective
Understand how SQL injection works and how defenses differ across DVWA security levels.

## Environment
| Item | My setup |
|---|---|
| DVWA URL | http://localhost:4280/vulnerabilities/sqli/ |
| Security level | Low |
| Browser / Burp used | Firefox on Parrot OS (VirtualBox) |

## Procedure (general)
1. Log in to DVWA and open **SQL Injection**.
2. Set security to **Low**.
3. Test normal input and observe the output.
4. Observe how special characters change behavior.
5. Compare the page's source code with **View Source**.
6. Extension: repeat on Medium, High, and Impossible and compare the results.

## Observations by level
| Level | What I observed | Why it behaves this way |
|---|---|---|
| Low | The input `%' or '0'='0` returned all five user records (admin, Gordon Brown, Hack Me, Pablo Picasso, Bob Smith) instead of one. | The input is placed directly into the SQL query, so the injected condition is always true and every row matches. |
| Medium | Not tested in my lab | See the reference table below |
| High | Not tested in my lab | See the reference table below |
| Impossible | Not tested in my lab | See the reference table below |

## Screenshots
![DVWA SQL Injection result](../images/dvwa_sql_injection.png)

*Input `%' or '0'='0` in the User ID field returned all five user records (admin, Gordon Brown, Hack Me, Pablo Picasso, Bob Smith) instead of a single user.*

## Defense comparison (reference)
General design of the DVWA SQL Injection page at each level:

| Level | Handling |
|---|---|
| Low | User input is concatenated directly into the query, so it is vulnerable |
| Medium | Input comes from a dropdown and is escaped, but the query is still not parameterized |
| High | Input is entered on a separate page and the query is limited, which makes it harder but is not a real fix |
| Impossible | Uses prepared statements (parameterized queries) with an anti-CSRF token, which is the secure approach |

My hands-on test was done at **Low** only; the other levels are listed for comparison.

## My Reflection
In this laboratory activity, I learned how SQL injection vulnerabilities can affect a web application's database. Using DVWA helped me understand how different security settings influence the application's response to input. I also learned that observing the results carefully is important when documenting a security test. This activity improved my understanding of database security and the importance of using parameterized queries to prevent SQL injection.
