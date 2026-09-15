# ICS0027 Web Application Security

## PortSwigger Web Security Academy - Required Lab List

Complete **50 PortSwigger Web Security Academy labs** during the semester.

Difficulty labels:

* **Apprentice:** introductory
* **Practitioner:** intermediate
* **Expert:** advanced

---

## 1. HTTP, Origins, and Browser Trust - 3 labs

1. **Apprentice: Host header authentication bypass**  
   https://portswigger.net/web-security/host-header/exploiting/lab-host-header-authentication-bypass

2. **Apprentice: CORS vulnerability with basic origin reflection**  
   https://portswigger.net/web-security/cors/lab-basic-origin-reflection-attack

3. **Apprentice: CORS vulnerability with trusted null origin**  
   https://portswigger.net/web-security/cors/lab-null-origin-whitelisted-attack

---

## 2. Client-Side Controls and DOM Behaviour - 3 labs

4. **Apprentice: Excessive trust in client-side controls**  
   https://portswigger.net/web-security/logic-flaws/examples/lab-logic-flaws-excessive-trust-in-client-side-controls

5. **Practitioner: DOM-based open redirection**  
   https://portswigger.net/web-security/dom-based/open-redirection/lab-dom-open-redirection

6. **Practitioner: DOM-based cookie manipulation**  
   https://portswigger.net/web-security/dom-based/cookie-manipulation/lab-dom-cookie-manipulation

---

## 3. Cross-Site Scripting (XSS) - 5 labs

7. **Apprentice: Reflected XSS into HTML context with nothing encoded**  
   https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded

8. **Apprentice: Stored XSS into HTML context with nothing encoded**  
   https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded

9. **Apprentice: DOM XSS in `document.write` sink using source `location.search`**  
   https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-document-write-sink

10. **Apprentice: DOM XSS in `innerHTML` sink using source `location.search`**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-innerhtml-sink

11. **Practitioner: Reflected DOM XSS**  
    https://portswigger.net/web-security/cross-site-scripting/dom-based/lab-dom-xss-reflected

---

## 4. Authentication and Session Security - 4 labs

12. **Apprentice: Username enumeration via different responses**  
    https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses

13. **Apprentice: 2FA simple bypass**  
    https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-simple-bypass

14. **Apprentice: Password reset broken logic**  
    https://portswigger.net/web-security/authentication/other-mechanisms/lab-password-reset-broken-logic

15. **Practitioner: Brute-forcing a stay-logged-in cookie**  
    https://portswigger.net/web-security/authentication/other-mechanisms/lab-brute-forcing-a-stay-logged-in-cookie

---

## 5. Backend Components, Files, and Server-Side Attacks - 8 labs

16. **Apprentice: File path traversal, simple case**  
    https://portswigger.net/web-security/file-path-traversal/lab-simple

17. **Practitioner: File path traversal, traversal sequences stripped non-recursively**  
    https://portswigger.net/web-security/file-path-traversal/lab-sequences-stripped-non-recursively

18. **Practitioner: File path traversal, validation of file extension with null byte bypass**  
    https://portswigger.net/web-security/file-path-traversal/lab-validate-file-extension-null-byte-bypass

19. **Apprentice: OS command injection, simple case**  
    https://portswigger.net/web-security/os-command-injection/lab-simple

20. **Practitioner: Blind OS command injection with time delays**  
    https://portswigger.net/web-security/os-command-injection/lab-blind-time-delays

21. **Apprentice: Remote code execution via web shell upload**  
    https://portswigger.net/web-security/file-upload/lab-file-upload-remote-code-execution-via-web-shell-upload

22. **Apprentice: Web shell upload via Content-Type restriction bypass**  
    https://portswigger.net/web-security/file-upload/lab-file-upload-web-shell-upload-via-content-type-restriction-bypass

23. **Apprentice: Basic SSRF against the local server**  
    https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-localhost

---

## 6. Access Control and IDOR - 4 labs

24. **Apprentice: Unprotected admin functionality**  
    https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality

