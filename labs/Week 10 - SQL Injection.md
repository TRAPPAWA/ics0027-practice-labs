# Week 10 - SQL Injection

## Labs

1. **Apprentice: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data**  
   https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data

2. **Apprentice: SQL injection vulnerability allowing login bypass**  
   https://portswigger.net/web-security/sql-injection/lab-login-bypass

3. **Practitioner: SQL injection UNION attack, determining the number of columns returned by the query**  
   https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns

4. **Practitioner: SQL injection UNION attack, finding a column containing text**  
   https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text

5. **Practitioner: SQL injection UNION attack, retrieving data from other tables**  
   https://portswigger.net/web-security/sql-injection/union-attacks/lab-retrieve-data-from-other-tables

6. **Practitioner: Blind SQL injection with conditional responses**  
   https://portswigger.net/web-security/sql-injection/blind/lab-conditional-responses

7. **Practitioner: SQL injection UNION attack, retrieving multiple values in a single column**  
   https://portswigger.net/web-security/sql-injection/union-attacks/lab-retrieve-multiple-values-in-single-column

8. **Practitioner: Visible error-based SQL injection**  
   https://portswigger.net/web-security/sql-injection/blind/lab-sql-injection-visible-error-based

9. **Practitioner: Blind SQL injection with time delays**  
   https://portswigger.net/web-security/sql-injection/blind/lab-time-delays

## Useful learning path

**SQL injection**: https://portswigger.net/web-security/learning-paths/sql-injection

## Quick reference

Common probes:

```text
'
''
' OR '1'='1
```

Comments vary by database. Common forms include:

```text
--
#
/* ... */
```

Determine column count with:

```sql
ORDER BY 1
ORDER BY 2
ORDER BY 3
```

or:

```sql
UNION SELECT NULL--
UNION SELECT NULL,NULL--
UNION SELECT NULL,NULL,NULL--
```

String concatenation is DBMS-specific.

Defence:
- parameterized queries / prepared statements;
- avoid string concatenation;
- constrain dynamic query structure;
- least-privilege database accounts.
