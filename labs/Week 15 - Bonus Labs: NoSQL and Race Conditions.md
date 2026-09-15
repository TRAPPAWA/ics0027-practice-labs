# Week 15 - Bonus Labs: NoSQL and Race Conditions

There is no normal practical session. The labs are therefore completed as self-study.

## Labs

1. **Apprentice: Detecting NoSQL injection**
   https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-detection

2. **Apprentice: Exploiting NoSQL operator injection to bypass authentication**
   https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-bypass-authentication

3. **Practitioner: Exploiting NoSQL injection to extract data**
   https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-extract-data

4. **Practitioner: Exploiting NoSQL operator injection to extract unknown fields**
   https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-extract-unknown-fields

5. **Apprentice: Limit overrun race conditions**
   https://portswigger.net/web-security/race-conditions/lab-race-conditions-limit-overrun

6. **Practitioner: Bypassing rate limits via race conditions**
   https://portswigger.net/web-security/race-conditions/lab-race-conditions-bypassing-rate-limits

7. **Practitioner: Multi-endpoint race conditions**
   https://portswigger.net/web-security/race-conditions/lab-race-conditions-multi-endpoint

8. **Practitioner: Single-endpoint race conditions**
   https://portswigger.net/web-security/race-conditions/lab-race-conditions-single-endpoint

## Useful learning paths

**NoSQL injection**: https://portswigger.net/web-security/learning-paths/nosql-injection

**Race conditions**: https://portswigger.net/web-security/learning-paths/race-conditions

## Quick reference

NoSQL injection does not necessarily use SQL syntax.

For JSON-based APIs, pay attention to whether a value expected to be a string can be replaced by an object or operator.

Conceptually:

```json
{
  "username": "value"
}
```

may behave very differently from:

```json
{
  "username": {
    "operator": "value"
  }
}
```

The exact operator syntax depends on the backend and the lab.