25. **Apprentice: User role controlled by request parameter**  
    https://portswigger.net/web-security/access-control/lab-user-role-controlled-by-request-parameter

26. **Apprentice: Insecure direct object references**  
    https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references

27. **Practitioner: Method-based access control can be circumvented**  
    https://portswigger.net/web-security/access-control/lab-method-based-access-control-can-be-circumvented

---

## 7. SQL Injection - 6 labs

28. **Apprentice: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data**  
    https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data

29. **Apprentice: SQL injection vulnerability allowing login bypass**  
    https://portswigger.net/web-security/sql-injection/lab-login-bypass

30. **Practitioner: SQL injection UNION attack, determining the number of columns returned by the query**  
    https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns

31. **Practitioner: SQL injection UNION attack, finding a column containing text**  
    https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text

32. **Practitioner: SQL injection UNION attack, retrieving data from other tables**  
    https://portswigger.net/web-security/sql-injection/union-attacks/lab-retrieve-data-from-other-tables

33. **Practitioner: Blind SQL injection with conditional responses**  
    https://portswigger.net/web-security/sql-injection/blind/lab-conditional-responses

---

## 8. Cross-Site Request Forgery (CSRF) - 4 labs

34. **Apprentice: CSRF vulnerability with no defenses**  
    https://portswigger.net/web-security/csrf/lab-no-defenses

35. **Practitioner: CSRF where token validation depends on request method**  
    https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-validation-depends-on-request-method

36. **Practitioner: CSRF where token is not tied to user session**  
    https://portswigger.net/web-security/csrf/bypassing-token-validation/lab-token-not-tied-to-user-session

37. **Practitioner: SameSite Lax bypass via method override**  
    https://portswigger.net/web-security/csrf/bypassing-samesite-restrictions/lab-samesite-lax-bypass-via-method-override

---

## 9. Clickjacking / UI Redress - 3 labs

38. **Apprentice: Basic clickjacking with CSRF token protection**  
    https://portswigger.net/web-security/clickjacking/lab-basic-csrf-protected

39. **Apprentice: Clickjacking with form input data prefilled from a URL parameter**  
    https://portswigger.net/web-security/clickjacking/lab-prefilled-form-input

40. **Practitioner: Multistep clickjacking**  
    https://portswigger.net/web-security/clickjacking/lab-multistep

---

## 10. Information Disclosure and Web Caching - 3 labs

41. **Apprentice: Source code disclosure via backup files**  
    https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-via-backup-files

42. **Practitioner: Information disclosure in version control history**  
    https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-in-version-control-history

43. **Apprentice: Exploiting path mapping for web cache deception**  
    https://portswigger.net/web-security/web-cache-deception/lab-wcd-exploiting-path-mapping

---

## 11. API Security - 4 labs

44. **Apprentice: Exploiting an API endpoint using documentation**  
    https://portswigger.net/web-security/api-testing/lab-exploiting-api-endpoint-using-documentation

45. **Practitioner: Finding and exploiting an unused API endpoint**  
    https://portswigger.net/web-security/api-testing/lab-exploiting-unused-api-endpoint

46. **Practitioner: Exploiting a mass assignment vulnerability**  
    https://portswigger.net/web-security/api-testing/lab-exploiting-mass-assignment-vulnerability

47. **Expert: Exploiting server-side parameter pollution in a REST URL**  
    https://portswigger.net/web-security/api-testing/server-side-parameter-pollution/lab-exploiting-server-side-parameter-pollution-in-rest-url

---

## 12. NoSQL Injection - 3 labs

48. **Apprentice: Detecting NoSQL injection**  
    https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-detection

49. **Apprentice: Exploiting NoSQL operator injection to bypass authentication**  
    https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-bypass-authentication

50. **Practitioner: Exploiting NoSQL injection to extract data**  
    https://portswigger.net/web-security/nosql-injection/lab-nosql-injection-extract-data

---

## Completion

**Total required labs: 50**
