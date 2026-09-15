# Week 2 - Introduction, OWASP Top 10, and Burp Orientation

## Session goals

- Understand the role of vulnerability classes and the OWASP Top 10.
- Become familiar with Burp Proxy, HTTP history, and Repeater.
- Identify where user-controlled data appears in HTTP requests.
- Practise distinguishing a vulnerability, an exploit, an impact, and a mitigation.

## Practical work

1. OWASP Top 10 group exercise.
2. Configure Burp Suite and browser proxying.

## PortSwigger orientation sampler - 8 labs

1. **SQL injection vulnerability allowing login bypass**  
   https://portswigger.net/web-security/sql-injection/lab-login-bypass

2. **Reflected XSS into HTML context with nothing encoded**  
   https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded

3. **CSRF vulnerability with no defenses**  
   https://portswigger.net/web-security/csrf/lab-no-defenses

4. **File path traversal, simple case**  
   https://portswigger.net/web-security/file-path-traversal/lab-simple

5. **Unprotected admin functionality**  
   https://portswigger.net/web-security/access-control/lab-unprotected-admin-functionality

6. **OS command injection, simple case**  
   https://portswigger.net/web-security/os-command-injection/lab-simple

7. **Basic SSRF against the local server**  
   https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-localhost

8. **Source code disclosure via backup files**  
   https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-via-backup-files

## Quick reference

Common HTTP request structure:

```http
GET /account?id=123 HTTP/1.1
Host: example.test
Cookie: session=...
User-Agent: ...
```

Useful places to inspect in Burp:
- **Proxy → HTTP history**
- **Send to Repeater**
- **Repeater → Send**
- request method and path;
- query parameters;
- request body;
- `Host`;
- `Cookie`;
- `Origin`;
- `Referer`;
- `Content-Type`.

When testing, change **one thing at a time**. Otherwise you eventually discover that something broke, while learning absolutely nothing about which change broke it.
