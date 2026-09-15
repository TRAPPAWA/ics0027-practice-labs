# Week 3 - HTTP, Headers, Origins, and Browser Trust

## Labs

1. **Apprentice: Host header authentication bypass**  
   https://portswigger.net/web-security/host-header/exploiting/lab-host-header-authentication-bypass

2. **Apprentice: CORS vulnerability with basic origin reflection**  
   https://portswigger.net/web-security/cors/lab-basic-origin-reflection-attack

3. **Apprentice: CORS vulnerability with trusted null origin**  
   https://portswigger.net/web-security/cors/lab-null-origin-whitelisted-attack

4. **Practitioner: CORS vulnerability with trusted insecure protocols**  
   https://portswigger.net/web-security/cors/lab-breaking-https-attack

5. **Apprentice: Basic password reset poisoning**  
   https://portswigger.net/web-security/host-header/exploiting/password-reset-poisoning/lab-host-header-basic-password-reset-poisoning

6. **Practitioner: Routing-based SSRF**  
   https://portswigger.net/web-security/host-header/exploiting/lab-host-header-routing-based-ssrf

7. **Practitioner: SSRF via flawed request parsing**  
   https://portswigger.net/web-security/host-header/exploiting/lab-host-header-ssrf-via-flawed-request-parsing

8. **Practitioner: Web cache poisoning via ambiguous requests**  
   https://portswigger.net/web-security/host-header/exploiting/lab-host-header-web-cache-poisoning-via-ambiguous-requests

## Useful learning paths

**Cross-origin resource sharing (CORS)**: https://portswigger.net/web-security/learning-paths/cors

**WebSockets vulnerabilities** *(optional further study)*:
https://portswigger.net/web-security/learning-paths/websockets-security-vulnerabilities

## Quick reference

Headers worth watching:

```http
Host: example.test
Origin: https://attacker.example
Referer: https://example.test/page
Cookie: session=...
Access-Control-Allow-Origin: ...
Access-Control-Allow-Credentials: true
```

Useful questions:
- Does the server trust the `Host` header?
- Is an arbitrary `Origin` reflected?
- Are credentials permitted cross-origin?
- Is `null` accepted as an origin?
- Does the server make a security decision based on a client-controlled header?